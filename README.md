[<img src="http://i.imgur.com/ihzCgEr.png">](http://concisecss.com/)

This is the branch where the next version of ConciseCSS is being built.
Although the final picture is still blurry I'll try to write here all the details and planned changes.
Anything written here may change.

## Architecture
ConciseCSS v3 already uses add-ons to extend the functionality of the framework, however, the core and the UI add-on are already pretty large. In this new version (v4), the core will be as minimal as possible. No classes and no excessive styles, just some basic ones for the default HTML elements and an extensive interface for the add-ons.
The core will be composed of two main components/sections; Base styles and what I call the Concise Style Interface.

### Base Styles
They provide a foundation for further styling by the user, overriding the default browser styles. The goal of this is to reduce the amount of custom CSS. The user should be able to include this styles in a CSS file and get a good result without using any extra rules (for a document-based site at least).

### Concise Style Interface
An array of variables provided for the add-ons and the end-user. The user should be able to edit those variables and the changes will be reflexed across the whole stylesheet. Add-ons should use those variables whenever is possible. Also, add-ons should be able to extend the Interface with exclusive variables for the add-on. All the variables should be namespaced (or some similar approach) to avoid conflicts.

### Official Add-ons
ConciseCSS will have some official add-ons. Basic useful components will be officially provided by ConciseCSS

- atGrid: Attribute-and-Float-based Grid System.
- FlexGrid: Attribute-and-Flexbox-based Grid System.
- Debug: Outlines the elements depending on the type.
- UI: A basic user interface kit.
- Add-on: A boilerplate to build new add-ons.
- Utils: Single purpose classes to adjust the design (margins, borders, paddings, etc).
