---
title: Release notes for Genus release 2019.2.
description: User-visible changes to Genus from release 2019.1 to 2019.2.
author: jtroset
---
# Release notes for version 2019.2

## Introduction

This document lists all user-visible changes to Genus Apps since the previous release.
 
This release note will be updated prior to the release and may also be updated as long as the release is available, e.g. with information of new patches or known issues. Please take note of the [installation and upgrading](#installation-and-upgrading) comments, and the release notes [change log](#change-log).

## Installation and upgrading
 
Prior to upgrading to this release, you must:
* Upgrade to the previous release. See the Release notes for the previous release for more information.
* Review the Expiry date of your Genus License File and install a new one if necessary.
* Review the rest of the release notes for this release.
* Please note that there does not exist any Genus Upgrade Assistant for this upgrade.
 
For general information about installing and upgrading Genus Apps, see [here](../installation-and-configuration/index.md). We especially recommend reviewing the [System Requirements](../installation-and-configuration/system-requirements.md) article.

## Important issues in this release

There are currently no critical issues in this release.

<!--rntype01-start INSTALLATION / UPGRADE. DO NOT CHANGE THESE TAGS. ANY CHANGES BELOW WILL BE OVERWRITTEN.-->

<!--rntype01-end   INSTALLATION / UPGRADE. DO NOT CHANGE THESE TAGS. ANY CHANGES ABOVE WILL BE OVERWRITTEN.-->
<!-- release note type 2 is missing. That's ok.-->

## End-of-life functionality

End-of-life functionality is functionality that was available in the previous release, but is no longer available in this release.
<!--rntype03-start END-OF-LIFE. DO NOT CHANGE THESE TAGS. ANY CHANGES BELOW WILL BE OVERWRITTEN.-->
There are no end-of-life functionality identified in this release.
<!--rntype03-end   END-OF-LIFE. DO NOT CHANGE THESE TAGS. ANY CHANGES ABOVE WILL BE OVERWRITTEN.-->
## Deprecated functionality

Deprecated functionality is available in this release, but will (most probably) no longer be available in the next release.
<!--rntype04-start DEPRECATED. DO NOT CHANGE THESE TAGS. ANY CHANGES BELOW WILL BE OVERWRITTEN.-->
There is no deprecated functionality in this release.
<!--rntype04-end   DEPRECATED. DO NOT CHANGE THESE TAGS. ANY CHANGES ABOVE WILL BE OVERWRITTEN.-->
## Breaking changes

This section lists important changes introduced in this release. You will need to use this list in order to understand the changes you might need to make to your application to support the new release.
<!--rntype05-start BREAKING. DO NOT CHANGE THESE TAGS. ANY CHANGES BELOW WILL BE OVERWRITTEN.-->
There are no breaking changes in this release.
<!--rntype05-end   BREAKING. DO NOT CHANGE THESE TAGS. ANY CHANGES ABOVE WILL BE OVERWRITTEN.-->
## Major new functionality
<!--rntype06-start MAJOR. DO NOT CHANGE THESE TAGS. ANY CHANGES BELOW WILL BE OVERWRITTEN.-->
There are no major new functionality in this release.
<!--rntype06-end   MAJOR. DO NOT CHANGE THESE TAGS. ANY CHANGES ABOVE WILL BE OVERWRITTEN.-->
## Minor new functionality
<!--rntype07-start MINOR. DO NOT CHANGE THESE TAGS. ANY CHANGES BELOW WILL BE OVERWRITTEN.-->
<!--ID 606ea95b-b89b-4bca-9f2d-20e29f78604f -->
**#23171 Implemented options to specify content type for Multipart requests in Consume Rest Service effect** (Desktop;Services)

It is now possible to specify the content type of both the root of multipart requests (typically multipart/form-data or multipart/mixed) and also for the individual parts og a multipart request.

<!--ID a45c231a-3fbd-46ca-97f7-0ec8d1917a7b -->
**#23172 Context menu closes on Escape and clicks** (Desktop)

The context menu (right-click menu) now closes on Escape and clicks

<!--ID 8bc8ea13-e641-4bfa-bf01-7114170c3a6e -->
**#23173 Better handling of "The data mart has new data"** (Desktop)

When  the data mart has new data, we load the new data and try to keep the current selection. A snackbar message notifies the user that "The Data Mart has been reloaded with new data".

<!--ID 8c5a44d5-d72d-44e3-a761-ad4bdab73fff -->
**#23174 Better handling of tile rendering errors** (Desktop;Studio)

If tile rendering fails due to an unknown error, we only display "Rendering tile failed" on the tile, instead of showing a modal/dialog you have to close.

<!--ID 25060f68-c16c-41e1-ba46-c03470799384 -->
**#23175 Display a message if a bookmark has been deleted** (Desktop)

A small message (snackbar) is shown to the user if he/she tries to open a bookmark that has been deleted (ie. does not exist).

<!--ID 7ad63bbc-55f4-448b-953b-5d6c08cc3339 -->
**#23180 Sunburst can now be downloaded as an image**

<!--ID dcacd374-ea49-4137-a101-7609a5b6729d -->
**#23181 Added option to show details for fields when adding them to the published fields of a data mart**

<!--ID 5a0b8cfb-2397-4867-8bc5-e3f6a4e9531d -->
**#23194 Selections in Sankey** (Desktop;Web)

It is now possible to do selections in Sankey

<!--ID 466467f3-8914-48f2-aa9e-0050f4504dbe -->
**#23201 Handle special aggregation results in Discovery** (Desktop;Web)

Handle the special aggregation results NaN (ie. no observations), NegInfinity and Infinity

<!--ID 499511ae-8939-410a-8596-348b0b54f9c5 -->
**#23204 Subset added as option for mapping when opening tabls/forms/analysis** (Desktop;Web)

Added subset as a new mapping-type when specifying what data should be transferred when opening forms/tables from an analysis.

<!--rntype07-end   MINOR. DO NOT CHANGE THESE TAGS. ANY CHANGES ABOVE WILL BE OVERWRITTEN.-->
## Resolved issues
<!--rntype08-start RESOLVED ISSUES. DO NOT CHANGE THESE TAGS. ANY CHANGES BELOW WILL BE OVERWRITTEN.-->
<!--ID 64225008-5d3f-4724-98ad-209428a3aae7 -->
**#23176 Removed option for creating formula in map layer values** (Studio)

Formulas for maps are not currently supported, but it was still possible to define formulas in map layer values. This possibility is now removed

<!--ID ce936e01-3fe3-4010-a8dd-ae8db39d4670 -->
**#23177 Number format on formula value was cleared after editing formula** (Studio)

Number format on formula value formulas are no longer cleared after editing formulas

<!--ID d7d65bbb-55ea-4d5f-9fe6-d21371b37330 -->
**#23178 Resolved by reducing thread-locking when dumping call stacks on errors** (Desktop)

<!--ID 23ab62a2-3f1a-4451-ac67-74cc89b55241 -->
**#23179 Forced lower-case when specifying virtual directory for a dataset to avoid cookie-conflicts**

<!--ID e653b8e1-46c5-4dd4-8829-9ed81e537085 -->
**#23182 Fixed doble save as dialog when saving analysis**

<!--ID 9d48a32a-1f59-4c2c-8a28-f9361fdbe26f -->
**#23183 Fixed problem with escape key closing analysis window instead of popup or menu**

<!--ID a9b65be8-a1a9-4b28-95ce-3714f5d70a63 -->
**#23184 Theme** (Desktop;Web)

Modified the appearance of some dialogs to be more user-friendly.

<!--ID 1ac7b1be-ffbc-42c8-8f4f-36d4f4931b4b -->
**#23185 Transposed Table** (Desktop;Web)

Fixed an issue where transposed table would not display values.

<!--ID 9b958d69-d20e-419e-8947-db0b8b03943e -->
**#23186 Summary** (Desktop;Web)

Fixed an issue where NaN would be displayed as result, instead of the actual result.

<!--ID 48bac3f7-5e8f-439f-aca2-8690ca3312c8 -->
**#23187 Summary popup** (Desktop;Web)

Fixed errors with summary popup that could result in the tile not displaying correctly.

<!--ID 26f44e3f-2b00-4310-82d9-77c5c5316493 -->
**#23188 Open Analysis** (Desktop;Web)

Fixed issues that could lead to the current selection not being properly applied when switching between different analysis.

<!--ID f67ef90b-51ac-4fb6-83ec-725fb17e64de -->
**#23189 Theme** (Desktop;Web)

Fixed an issue where the theme editor did not start properly, and modified the default theme

<!--ID a6d056f7-6a20-4452-8286-3128ca5b955e -->
**#23190 Variable Radius Pie** (Desktop;Web)

Fixed an issue where when making an selection, the wrong item would be selected

<!--ID eca11c27-15d9-4937-b4d0-c8756cf066a8 -->
**#23191 Improved hotspot- and heatmap-layer for maps in Analysis** (Desktop;Web)

The map layers now supports using aggregated values for intensity (heatmap), and size and color (hotspot). 

Heatmap now also supports filtering.

<!--ID 26c34e2a-e11d-4cb1-9aa6-7dc5ea7e1390 -->
**#23192 Clustering of points in maplayers now toggles correctly** (Desktop;Web)

Clustering of points in point-layer and hotspot-layer should now work as expected.

<!--ID b1acf31e-6d86-40a2-967c-920e3733db50 -->
**#23193 Icons on points in pointlayer for map in analsysis now displayed correctly** (Desktop;Web)

<!--ID 357a2c0e-924d-4995-b783-a98ad3a03a4e -->
**#23195 Floor & Ceiling** (Desktop;Web)

Fixed an issue where setting the floor equal to zero would cause the graph to display empty.

<!--ID 66738bf0-8272-409c-a8a6-e6c8f07a4803 -->
**#23196 Selector** (Desktop;Web)

Redesign of how the selector works in terms of applying selections in the global scope.

<!--ID 41bf5d6a-354c-4d76-a49b-faf6bc2e3231 -->
**#23197 Fixed issue where "Open in new window" did not appear in the right-click/context menu** (Desktop;Web)

<!--ID 8a3d9c61-86b9-4e64-b5dd-8af040711b9c -->
**#23198 Table** (Desktop;Web)

Fixed an issue where limit would always be set to 1, even if the user modified the value.

<!--ID 4ffc490c-cab5-44bd-8dca-97a3888009e4 -->
**#23199 Better error handling in Discovery** (Desktop;Web)

Improved error handling in Discovery. If an unknown error occured, the user won't be presented with unnecessary, technical error information

<!--ID a6a04adc-4b0e-47d9-bcf8-a59be5b6edc8 -->
**#23200 Column total for formula with "zero if missing"** (Desktop;Web)

Fixed an issue where a total aggregate (a sum) was not displayed for a column if any of the observations it was aggregating over was missing.

<!--ID 4fd53f02-9523-47dd-884c-43f1a66ac005 -->
**#23202 Browsing through objects in a form containing an RTF editor marks the objects as changed** (Desktop)

In a form containing an RTF editor the object is marked as changed when the user browses through objects using the next/previous functionality. The save button is immediately enabled, and it is not possible to go to the next or previous object before the object is saved.

<!--ID 9e3dc11f-9857-4490-85fe-6585f06b1540 -->
**#23203 Data validation error for an object class property containing an RTF document not displayed correctl** (Desktop)

If the data size is set for an object class property containing an RTF document, violation of the size is not displayed correctly by the RTF editor.

<!--rntype08-end   RESOLVED ISSUES. DO NOT CHANGE THESE TAGS. ANY CHANGES ABOVE WILL BE OVERWRITTEN.-->
## Known issues

Known issues are errors or lack of functionality. Known issues may be solved in a future release based on customer demand.
<!--rntype09-start KNOWN ISSUES. DO NOT CHANGE THESE TAGS. ANY CHANGES BELOW WILL BE OVERWRITTEN.-->
There are no known issues in this release.
<!--rntype09-end   KNOWN ISSUES. DO NOT CHANGE THESE TAGS. ANY CHANGES ABOVE WILL BE OVERWRITTEN.-->
## Tips and hints

Tips and hints are design decisions or answers to support questions that may be of general interest.
 
There are no tips and hints specifically targeting this release.

## Change log
* 2019-04-01 Released (builds starting with 18.45.21).
* 2019-03-27 Created (builds starting with 18.45.1).
<!--changelog CHANGELOG. DO NOT CHANGE THIS TAG. ANY CHANGES BELOW WILL BE DELETED.-->