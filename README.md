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

#### Flexbox
- [Flexbox Froggy](https://flexboxfroggy.com/)


#### Grid
- [Grid Garden](https://cssgridgarden.com/)
