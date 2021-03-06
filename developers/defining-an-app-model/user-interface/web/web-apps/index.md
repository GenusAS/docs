# Web apps

The fundamental purpose of a web app is to facilitate the completion of one or more tasks. To do so, the web app provides multiple destinations for interacting with the user, where each destination is represented by a web component, such as a form, an analysis, a map, or a diagram. Web components are defined separately from the web app. Users can navigate to different destinations from the navigation menu, or by invoking actions attached to UI elements, such as a button.

## Main elements

The layout for a web app is composed of three main elements:

* The app bar
* The navigation drawer
* A content area 

### App bar
The app bar which appears at the top of the screen is used for branding, navigation, search, and built-in actions.

### Navigation drawer
The navigation drawer provides access to destinations in the web app. It can either be permanently on-screen, or controlled by the navigation menu icon in the app bar. The navigation drawer is displayed to the left side of the content.

The navigation drawer contains a menu including folders and entries to various web components defined in your app model, such as a form.

### Content area
When a user selects an entry in the navigation menu, or navigates to a web component by invoking an action, the content for the web component is displayed in this area. The content area is located to the right of the navigation drawer.

## The purpose of a web app
When building a web app, there are a number of well-known guides to follow. One is to keep the app as focused as possible. An app that has a specific, focused purpose can be optimized in many aspects such as content, device support, and means of interaction. However, enterprise solutions tend to try to cover a lot of purposes. Building a single app for every purpose will lead to many apps. Normally this is a challenge, but since we have a single shared app model you can easily allow users to navigate between the apps defined in your app model. That is, you can combine single purpose apps into a multi-purpose enterprise solution.
