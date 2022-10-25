HTML boilerplate: https://www.freecodecamp.org/news/basic-html5-template-boilerplate-code-example/

OVERVIEW = What is CSS, What are CSS properties, What are CSS units, What are CSS Selectors

- What is CSS
  - HTML gives us “default” styles for every element
  - CSS is a rule-based language — you define the rules by specifying groups of styles that should be applied to particular elements or groups of elements on your web page.
  - CSS properties / HTML elements / HTML properties (go over the lingo)
  - Inline styles vs CSS stylesheets
  - CSS units
    - Relative vs absolute
      | px  | Absolute pixels (1px = 1/96th of 1in)          |
      | --- | ---------------------------------------------- |
      | %   | Relative to the parent element                 |
      | rem | Relative to font-size of the root element      |
      | vw  | Relative to 1% of the width of the viewport\*  |
      | vh  | Relative to 1% of the height of the viewport\* |
- What are CSS properties
  - Most popular
    - Color
    - Font Size
    - Font Family
    - Background Color
    - Background
    - Margin
    - Padding
    - Height/Width
    - Border
    - Border Radius
  - Advanced properties
    - Display:
      | inline       | Displays an element as an inline element (like <span>). Any height and width properties will have no effect                                             |
      | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
      | block        | Displays an element as a block element (like <p>). It starts on a new line, and takes up the whole width                                                |
      | inline-block | Displays an element as an inline-level block container. The element itself is formatted as an inline element, but you can apply height and width values |
      | flex         | Displays an element as a block-level flex container                                                                                                     |
      | grid         | Displays an element as a block-level grid container                                                                                                     |
    - Position:
      | absolute | The element is positioned relative to its first positioned (not static) ancestor element                                                                                                                                                                                                                                                                                                         | Play it » |
      | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------- |
      | fixed    | The element is positioned relative to the browser window                                                                                                                                                                                                                                                                                                                                         | Play it » |
      | relative | The element is positioned relative to its normal position, so "left:20px" adds 20 pixels to the element's LEFT position                                                                                                                                                                                                                                                                          | Play it » |
      | sticky   | The element is positioned based on the user's scroll position A sticky element toggles between relative and fixed, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "sticks" in place (like position:fixed).Note: Not supported in IE/Edge 15 or earlier. Supported in Safari from version 6.1 with a -webkit- prefix. |           |
    - Keyframes: [https://www.w3schools.com/cssref/tryit.php?filename=trycss3_keyframes](https://www.w3schools.com/cssref/tryit.php?filename=trycss3_keyframes)
      ```jsx
      div {
      	width: 100px;
      	height: 100px;
      	background: red;
      	position: relative;
      	animation: mymove 5s infinite;
      }
      ```
      ```jsx
      @keyframes mymove {
      	from {top: 0px;}
      	to {top: 200px;}
      }
      ```
    - Transform: [https://developer.mozilla.org/en-US/docs/Web/CSS/transform#try_it](https://developer.mozilla.org/en-US/docs/Web/CSS/transform#try_it)
      ```jsx
      div.a {
      	transform: rotate(20deg);
      }
      ```
- What are CSS selectors? [https://www.w3schools.com/cssref/css_selectors.php](https://www.w3schools.com/cssref/css_selectors.php)
  | .class               | .intro                | Selects all elements with class="intro"                                                              |
  | -------------------- | --------------------- | ---------------------------------------------------------------------------------------------------- | ---- | ------------------------------------------------------------------------------------- |
  | .class1.class2       | .name1.name2          | Selects all elements with both name1 and name2 set within its class attribute                        |
  | .class1 .class2      | .name1 .name2         | Selects all elements with name2 that is a descendant of an element with name1                        |
  | #id                  | #firstname            | Selects the element with id="firstname"                                                              |
  | \*                   | \*                    | Selects all elements                                                                                 |
  | element              | p                     | Selects all <p> elements                                                                             |
  | element.class        | p.intro               | Selects all <p> elements with class="intro"                                                          |
  | element,element      | div, p                | Selects all <div> elements and all <p> elements                                                      |
  | element element      | div p                 | Selects all <p> elements inside <div> elements                                                       |
  | element>element      | div > p               | Selects all <p> elements where the parent is a <div> element                                         |
  | element+element      | div + p               | Selects the first <p> element that is placed immediately after <div> elements                        |
  | element1~element2    | p ~ ul                | Selects every <ul> element that is preceded by a <p> element                                         |
  | [attribute]          | [target]              | Selects all elements with a target attribute                                                         |
  | [attribute=value]    | [target=_blank]       | Selects all elements with target="\_blank"                                                           |
  | [attribute~=value]   | [title~=flower]       | Selects all elements with a title attribute containing the word "flower"                             |
  | [attribute           | =value]               | [lang                                                                                                | =en] | Selects all elements with a lang attribute value equal to "en" or starting with "en-" |
  | [attribute^=value]   | a[href^="https"]      | Selects every <a> element whose href attribute value begins with "https"                             |
  | [attribute$=value]   | a[href$=".pdf"]       | Selects every <a> element whose href attribute value ends with ".pdf"                                |
  | [attribute*=value]   | a[href*="w3schools"]  | Selects every <a> element whose href attribute value contains the substring "w3schools"              |
  | :active              | a:active              | Selects the active link                                                                              |
  | ::after              | p::after              | Insert something after the content of each <p> element                                               |
  | ::before             | p::before             | Insert something before the content of each <p> element                                              |
  | :empty               | p:empty               | Selects every <p> element that has no children (including text nodes)                                |
  | :first-child         | p:first-child         | Selects every <p> element that is the first child of its parent                                      |
  | ::first-letter       | p::first-letter       | Selects the first letter of every <p> element                                                        |
  | ::first-line         | p::first-line         | Selects the first line of every <p> element                                                          |
  | :first-of-type       | p:first-of-type       | Selects every <p> element that is the first <p> element of its parent                                |
  | :focus               | input:focus           | Selects the input element which has focus                                                            |
  | :fullscreen          | :fullscreen           | Selects the element that is in full-screen mode                                                      |
  | :hover               | a:hover               | Selects links on mouse over                                                                          |
  | :last-child          | p:last-child          | Selects every <p> element that is the last child of its parent                                       |
  | :last-of-type        | p:last-of-type        | Selects every <p> element that is the last <p> element of its parent                                 |
  | :link                | a:link                | Selects all unvisited links                                                                          |
  | :not(selector)       | :not(p)               | Selects every element that is not a <p> element                                                      |
  | :nth-child(n)        | p:nth-child(2)        | Selects every <p> element that is the second child of its parent                                     |
  | :nth-last-child(n)   | p:nth-last-child(2)   | Selects every <p> element that is the second child of its parent, counting from the last child       |
  | :nth-last-of-type(n) | p:nth-last-of-type(2) | Selects every <p> element that is the second <p> element of its parent, counting from the last child |
  | :nth-of-type(n)      | p:nth-of-type(2)      | Selects every <p> element that is the second <p> element of its parent                               |
  | :only-of-type        | p:only-of-type        | Selects every <p> element that is the only <p> element of its parent                                 |
  | :only-child          | p:only-child          | Selects every <p> element that is the only child of its parent                                       |
  - What is CSS specificity
    ```html
    <div id="box" class="box">
      <p id="text">My cool box!</p>
    </div>
    ```
    ```css
    .box {
      background-color: red;
    }

    /* Selecting id will always out specify class so the box will be blue */
    #box {
      background-color: blue;
    }

    p {
      color: yellow;
    }

    /* Multiple selectors are always more specific than a single selector */
    div p {
      color: orange;
    }

    #text {
      color: green;
    }

    /* id's will still outspecify ANY amount of selectors */
    /* unless they include id themselves */
    /* So the text is green! */
    ```
