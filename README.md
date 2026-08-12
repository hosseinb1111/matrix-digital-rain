# 🌧️ Matrix Digital Rain

[![GitHub Pages](https://img.shields.io/badge/Hosted%20on-GitHub%20Pages-222222?logo=github)](https://pages.github.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML](https://img.shields.io/badge/HTML-5-E34F26?logo=html5\&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?logo=javascript\&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

A customizable **Matrix-style digital rain animation** built entirely with HTML, CSS, and vanilla JavaScript.

It runs completely in the browser with no frameworks, libraries, backend, API, or build process required.

🔗 **[Try it live](https://hosseinb1111.github.io/matrix-digital-rain/)**

![Matrix Digital Rain](https://raw.githubusercontent.com/hosseinb1111/matrix-digital-rain/main/example.png)

---

## ✨ Features

### 🌧️ Digital Rain

A full-screen animated Matrix-style digital rain effect rendered using the HTML5 Canvas API.

### 🎨 Custom Colors

Choose any color for the falling characters using the built-in color picker.

The default is the classic Matrix green:

```text
#00ff41
```

### ⚡ Adjustable Speed

Change how quickly the digital rain moves.

The speed can be adjusted from very slow to extremely fast.

### 🌊 Adjustable Trail

Control how long the characters remain visible on screen.

A low value produces longer trails, while a higher value creates a faster fade.

### 📊 Adjustable Density

Control how many columns of characters appear across the screen.

### 🔤 Adjustable Font Size

Change the size of the falling characters from small, dense streams to larger, more dramatic characters.

### ✨ Glow Effect

Adjust the amount of glow around the characters.

The glow is rendered using the Canvas shadow system.

### 🧬 Multiple Character Sets

Choose between several character modes:

* Latin + numbers
* Katakana + Latin
* Binary
* Symbols
* Everything

### 🌌 Multiple Background Styles

The background can be changed between:

* Classic Black
* Cyber Grid
* Radial Glow
* Deep Space
* Terminal

### 🎲 Randomize

The **Randomize** button generates an entirely new visual configuration.

It can randomly change:

* Color
* Speed
* Density
* Font size
* Trail
* Glow
* Background
* Character set

### ⏸️ Pause / Resume

Pause the animation whenever you want and resume it later.

### ⛶ Fullscreen

Switch to browser fullscreen mode for a cleaner visual experience.

### 📱 Responsive

The project works on:

* Desktop
* Laptop
* Tablet
* Mobile

The control panel automatically adapts to smaller screens.

### ⌨️ Keyboard Shortcuts

You can control the application without touching the buttons.

| Key     | Action                |
| ------- | --------------------- |
| `Space` | Pause / Resume        |
| `C`     | Open / Close controls |
| `R`     | Randomize             |
| `Esc`   | Close controls        |

---

## 🛠️ Technologies

This project intentionally uses only browser-native technologies.

| Technology   | Purpose                      |
| ------------ | ---------------------------- |
| HTML5        | Page structure               |
| CSS3         | Interface and visual effects |
| JavaScript   | Animation and controls       |
| Canvas API   | Matrix rain rendering        |
| GitHub Pages | Hosting                      |

There are **zero external dependencies**.

No:

* React
* Vue
* Angular
* Node.js
* npm packages
* CDN libraries
* Backend
* Database
* API

are required.

---

## 📁 Project Structure

```text
matrix-digital-rain/
│
├── index.html
├── example.png
├── README.md
└── LICENSE
```

### `index.html`

Contains the complete application:

* HTML structure
* CSS
* Canvas animation
* Controls
* Visual effects
* JavaScript logic

### `example.png`

Screenshot used in this README.

### `README.md`

Project documentation.

### `LICENSE`

MIT License for the project.

---

## 🚀 Run Locally

Because this is a static website, you don't need to install anything.

Simply download or clone the repository:

```bash
git clone https://github.com/hosseinb1111/matrix-digital-rain.git
```

Then enter the directory:

```bash
cd matrix-digital-rain
```

You can open `index.html` directly in your browser.

That's it.

For local development, you can also use a simple development server such as VS Code's Live Server extension.

---

## 🌐 GitHub Pages Deployment

This project is designed specifically for GitHub Pages.

### 1. Create a repository

Create a repository on GitHub.

For example:

```text
matrix-digital-rain
```

### 2. Upload the files

Your repository should contain:

```text
index.html
README.md
LICENSE
example.png
```

### 3. Enable GitHub Pages

Open your repository and go to:

**Settings → Pages**

Under **Build and deployment**:

```text
Source: Deploy from a branch
Branch: main
Folder: / (root)
```

Click **Save**.

GitHub will build and host the site automatically.

Your website will then be available at:

```text
https://YOUR_USERNAME.github.io/YOUR_REPOSITORY/
```

For this repository:

```text
https://hosseinb1111.github.io/matrix-digital-rain/
```

---

## 🎛️ Customization

The project is intentionally easy to modify.

Everything is contained inside `index.html`.

### Change the Default Color

Find:

```javascript
color: "#00ff41",
```

and replace it with another color.

For example:

```javascript
color: "#00e5ff",
```

### Change the Default Speed

Find:

```javascript
speed: 1,
```

and change the value.

For example:

```javascript
speed: 2,
```

### Change the Default Font Size

Find:

```javascript
fontSize: 16,
```

and change it:

```javascript
fontSize: 20,
```

### Add Characters

Character sets are stored in:

```javascript
const characterSets = {
```

You can create your own.

For example:

```javascript
custom:
  "ABCDEFGHIJKLMNOPQRSTUVWXYZ" +
  "0123456789" +
  "@#$%&"
```

Then add an option to the character selector in the HTML:

```html
<option value="custom">Custom</option>
```

### Add Another Background

The background styles are handled inside:

```javascript
function updateBackground()
```

You can add your own visual style there.

---

## 🎨 How the Matrix Effect Works

The animation uses the browser's **Canvas API**.

The screen is divided into columns.

Each column has a value representing the vertical position of its falling characters.

Conceptually:

```text
Column 1    Column 2    Column 3    Column 4
   ↓           ↓           ↓           ↓
   A           7           X           0
   F           1           4           B
   9           K           8           2
```

Every animation cycle:

1. The previous frame is partially covered with a transparent black layer.
2. A random character is selected.
3. The character is drawn at the current position.
4. The column moves downward.
5. Occasionally, a character becomes bright white.
6. When the stream leaves the screen, it is randomly reset.

The transparent black layer is what creates the characteristic fading trail.

---

## ✨ Visual Effects

The project doesn't rely only on the falling characters.

Additional layers create the overall atmosphere:

### Scanlines

A repeating CSS gradient creates subtle horizontal scanlines.

### Vignette

A radial gradient darkens the edges of the screen.

### Atmospheric Glow

Multiple radial gradients create soft colored light behind the rain.

### Character Glow

Canvas shadow rendering creates the glowing effect around brighter characters.

### Cyber Grid

The optional grid background draws faint vertical and horizontal lines behind the animation.

---

## 📱 Mobile Support

The control interface automatically adapts to smaller screens.

On mobile devices:

* The title becomes smaller.
* The settings panel uses the available width.
* Controls remain scrollable.
* The animation continues to use the full viewport.

---

## ♿ Accessibility

The project includes a few accessibility improvements:

* Accessible labels for interactive controls
* Keyboard navigation
* `aria-expanded` state for the settings button
* Visible focus indicators
* Support for `prefers-reduced-motion`

The animation still remains primarily a visual experiment, so users who rely heavily on reduced motion may still prefer to pause the effect.

---

## 🔒 Privacy

This project does not collect or transmit personal data.

There is:

* No backend
* No analytics
* No database
* No account system
* No cookies
* No external API requests

Everything runs locally in the user's browser.

---

## ⚡ Performance

The project is designed to remain lightweight.

The animation uses:

```javascript
requestAnimationFrame()
```

for rendering and the HTML5 Canvas API for drawing.

The device pixel ratio is also capped to help prevent unnecessarily large canvas buffers on high-resolution displays.

No external JavaScript libraries are loaded.

---

## 🤝 Contributing

Contributions are welcome.

You can contribute by:

* Adding new character sets
* Creating new background styles
* Improving the animation
* Improving mobile support
* Improving accessibility
* Adding new controls
* Optimizing performance
* Fixing bugs
* Improving the interface

To contribute:

```bash
git clone https://github.com/hosseinb1111/matrix-digital-rain.git

cd matrix-digital-rain

git checkout -b feature/my-feature
```

Make your changes:

```bash
git add .
git commit -m "Add my new feature"
```

Push your branch:

```bash
git push origin feature/my-feature
```

Then open a Pull Request on GitHub.

---

## 📄 License

This project is licensed under the **MIT License**.

You are free to:

* Use the project
* Modify the project
* Distribute the project
* Use it commercially
* Include it in other projects

See the [LICENSE](LICENSE) file for the complete license text.

---

## ⭐ Support

If you like the project, consider giving the repository a ⭐ on GitHub.

Issues, suggestions, and pull requests are welcome.

---

Made with ☕, JavaScript, and an unreasonable amount of green text. 🟢
