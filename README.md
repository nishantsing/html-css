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

```css
box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
/* box-shadow: offset-x offset-y blur-radius color; */
/* Multiple Shadows */
box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2), 0 6x 8px rgba(0, 0, 0, 0.2);

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

