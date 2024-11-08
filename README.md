# Live Code Editor

This project is a **simple live code editor** built with HTML, CSS, and JavaScript. It allows users to enter HTML, CSS, and JavaScript code in separate text areas on the left side of the screen and displays the rendered output in real time on the right side.

## Features

- **Real-Time Output**: As you type HTML, CSS, or JavaScript code, the output updates instantly.
- **Separate Code Sections**: The editor has dedicated areas for HTML, CSS, and JavaScript, making it easy to focus on each part independently.
- **Interactive Preview**: You can see changes reflected immediately, allowing for a fast feedback loop while testing and experimenting with code.

## File Structure

The entire code is contained in a single HTML file with inline JavaScript and CSS.

### HTML Structure

- **`.leftPart` (Left Section)**: This section contains three labeled text areas for HTML, CSS, and JavaScript code input.
- **`.rightPart` (Right Section)**: Contains an `<iframe>` element that serves as the preview window to display the rendered output.

### CSS Styling

Basic CSS styling is applied to make the layout clean and responsive:
- Uses `flex` layout to split the screen into two equal parts for code input and preview.
- Background colors and padding are applied for visual separation between sections.

### JavaScript Functionality

The JavaScript code handles the real-time updating of the preview in the `<iframe>`:
1. **Element Selection**: Selects the `<iframe>` and all text areas within `.leftPart`.
2. **Event Listener**: Listens for the `keyup` event on each text area.
3. **Updating the Preview**:
   - **HTML Content**: Updates the `body` of the `<iframe>` with the HTML code.
   - **CSS Content**: Injects CSS directly into the `<iframe>` `<head>` using a `<style>` tag.
   - **JavaScript Content**: Executes the JavaScript within the `<iframe>` using `eval()`.

## How It Works

1. **HTML Code Section**: Content typed in this section is rendered directly in the `<iframe>`’s body.
2. **CSS Code Section**: CSS code is injected into the `<iframe>` head within a `<style>` tag.
3. **JavaScript Code Section**: JavaScript is evaluated in the `<iframe>`’s context, allowing it to manipulate the HTML content dynamically.

## Usage

1. Clone or download the project to your local machine.
2. Open the HTML file in any web browser.
3. Enter HTML, CSS, or JavaScript code in the respective sections, and see the live output on the right.

## Potential Improvements

- **Error Handling**: Currently, JavaScript errors are not displayed. Adding error handling would improve the user experience.
- **Auto-refresh Optimization**: To improve performance, you could add a short delay (e.g., 500 ms) before updating the iframe to prevent excessive updates during typing.

## Example Code

Below is a small example to test the editor:

```html
<!-- HTML -->
<div>Hello, World!</div>

<!-- CSS -->
div {
    color: blue;
    font-size: 24px;
}

<!-- JavaScript -->
alert("Hello from JavaScript!");
```

With this live code editor, you can quickly test small snippets of HTML, CSS, and JavaScript, making it a useful tool for learning and experimentation.

