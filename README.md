# CSS Layout

Thursday, 11 August 2022

# Contents

1. __Display Types____
2. __Position Attributes__
3. __Box Model__

# Display Properties

### Block Display:

`display: inline;`

- Takes up the __entire horizontal space__ of its parent element, and as much vertical space as its content.
- Always starts on a new line.
- Often used to create structures and layouts.
- Most elements are block display elements.
  - `<div>` This is a block `</div>`

__*More Information*__: [Block-level Elements - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements)

### Inline Display:

`display: block;`

- Only accomodates as much space as required by their content.
- Does __not__ start on a new line.
- Can fit inside block-level elements.

- Can not have their size altered, unless:
- `display: inline-block;` : Keeps as inline display, but allows you to position or add width/height.
  - `<span>` This is inline `</span>`

__*More Information*__: [Inline Elements - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements)

### Overflow

- If content is larger than the size of the element, it will overflow.
- The default value of the overflow property is visible.

__*More Information*__: [Overflow - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow)

# Position Attribute

#### How an element position itself in relation to other elements around it.

### Static Position:

- Positioned according to the normal flow of the document.
- Default value (`top`, `right`, `bottom`, `left` and z-index properties have no effect).

### Relative Positioning:

`position: relative;`

- Allow you to position an element relative to where it's supposed to be on the document.
- Does not visually impact other nearby elements.
  - `Top: #px;`: Moves down
  - `Bottom: #px;`: Moves Up
  - `Left: #px;`
  - `Right: #px;`
    - *Also applies to absolute positioning.

### Absolute Positioning:

`position: absolute;`
- Element is taken out of the static flow of the document.

- Automatically moves to _the nearest positioned ancestor_.

``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Three Boxes</title>
</head>
<body>
    <style>
        .box {
            width: 100px;
            height: 100px;
        }
        #box1 {background: red}
        #box2 {background: blue}
        #box3 {background: green}
    </style>
    <div class="box" id="box1"></div>
    <div class="box" id="box2"></div>
    <div class="box" id="box3"></div>
</body>
```

__*More Information*__: [Positioning - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/position)

# Inheritance

### In CSS, inheritance controls what happens when __no value is specified__ for a property on an element.

### CSS properties can be categorized in two types:

- __Inherited Properies__: Set to the _computed_ value of __parent element__ _(by default)_.
- __Non-Inherited Properties__: Set to _intial_ value of the __property__ _(by default)_.

__*More Information*__: [Inheritance - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/inheritance)

# Box Model

### Refers to how HTML elements are modeled in browser engine and how the dimensions of those HTML elements are derived from CSS properties.
  
  ![CSS Box Model](https://upload.wikimedia.org/wikipedia/commons/7/7a/Boxmodell-detail.png)

### __Contains 4 Parts:__

1. __Margin__: `margin: 25px;`
   - All of the space surrounding the element. _(block)_

    __*More Information*__: [Margin - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)

2. __Border__: `border: 5px solid black;`
   - A border that is directly around the element. _(outline)_

3. __Padding__: `padding: 15px;`
    - Space directly inside of the box.
    - Can move content away from border.

    __*More Information*__: [Padding - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)
  
4. __Content__: Center of the box.

``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <style>
        .box {
            width: 100px;
            height: 100px;
            background: lightblue;
            border: 5px solid black;
            margin: 25px;
            padding: 15px;
        }
    </style>
    <div class="box">Content</div>
</body>
```
__*More Information*__: [Introduction to the CSS Basic Box Model - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)

# __Box Sizing:__

`box-sizing: border-box;`
  - Determines how the size of a box is calculated.
  - Specifically, whether or not the padding and border are caculated as part of the element's width and height.

## `Content-Box`

- Default sizing for elements.
- If we do not set a box-sizing property or element will default to using `content-box`.
- `Padding` and `border` add to the size of the element but `margin` does not.

## `Border-Box`

- If the `box-sizing` property is set to `border-box`, then the size of the element will be inclusive of padding and border. 
- Margin will always add space around the element.

__*More Information*__: [Box-Sizing - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing)

# Colours

__*More Information*__: [Color - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)

### Colours can be represented by:

#### __Named Colours__
  - Keywords *(red, green, coral etc.)*

    ``` html
    p {
    color: red;
    }
    ```

__*More Named Colours*__: [Color Names - HTML Color Codes](https://htmlcolorcodes.com/color-names/)

#### __RGB__
- Defines colours by providing a __value of intensity__ between `0` and `255` to the red, green, and blue channels.

    ``` html
    p {
        color: rgb(200, 0, 255);
    }
    ```

#### __HSL__
- Some (not all) browsers support defining colours using `hue`, `saturation`, and `lightness`.
- `Hue`: Degree between `0` and `360` on colour wheel.
- `Saturation` & `Lightness`: Percentage values.

    ``` html
    p {
        color: hsl(120, 50%, 50%);
    }
    ```

__*HSL Color Picker*__: [HSL Picker](https://hslpicker.com/)

#### Hexadecimal
- Uses a __base 16 number system__.

    ``` html
    p {
        color: #ff0099;
    }
    ```
