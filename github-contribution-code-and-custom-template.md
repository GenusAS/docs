# GitHub contribution code and custom template

The Genus Docs it built using a custom template. When a new versions of DocFX is released, there may be changes that are not effectuated without updating *_custom_templates*. The template contains some customized code for showing contributors. Below is a step by step procedure for updating the exported template. All changes are done locally, tested and pushed to the repository.

## Detect changes in custom template files
### Clear existing default template
Delete all content of *_exported_templates*.

### Create a new default template
Open a command window and navigate to your root catalog. Run the command 
```
docfx template export default
```
### Use git diff detect changes in relevant files
If git diff reports changes in these three files _master.tmpl_, _docfx.css_ and _docfx.js_ in *_exported_templates*. These changes must be merged into the same files in *_custom_templates*.
> [!NOTE]
> Changes in *_exported_template* must also be commited regardless of whether these changes affect the custom template to create a new baseline for future comparison of new DocFX versions.

### Test changes

Build the local docfx version with the template.
```cmd
docfx docfx.json --serve
```
And verify that the site is running correctly and that contributors are loaded.

### Commit changes
Commit changes to GitHub. 


## Contributors code
Edit these three documents, _master.tmpl_, _docfx.css_ and _docfx.js_.


### \_master.tmpl

Add
```xml
<div id="contributors"></div>
```
into the `<article>`-element, before the `{{!body}}`-tag.


### docfx.css

Add
```css
#contributorimg{
    border-radius: 50%;
}
```
after the `a.disable:hover-element`


### docfx.js

Add
```javascript
loadContributors();
```
after all initial function calls, last as of now is `renderTabs()`.

Add
```javascript
function containsName(array, login){
    var i =array.length; 
    while(i--){
        if(array[i].login == login){
            return true;
        }
    }
    return false;
}

function loadContributors() {
    var xhttp = new XMLHttpRequest();
    xhttp.onreadystatechange = function() {
        if (this.readyState == 4 && this.status == 200) {
            generateContributorIcons(JSON.parse(this.responseText));
        }
    };
    
    var relativePath = window.location.pathname.replace('.html','.md')
    if (relativePath==="/"){
        relativePath = "/index.md"
    };

    xhttp.open("GET", "https://api.github.com/repos/GenusBiz/docs/commits?path="+relativePath, true);
    xhttp.send();
}

function generateContributorIcons(list){
    var authors = []
    var lastCommit = list[0].commit.author.date.substr(0,10)
    for (var i=0; i<list.length; i++){
        if(!containsName(authors, list[i].author.login)){
            authors.push({
                name: list[i].commit.author.name,
                email: list[i].commit.author.email,
                login: list[i].author.login,
                avatarUrl: list[i].author.avatar_url,
                html_url: list[i].author.html_url,
                login: list[i].author.login
            });
        }
    }
    
    var lastcommitdate = document.createTextNode(lastCommit)
    var divider = document.createTextNode(' • ')
    var textContributors = document.createTextNode('Contributors ')
    document.getElementById("contributors").appendChild(lastcommitdate)
    document.getElementById("contributors").appendChild(divider)
    document.getElementById("contributors").appendChild(textContributors)
    
    for (var i=0; i<authors.length; i++){
        var img = document.createElement("IMG")
        img.src = authors[i].avatarUrl
        img.name = authors[i].name
        img.height = 28
        img.width = 28
        img.alt = authors[i].login
        img.id ="contributorimg"
        var a = document.createElement("a")
        a.href = authors[i].html_url
        a.alt = authors[i].login
        a.title = authors[i].name
        document.getElementById("contributors").appendChild(a).appendChild(img)
    }
}
```

after the windows.refresh() function declaration.

## Test changes

Build the local docfx version with the template.
```cmd
docfx docfx.json -t _exported_templates\default --serve
```
And verify that the site is running correctly and that contributors are loaded.

## Commit changes
Commit changes to GitHub.