# What is `dialog` in HTML and JS?

## Explaination

The `dialog` element is used similar as a `div` but with a specific purpose. <mark>Popping up on the user's screen and closing.</mark> The reason people prefers this is because it is much easier to use and requires less code than alternative options. Then some people would probably ask...

#### What's the difference between a normal popup `div` and a `dialog` then?

From my experience, both are similar but very different. `div` popups requires you to setup style tags for it to have the popup's essentials. A shadow when display and the popup centering on screen. The `dialog` element in the other hand, acts as a `div` but also has the essentials of a popup modal in the meantime. You are not required to style the `div` to have a shadow when popup or center on the screen.

<br>

## How to use it
##### HTML
In HTML you simply use `dialog` like a `div`. Typing it like this; `<dialog>`, `</dialog>`. Don't forget to add an open button and close button for the `dialog` to open and close!
```html
    <button id='open'>open</button>

    <dialog>
        <h1>This is a dialog!</h1>
        <button id='close'>close</button>
        <p>Put some content here</p>
    </dialog>
```

##### JavaScript
In JS we should be making the buttons to work, so that the `dialog` element opens and closes. Just like the below.
```js
open.addEventListener('click', function () {
    /*
        Apperently there are alternatives to do the same thing; opening the dialog.
        Here are the recommended to use:
            .show()
            .showModal()
    */
    dialogModal.showModal();
});

close.addEventListener('click', function () {
    dialogModal.close();
});
```

<br>

## Browser compatability
The `dialog` element is surprisingly compatible with all browsers except Interent Explorer. Both `.showModal` and `.close` code are compatible with the same browsers mentioned right before. 

Here's a visual example I found from MDN web docs.

![Table of compatibility](Screenshot%202022-05-16%20152000.png)

<br>

## References 
- [MDN web docs dialog](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog)
- [MDN web docs dialog.close()](https://developer.mozilla.org/en-US/docs/Web/API/HTMLDialogElement/close)
- [MDN web docs dialog.show()](https://developer.mozilla.org/en-US/docs/Web/API/HTMLDialogElement/show)
- [MDN web docs dialog.showModal()](https://developer.mozilla.org/en-US/docs/Web/API/HTMLDialogElement/showModal)
