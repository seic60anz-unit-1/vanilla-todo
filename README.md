# Todo List

### Getting Started

1. Fork this repo and `git clone` it down to your computer
1. Open index.html in your browser
1. When you're finished or when time is up, push your work to your remote repo, and file a Pull Request

---

### Part 1

Write code in `script.js` so that when the done button (check icon) is clicked the todo item is removed.

Your script should only have a **single** click event handler.

<details>
<summary>HINT</summary>

You'll need to combine:
- DOM selection
- event delegation
- `event.target`
- some way to check that the clicked element is the done button
- DOM traversal
- DOM manipulation (removing elements)

</details>

### Part 2

Add code to `script.js` so that when the `.todo-form` is submitted, the text the user typed in the `input` textbox is added to the end of the `.todo-list` as a new todo item. Check `index.html` for how each todo item should be structured.

<details>
<summary>HINT</summary>

- Add a [`submit` event](https://developer.mozilla.org/en-US/docs/Web/API/HTMLFormElement/submit_event) listener on the form (`.todo-form`) element.

In the `submit` event handler:
- [Stop the default behaviour](https://developer.mozilla.org/en-US/docs/Web/API/Event/preventDefault) of form submissions.
- Get the `input` element using DOM traversal (`.children`, etc.) or DOM selection (`.querySelector`, etc.).
- Get what the user typed in the `input` element using the [`.value` property](https://www.w3schools.com/jsref/prop_text_value.asp).
- Create a new todo item with this structure:
    ``` html
    <div class="todo">
      <p>{WHAT_THE_USER_TYPED_IN_THE_INPUT_ELEMENT}</p>
      <button class="done">done</button>
    </div>
    ```

    - You'll need:
        - [`document.createElement`](https://developer.mozilla.org/en-US/docs/Web/API/Document/createElement)
        - [`.className`](https://developer.mozilla.org/en-US/docs/Web/API/Element/className) or [`.classList.add()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList)
        - [`.textContent`](https://www.w3schools.com/jsref/prop_node_textcontent.asp)
        - [`.appendChild`](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild)

- Append your new todo item to the `.todo-list` element with [`.appendChild`](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild).

</details>
