# 📂 Expanding Cards Project

A simple and interactive web project built using HTML, CSS, and vanilla JavaScript that demonstrates a fluid layout where clicking on an image expands it while collapsing the others. This project is excellent for learning **CSS Flexbox**, **CSS Transitions**, and **DOM manipulation** with JavaScript.

---

## ✨ Features

- **Responsive Design:** The layout adjusts for smaller screens (e.g., mobile devices) by hiding some panels to maintain usability.
- **Smooth Transitions:** Uses the `transition` CSS property to create a smooth, appealing animation when cards expand and collapse.
- **Flexbox Layout:** Utilizes CSS Flexbox for easy and dynamic arrangement of the cards.
- **Vanilla JavaScript:** The interactivity is handled purely with basic JavaScript, making it simple to understand.

---

## 🛠️ Technologies Used

- **HTML5:** For the structure and content.
- **CSS3:** For styling, layout (Flexbox), and transitions.
- **JavaScript (ES6):** For handling the click events and adding/removing the active state.

---

## 🚀 Getting Started

Follow these steps to get a copy of the project running on your local machine.

### 1. Cloning the Repository

If you were using Git, you would clone the repository. For now, simply create a new folder on your computer and save the three files inside it:

- `index.html`
- `style.css`
- `script.js`

### 2. Running the Project

1.  Locate the `index.html` file in your project folder.
2.  **Double-click** on `index.html`.

This will open the project in your default web browser, and you can immediately start clicking on the cards to see them expand!

---

## 🧭 Project Structure Explained (For Beginners)

Here's a quick breakdown of what each file does:

### `index.html` (The Structure)

- It defines the **container** (`<div class="container">`) that holds all the cards.
- Each **card** is a `div` with the class `panel`.
- The first card has an extra class, **`active`**, to make it expanded by default.
- Crucially, it **links** the `style.css` file in the `<head>` and the `script.js` file just before the closing `</body>` tag.

### `style.css` (The Looks and Animation)

- **Body:** Sets up a full-page Flexbox container to center the cards.
- **.container:** Uses `display: flex` to make the cards arrange horizontally.
- **.panel:**
  - Sets the initial size (`flex: 0.5`) and style (background, rounded corners).
  - The `transition: flex 0.7s ease-in-out;` line is what creates the smooth animation when the **`flex`** property changes.
- **.panel.active:** When this class is present, the card is instructed to expand using `flex: 5;`, taking up a larger portion of the container space.
- **`@media` Query:** Hides panels 4 and 5 on small screens to prevent overlap.

### `script.js` (The Brains)

- It finds all elements with the class `panel` and stores them in a variable called `panels`.
- It uses a **loop** (`forEach`) to attach a **click listener** to every single card.
- When a card is clicked:
  1.  It calls the function `removeActiveClasses()` to ensure all cards are collapsed.
  2.  It then adds the class **`active`** to the _one_ card that was just clicked, making it expand according to the CSS rules.

---

## 💡 How to Customize

- **Change Images:** Edit the `style` attribute inside each `<div class="panel">` in `index.html` to change the `background-image: url('...');`.
- **Change Text:** Update the text within the `<h3>` tags in `index.html`.
- **Change Speed:** Adjust the `0.7s` value in the `transition` property within the `.panel` CSS rule in `style.css`. A lower number (e.g., `0.3s`) makes it faster.

---

## 🤝 Contributing

This project is a small, standalone exercise. Feel free to use it as a starting point for your own learning and experimentation!
