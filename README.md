# Canvas.js

A simple paint application using HTML5 Canvas and JavaScript.

## Features

- **Draw Circles**: Click and drag to create colorful circles.
- **Hit Detection**: Check if a circle is clicked ("Hit") or not ("Miss").
- **Delete Circles**: Double-click on a circle to remove it.
- **Reset Canvas**: Clear the canvas and start fresh.

## Usage

1. Clone this repository:
    ```bash
    git clone https://github.com/your-repo/canvas.js.git
    ```
2. Open the `index.html` file in your browser to start using the app.

## How It Works

- **Drawing**:  
    - Press and hold the mouse button on the canvas to start drawing a circle.
    - Drag the mouse and release to set the circle size.
    - The circle gets a random color on creation.

- **Hit or Miss**:  
    - Single-click anywhere on the canvas:
        - If a circle is clicked, "Hit" is displayed.
        - If no circle is clicked, "Miss" is displayed.

- **Delete Circles**:  
    - Double-click on any circle to delete it from the canvas.

- **Reset**:  
    - Click the "Reset" button to clear all circles and reset the canvas.

## Technologies

- **HTML5 Canvas**
- **CSS3**
- **Vanilla JavaScript**

## Sample Code

```javascript
canvas.addEventListener("mousedown", function(e) {
    const hitIndex = isHit(e.offsetX, e.offsetY);
    if (hitIndex !== -1) {
        statusText.textContent = "Hit";
    } else {
        statusText.textContent = "Miss";
    }
});
