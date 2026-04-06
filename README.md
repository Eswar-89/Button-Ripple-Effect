# 🎯 Button Ripple Effect

A simple and elegant button hover effect using **HTML, CSS, and JavaScript**.
When you hover over the button, a ripple animation expands from the cursor position, creating a smooth interactive experience.

---

## 🚀 Demo

Hover over the button to see the ripple effect in action.

---

## 📁 Project Structure

```
button-ripple-effect/
│── index.html
│── style.css
│── index.js
└── README.md
```

---

## 🛠️ Technologies Used

* HTML5
* CSS3 (with custom properties & transitions)
* Vanilla JavaScript

---

## ✨ Features

* 🎨 Smooth ripple animation
* 📍 Ripple originates from cursor position
* ⚡ Lightweight (no libraries required)
* 📱 Responsive and works across devices

---

## 📄 Code Explanation

### 🔹 HTML

Creates a simple button using an anchor tag:

```html
<a href="#" class="btn"><span>Button</span></a>
```

---

### 🔹 CSS

* Uses `::before` pseudo-element to create the ripple
* Custom properties (`--xPos`, `--yPos`) control ripple origin
* `overflow: hidden` ensures ripple stays inside the button

```css
.btn::before {
  position: absolute;
  width: 0;
  height: 0;
  border-radius: 50%;
  transition: width 0.5s, height 0.5s;
}
```

---

### 🔹 JavaScript

Captures mouse position and updates CSS variables dynamically:

```javascript
btnEl.addEventListener("mouseover", (event) => {
  const x = event.pageX - btnEl.offsetLeft;
  const y = event.pageY - btnEl.offsetTop;

  btnEl.style.setProperty("--xPos", x + "px");
  btnEl.style.setProperty("--yPos", y + "px");
});
```

---

## ▶️ How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/Eswar-89/Button-Ripple-Effect.git
   ```

2. Open `index.html` in your browser.

---

## 💡 Customization

* Change ripple color:

  ```css
  background-color: orangered;
  ```
* Adjust animation speed:

  ```css
  transition: width 0.5s, height 0.5s;
  ```
* Modify button size, color, or shadow as needed.

---

## 📸 Preview

You can enhance this project by adding:

* Click-based ripple instead of hover
* Multiple buttons with different styles
* Sound or haptic feedback

---

## 🤝 Contributing

Feel free to fork this repo and improve the effect!

---

## 🙌 Acknowledgement

Inspired by modern UI interactions and material design ripple effects.
