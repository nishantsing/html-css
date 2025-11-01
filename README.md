## HTML

#### Accordion
```html
<details name="group1">
    <summary>Title</summary>
    <div>Internal Content</div>
</details> 
```

#### Dialog
```html
<dialog id="myDialog" open>
    <h2>Welcome!</h2>
    <p>This is a dialog box.</p>
    <button id="closeDialog">Close</button>
</dialog>

```

#### Data Attribute Manipulation

```html
<div id="myDiv" data-user-id="123" data-user-name="JohnDoe">

<script>
     // Accessing data attributes
    console.log('Initial User ID:', myDiv.dataset.userId);
    console.log('Initial User Name:', myDiv.dataset.userName);

    // Modifying a data attribute
    myDiv.dataset.userId = '456';
    console.log('Modified User ID:', myDiv.dataset.userId);

    // Adding a new data attribute
    myDiv.dataset.status = 'active';
    console.log('New Status:', myDiv.dataset.status);

    // Removing a data attribute
    delete myDiv.dataset.userName;
    console.log('User Name after removal:', myDiv.dataset.userName); // undefined
</script>  
```


```js
const myDialog = document.getElementById('myDialog');
const openButton = document.getElementById('openDialog'); // Assuming you have an open button
const closeButton = document.getElementById('closeDialog');

openButton.addEventListener('click', () => {
    myDialog.showModal(); // Or myDialog.show() for non-modal
});

closeButton.addEventListener('click', () => {
    myDialog.close();
});

```

## CSS

### css Selectors

- element selector - p
- class selector - .className
- id selector - #id 

### css combinators (Above selectors can be combined)

- direct descendant - p > .className
- all descendant - p .className
- next sibling - .className + .className
- subsequent sibling - .className ~ .className
- attribute selector - p[attribute] | [attribute=""] | 

### css psuedo classes


selector:pseudo-class {
  property: value;
}

- Interactive States
:hover: Applies styles when the user's mouse pointer is over an element.
:active: Applies styles when an element is being activated (e.g., when a mouse button is pressed down on it).
:focus: Applies styles when an element (like an input field or button) receives focus, typically by tabbing or clicking.
:visited: Styles links that the user has already visited.
:link: Styles unvisited links.
- Structural Pseudo-classes (based on element position in the DOM):
:first-child: Selects the first child element of its parent. 
:last-child: Selects the last child element of its parent. 
:nth-child(n): Selects child elements based on their position (e.g., nth-child(even), nth-child(odd), nth-child(3)).
:root: Selects the root element of the document (usually <html>).
:empty: Selects elements that have no children (including text nodes).
- Form-related Pseudo-classes:
:checked: Selects radio buttons or checkboxes that are currently checked.
:enabled: Selects form elements that are enabled.
:disabled: Selects form elements that are disabled.
:required: Selects input fields with the required attribute.
:optional: Selects input fields without the required attribute.
:valid: Selects form elements whose content validates successfully.
:invalid: Selects form elements whose content does not validate successfully

```css
box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
/* box-shadow: offset-x offset-y blur-radius color; */
/* Multiple Shadows */
box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2), 0 6x 8px rgba(0, 0, 0, 0.2);

```

### Position 

```css
#anchor {
  anchor-name: --a1;
}

#label {
  position: absolute;
  position-anchor: --a1;
  position-area: bottom right;
}


```

### Codepip
- [Codepip](https://codepip.com/games/flexbox-froggy/)

#### Flexbox
- [Flexbox Froggy](https://flexboxfroggy.com/)

- Properties on container
    - display:flex
    - flex-direction: row | row-reverse | column | column-reverse
    - justify-content: | start | end | center | space-between | space-around -> horizontal(row) | vertical(column)
    - align-items -> vertical(row)
    - align-content -> gap between each line
    - flex-wrap: nowrap | wrap | wrap-reverse
    - flex-flow: column wrap -> combines flex-direction and flex-wrap

- properties on individual child element
    - order: 0 (negative comes before 0 and positive comes after)
    - align-self -> how items are aligned

#### Grid
- [Grid Garden](https://cssgridgarden.com/)

- properites on container
    - display: grid;
    - grid-template-colums: | 1fr | 0 | repeat(4, 1fr) | % | px
    - grid-template-rows:
    - grid-template -> shorthand for above 2 properties

- properties on individual child elements
    - grid-row-start
    - grid-row-end
    - grid-row -> shorthand for above 2
    - grid-column-start
    - grid-column-end
    - grid-column -> shorthand for above 2
    - grid-area -> shorthand for grid-row and grid-column

