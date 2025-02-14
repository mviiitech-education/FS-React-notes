# Major types of event handling

Here's an example of a React component that demonstrates handling the most common types of events, such as clicks, form submissions, changes, keyboard inputs, and mouse events.

## Explanation of the Events Handled

1. **Input Change Event (`onChange`)**:

   - The input field captures the value entered by the user and updates the `inputValue` state.

2. **Form Submit Event (`onSubmit`)**:

   - When the form is submitted, it prevents the default behavior (page refresh) and shows an alert with the current input value.

3. **Button Click Event (`onClick`)**:

   - The button handles a click event and toggles the `isClicked` state, changing the button text and triggering an alert.

4. **Keyboard Key Press Event (`onKeyDown`)**:

   - Captures the key pressed in the input field and displays the key in real time.

5. **Mouse Move Event (`onMouseMove`)**:
   - Tracks the mouse position and updates the coordinates on the screen as you move the mouse within the `div`.

### How to Use

- The input field will show the key pressed and update as you type.
- The form will submit and display the input value in an alert.
- The button will change its text on click and show an alert.
- The mouse position will update dynamically as you move the mouse within the container.
