# material-design-inspired-color-picker
> A javascript color picker inspired by material design

### [DEMO](https://bennyalex.github.io/material-design-inspired-color-picker/ "DEMO")

## Features
* built-in material color palette with shades and accent colors
* support for custom color palettes
* display main color first and by clicking on it show its shades or accent colors
* easy to use
* lightweight
* can be used in plain javascript projects or with other js frameworks

## Todo
* add babel, but at the moment it looks like there is an error with rollup-babel plugin  :(
* margin attribute
* number of colors per row attribute
* color-size attribute

## Installation
> npm install material-design-inspired-color-picker --save

## Usage
First include the script in your app. There are two ways to do it.
1. Recommended if you are using es6:
````javascript
import 'material-design-inspired-color-picker'
````
2. Compatible with plain javascript
````html
<script src="path/to/md-color-picker.js"></script>
````
Then, you can use it like a custom-element tag:
````html
<md-color-picker></md-color-picker>
````

A custom elements polyfill is included, so it will work in even in browsers wich do not support the custom-elements specification.

## Api
The picker let you pass in some options and attributes so you can customize it.

Note: In html the attributes are seperated by a hyphen instead of using camelCase in JavaScript.

Following properties can be parsed into the picker:

|propertyname (JS / HTML)|type|default| example|
| :---: | :---:| :---:| :---: |
| colorMargin / color-margin (in px) | number | 6 | 12 |
| colorsPerRow / colors-per-row | number | 5 | 4 |
| colorSize / color-size (in px) | number | 58 | 48 |
| defaultTint / default-tint | number or string | 500 | '200' |
| palette | string or object | 'material' | 'material-full' |
| useSpectrumPicker / use-spectrum-picker | bool | true | false |
| value | string | none | #f1c5a9 |

**Description:**
* colorMargin : The distance between the colors
* colorsPerRow : The number of colors per row
* colorSize : The size of each color circle
* defaultTint : this is the tint for each color wich will be shown at the beginning. Material colors default tint is 500. For custom palettes you can also use strings.
* palette : the palette with all colors. If it is a string, the picker will use a built in palette. Currently the following palettes are available:
````
material : standard material colors 
material-full : the material colors including the accent colors 
material-accent : only the accent material colors
````
* useSpectrumPicker : if false, the other color tints can not be selected, so only the color wich matches default tint is selectable.
* value : the color which is selected. Must be a hex number with 6 digits and a hashtag.

**Full example:**
````html
<md-color-picker value="#abcdef" palette="material-accent" default-tint="300" use-spectrum-picker="false"></md-color-picker>
````

For a more detailed example, see the demo page under docs folder or live: https://bennyalex.github.io/material-design-inspired-color-picker/