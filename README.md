![alt text](/img/logo_parasail.png "Logo Parasail Health")
<br/>
<br/>
<br/>
## TABLE OF CONTENT
- [01 INTRODUCTION](#01-introduction)
- [02 GETTING STARTED](#02-getting-started)
- [03 NAMING CONVENTION - BEM](#03-naming-convention---bem)
- [04 TECHNOLOGIES](#04-technologies)
- [05 GRID SYSTEM](#05-grid-system)
- [06 FLEXBOX](#06-flexbox)
- [07 FORMS](#07-forms)
- [08 TYPOGRAPHY](#08-typography)
- [09 BUTTONS](#09-buttons)
- [10 ALERTS](#10-alerts)
- [11 LOGOS](#11-logos)
- [12 ICONS](#12-icons)
- [13 LISTS](#13-lists)
- [14 HELPER CLASSES](#14-helper-classes)
- [15 BROWSER SUPPORT](#15-browser-support)
- [16 BEST PRACTICES IN CSS](#16-best-practices-in-css)

<br/>
<br/>

## 01 INTRODUCTION
Parasail is a minimalistic CSS framework from Parasail Health using SASS and Flexbox. It's main feature is a Flexbox based grid system which lets you create responsive layouts easily.
<br/>
<br/>
<br/>


## 02 GETTING STARTED
###
###

### INSTALL WITH NPM
Install Parasail using npm:
```
$ npm install parasail
```
<br/>

### USAGE
You can include the file `parasail.min.css` in your header:
```html
<link rel="stylesheet" href="path/to/node_modules/parasail/css/parasail.min.css" >
```
Or you can import the `parasail.scss` file in your own scss file if you want to use our variables:
```html
<link rel="stylesheet" href="path/to/node_modules/parasail/scss/parasail.scss" >
```
<br/>

### CREATE YOUR OWN THEME
We included a file called `_variables.scss` in the `scss` folder which by default loads our Parasail styles. By editing this file you can create your own theme in just a few minutes.
<br/>
<br/>
<br/>

## 03 NAMING CONVENTION - BEM
BEM stands for Block, Element, Modifier, it is a naming convention for classes in HTML and CSS which assists you to write modular CSS. The goal of BEM is, to help developers better understand the relationship between HTML and CSS by quickly giving them an idea of which element depends on another.
<br/>

BEM is successful not because it gives you a lot of options but because it limits what you are allowed to do. The problem it's trying to avoid is getting your rules to match the elements you want, without them accidentally matching the elements you don’t want to affect.
<br/>
<br/>

`Block` is a top-level abstraction of a new component.
```html
<button class="btn">Block</button>
```
<br/>

`Element` depends upon the block.
```html
<button class="btn"> 
    <p class="btn__text">Element</p> 
</button>
```
<br/>

`Modifier` changes the style of the block.
```html
<button class="btn--green">Modifier</button>
```
<br/>

If you want to read more about BEM, check out the [Get BEM introduction](https://getbem.com/introduction/).
<br/>
<br/>
<br/>

## 04 TECHNOLOGIES

### SASS
Sass is the most popular CSS pre-processor on the market today. It is a lightweight tool that lets us write fast, reusable CSS by offering key features such as nested selectors, mixins, conditional statements, and variable declarations.
<br/>
<br/>

### FLEXBOX
Flexbox is a new layout technique that was introduced in CSS3. One of the most difficult concepts for new CSS users to grasp is how to properly align, scale, and position elements across different screen sizes. With Flexbox, we can address this problem with 1-2 lines of code.
<br/>
<br/>
<br/>

## 05 GRID SYSTEM
### GRID
The grid system is based on Flexbox, `.grid` defines a flex container by setting display to flex. It enables a flex context for all its direct children, which are called flex items.
<br/>
<br/>

### GRID COLUMNS
#### .grid_col-x
Different column sizes can be defined by using `.grid__col-1` to `.grid__col-12`, with `.grid__col-1` being the smallest column size and `.grid__col-12` taking up 100% of its parent container.
###
![Alt text](/docs/img/grid-columns.png)
<br/>
<br/>

#### .grid_col-auto
`.grid__col-auto` creates a column that will take up however much space is left in the row.  If the row has multiple `.grid__col-auto` columns, the space gets divided up evenly between the columns.
###
![Alt text](/docs/img/grid-columns-auto.png)
<br/>
<br/>

### GRID COLUMN OFFSET
#### .grid_col-offset-x
Offset a column by adding an offset class: `.grid_col-offset-x`.
###
![Alt text](/docs/img/grid-columns-offset.png)
<br/>
<br/>

### RESPONSIVE LAYOUTS
The grid system lets you create responsive layouts easily by giving you the option to define different column widths for each viewport. The viewports are determined by 4 different breakpoints:
<br/>
<br/>

#### Large: Viewport ≥ 1200px
- Column classes: `.grid__col-lg-1` to `.grid__col-lg-12`
- Column Offset classes: `.grid__col-lg-offset-1` to `.grid__col-lg-offset-12`
<br/>

#### Medium: Viewport ≥ 992px
- Column classes: `.grid__col-md-1` to `.grid__col-md-12`
- Column Offset classes: `.grid__col-md-offset-1` to `.grid__col-md-offset-12`
<br/>

#### Small: Viewport ≥ 768px
- Column classes: `.grid__col-sm-1` to `.grid__col-sm-12`
- Column Offset classes: `.grid__col-sm-offset-1` to `.grid__col-sm-offset-12`
<br/>

#### Extra Small: Viewport ≤ 767px
- Column classes: `.grid__col-xs-1` to `.grid__col-xs-12`
- Column Offset classes: `.grid__col-xs-offset-1` to `.grid__col-xs-offset-12`
<br/>

Using elements with the class `.grid__col-lg-x` defines column widths for the large viewport (min-width: 1200px) and `.grid__col-lg-offset-x` will offset those columns. `.grid-col-md-x` and `.grid-col-md-offset-x` will affect viewports with a min-width of 992px. Elements with the class `.grid__col-sm-x` or `.grid__col-sm-offset-x` will affect the small viewport (min-width: 768px) and `.grid__col-xs-x` defines columns width for the extra small viewport (max-width: 767px) which can be offset with `.grid__col-xs-offset-x`.
<br/>
<br/>
<br/>

## 06 FLEXBOX

### FLEX DIRECTION
Flex Direction defines the direction in which the flex items are placed in the flex container. It is influenced by the text direction property.
###

#### .direction-row
This is the default value, the direction will be the same as the text direction.
###
![Alt text](/docs/img/direction-row.png)
<br/>
<br/>

#### .direction-row-reverse
Setting the flex direction to `row-reverse` will switch the text direction to the opposite.
###
![Alt text](/docs/img/direction-row-reverse.png)
<br/>
<br/>

#### .direction-column
`Direction-column` behaves the same way as `direction-row` but it influences the vertical direction, so top to bottom.
###
![Alt text](/docs/img/direction-column.png)
<br/>
<br/>

#### .direction-column-reverse
`Direction-column-reverse` behaves the same way as `row-reverse` but it influences the vertical direction, so top to bottom.
###
![Alt text](/docs/img/direction-column-reverse.png)
<br/>
<br/>

### FLEX WRAP
`Flex-wrap` defines whether the flex items are forced in a single line or can be flowed into multiple lines if there isn't enough room for them on one flex line.
###

#### .nowrap
Default value, the flex items will not wrap.
###
![Alt text](/docs/img/nowrap.png)
<br/>
<br/>

#### .wrap
The flex items will wrap if necessary.
###
![Alt text](/docs/img/wrap.png)
<br/>
<br/>

#### .wrap-reverse
The flex items will wrap if necessary but in reverse order.
###
![Alt text](/docs/img/wrap-reverse.png)
<br/>
<br/>

### JUSTIFY CONTENT
`Justify-content` defines how flex items are aligned along the main-axis (that means by default horizontally, left to right). It helps distribute extra space between the items when they don't use all available space on the main-axis.
###

#### .justify-start
Default value, the items are positioned at the beginning of the container.
###
![Alt text](/docs/img/justify-start.png)
<br/>
<br/>

#### .justify-end
The items are positioned at the end of the container.
###
![Alt text](/docs/img/justify-end.png)
<br/>
<br/>

#### .justify-center
`Justify-center` will position the items at the center of the container.
###
![Alt text](/docs/img/justify-center.png)
<br/>
<br/>

#### .justify-space-between
Items are evenly spread horizontally, the first item is at the beginning of the container, the last item on the end of the container. The space gets distributed between the items.
###
![Alt text](/docs/img/justify-space-between.png)
<br/>
<br/>

#### .justify-space-around
The items are positioned with equal space before, between and after them.
###
![Alt text](/docs/img/justify-space-around.png)
<br/>
<br/>

### ALIGN ITEMS
This part is one of the best features of Flexbox because before Flexbox it was very painful to properly center elements vertically.
###

`Align-items` defines how flex items are aligned along the cross-axis (which is by default vertically, top to bottom) when they don't take up all of the available space in the container. It is the justify-content version for the cross-axis.
###

#### .align-stretch
Default value, it stretches the height of the flex item to fit the container (still respects min-width/max-width).
###
![Alt text](/docs/img/align-stretch.png)
<br/>
<br/>

#### .align-start
Flex items are positioned at the top of the container.
###
![Alt text](/docs/img/align-start.png)
<br/>
<br/>

#### .align-end
Flex items are positioned at the bottom of the container.
###
![Alt text](/docs/img/align-end.png)
<br/>
<br/>

#### .align-center
Flex items are positioned at the vertical center of the container (centered in the cross-axis).
###
![Alt text](/docs/img/align-center.png)
<br/>
<br/>

#### .align-baseline
Flex items are positioned at the baseline of the container.
###
![Alt text](/docs/img/align-baseline.png)
<br/>
<br/>

### ALIGN SELF
`Align Self` accepts the same 5 values as `align items`, with the difference that you apply it to individual flex items in order to overwrite `align items`.
###

#### .align-self-stretch
Default value, it stretches the height of the flex item to fit the container (still respects min-width/max-width).
###
![Alt text](/docs/img/align-self-stretch.png)
<br/>
<br/>

#### .align-self-start
Flex item gets positioned at the top of the container.
###
![Alt text](/docs/img/align-self-start.png)
<br/>
<br/>

#### .align-self-end
Flex item gets positioned at the bottom of the container.
###
![Alt text](/docs/img/align-self-end.png)
<br/>
<br/>

#### .align-self-center
Flex item gets positioned at the vertical center of the container (centered in the cross-axis).
###
![Alt text](/docs/img/align-self-center.png)
<br/>
<br/>

#### .align-self-baseline
Flex item gets positioned at the baseline of the container.
###
![Alt text](/docs/img/align-self-baseline.png)
<br/>
<br/>
<br/>

## 07 FORMS
We added basic styles for form elements, all values for form variables can be changed in the file `_variables.scss`.
###

### LABEL
`.form__label` gives you the option to change the font-size as well as the color.
<br/>
<br/>

### INPUT + SELECT
`.form__input` lets you change the font-size, text, placeholder, background and border color.
<br/>
<br/>

### RADIO BUTTONS
Input fields with type="radio" don't allow you to set a placeholder. To add a placeholder to a radio button, you need to add a label and make the label the actual placeholder. In order to still make it look like a button, wrap the label as well as the input in a div with the class="form__radio-btn".
###

```html
<div class="form__radio-btn"> 
    <input id="id" name="name" type="radio" /> 
    <label for="id">Great 760+</label> 
</div>
```
<br/>

### EXAMPLE
###
![Alt text](/docs/img/example-form.png)
<br/>
<br/>
<br/>

## 08 TYPOGRAPHY

### .text--left
Aligns the text on the left.
###
![Alt text](/docs/img/text--left.png)
<br/>
<br/>

### .text--center
Aligns the text in the center.
###
![Alt text](/docs/img/text--center.png)
<br/>
<br/>

### .text--right
Aligns the text on the right.
###
![Alt text](/docs/img/text--right.png)
<br/>
<br/>

### .text--uppercase
Transforms all characters to uppercase.
###
![Alt text](/docs/img/text--uppercase.png)
<br/>
<br/>

### .text--lowercase
Transforms all characters to lowercase.
###
![Alt text](/docs/img/text--lowercase.png)
<br/>
<br/>

### .text--capitalize
Transforms the first character of each word to uppercase.
###
![Alt text](/docs/img/text--capitalize.png)
<br/>
<br/>
<br/>

## 09 BUTTONS
The theme currently includes 4 different button styles, you can update the colors as well as the font-size in the _variables.scss file.
###

### .btn--default
![Alt text](/docs/img/btn--default.png)
<br/>
<br/>

### .btn--primary
![Alt text](/docs/img/btn--primary.png)
<br/>
<br/>

### .btn--secondary
![Alt text](/docs/img/btn--secondary.png)
<br/>
<br/>

### .btn--error
![Alt text](/docs/img/btn--error.png)
<br/>
<br/>

### EXAMPLE
```html
<button class="btn--default">Default</button>
```
<br/>
<br/>
<br/>

## 10 ALERTS
Use one of these 4 alert classes if you need to display a notification message to the user.
###

### .alert--success
![Alt text](/docs/img/alert--success.png)
<br/>
<br/>

### .alert--info
![Alt text](/docs/img/alert--info.png)
<br/>
<br/>

### .alert--warning
![Alt text](/docs/img/alert--warning.png)
<br/>
<br/>

### .alert--error
![Alt text](/docs/img/alert--error.png)
<br/>
<br/>

### EXAMPLE
```html
<div class="alert--success">This is a success message</div>
```
<br/>
<br/>
<br/>

## 11 LOGOS
By default the theme is loading the Parasail logo and gives you the option to use it in 3 different sizes. Simply go into the `_variables.scss` file and change the `$logo` variable to load your own logo. If you want to change the width and height ratio, you can do this by changing the values in the `_logos.scss` file.
###

### .logo
![Alt text](/docs/img/logo.png)
<br/>
<br/>

### .logo--md
![Alt text](/docs/img/logo--md.png)
<br/>
<br/>

### .logo--xs
![Alt text](/docs/img/logo--xs.png)
<br/>
<br/>
<br/>

## 12 ICONS
These are some icons we currently use, you can update the colors as well as the font-sizes in the `_variables.scss` file.
###

### .icon__arrow
![Alt text](/docs/img/icon__arrow.png)
```html
<span class="icon__arrow"></span>
```
<br/>

### .icon__close
![Alt text](/docs/img/icon__close.png)
```html
<span class="icon__close"></span>
```
<br/>

### .icon__question-mark
![Alt text](/docs/img/icon__question-mark.png)
```html
<span class="icon__question-mark"></span>
```
<br/>
<br/>
<br/>

## 13 LISTS
###

### .ordered-list
The list items are marked with numbers.
###

1. Ordered List Item 1
2. Ordered List Item 2
3. Ordered List Item 3
<br/>

### .unordered-list
The list items are marked with bullets.
###

- Unordered List Item 1
- Unordered List Item 2
- Unordered List Item 3
<br/>
<br/>
<br/>

## 14 HELPER CLASSES
### ALIGNMENT

### .align--left
Aligns block elements to the left.
###
![Alt text](/docs/img/align--left.png)
<br/>
<br/>

### .align--center
Centeres block elements.
###
![Alt text](/docs/img/align--center.png)
<br/>
<br/>


### .align--right
Aligns block elements to the right.
###
![Alt text](/docs/img/align--right.png)
<br/>
<br/>
<br/>

## 15 BROWSER SUPPORT
The Parasail framework uses Flexbox, the included grid system, for example, is based entirely on Flexbox. Flexbox is supported by all major browsers, as well as IE10 and higher, with the exception of Opera mini.
<br/>

Every project targets a different audience. Therefore, browser support is something that needs to be decided on an individual basis. Parasail focuses on providing a lightweight CSS framework that can be used for any project, for the simple reason that we do not wish to decide between which browsers to support.
<br/>

For supporting older browsers for your project, we recommend using [Autoprefixer](https://github.com/postcss/autoprefixer). Autoprefixer is an amazing tool that lets you specify which browser version you want to support, and automatically prefixes your CSS with the correct vendor prefixes.
<br/>

If you are looking to support IE9 and lower, you will need to add a polyfill such as [Flexibility](https://github.com/jonathantneal/flexibility).
<br/>
<br/>
<br/>

## 16 BEST PRACTICES IN CSS
###

### FORMATTING
- Don't nest further than 3 levels deep
- Use 2 spaces for indentation
- When using multiple selectors in a rule declaration, give each selector it's own line
- Put a space before the opening brace { in rule declarations
- In properties, put a space after, but not before, the : character.
- Put closing braces } of rule declarations on a new line
<br/>

### IDS
- Avoid using IDs unless that element is suppose to be a Javascript identifier.
- They are not reusable and introduce unnecessarily specificity to your rule declaration.
<br/>

### COMMENTS
- Put comment on its own line
- Avoid using end-of-line comments
- Write comments for code that isn't self-documenting (for example Browser hacks)
- When writing comments in SASS, keep in mind that comments using the double slash ( `// Double slash comment` ) will not be compiled to regular CSS while comments using the slash + asterix ( `/* Comment using slash + asterix */` ) will be compiled. 
<br/>

### EXAMPLE
```
.grid,
.grid__col-auto {
    // display: inline-block added for IE support
    display: inline-block;
}
```
<br/>
<br/>

## LICENSE

Licensed under the [MIT License](https://github.com/Parasail-Health/parasail/blob/master/LICENSE.txt).

