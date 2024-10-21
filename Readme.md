# Mini Calendar

## Overview

The **Mini Calendar** is a lightweight, responsive calendar widget built using HTML, CSS, and JavaScript. It dynamically displays the current date, including the month name, day of the week, day number, and year. This project is designed with simplicity and clarity, making it ideal for embedding on websites or using as a personal widget.

## Features

- Automatically shows the **current month, day, and year**.
- Clean, minimalistic design with modern styling.
- Fully responsive layout that works well on various screen sizes.
- Easy to integrate and customize for different projects.

## Live Demo
You can see the Mini Calendar in action by opening the `index.html` file in any modern browser.

## How It Works

The project uses JavaScript’s `Date` object to fetch the current date and update the DOM elements dynamically. The structure is built with HTML, styled with CSS, and the logic is handled with a few lines of JavaScript.

### Files Overview

1. **index.html**: Contains the structure of the calendar, with placeholders for the month, day, and year.
2. **style.css**: Provides the styling for the calendar, including layout, fonts, colors, and shadows.
3. **script.js**: Contains the logic to dynamically update the displayed date using JavaScript.

## Key Code Snippets

### HTML (index.html)

The core structure of the calendar is simple, with four main placeholders for displaying the current month, day, number, and year.

```html
<div class="calendar-container">
  <p class="month-name" id="month-name"></p>
  <p class="day-name" id="day-name"></p>
  <p class="day-number" id="day-number"></p>
  <p class="year" id="year"></p>
</div>
```

### CSS (style.css)

The styling ensures that the calendar is visually appealing, with a centered design and neat typography. The container is styled with a white background, box shadow, and rounded corners.

```css
.calendar-container {
  background-color: white;
  width: 300px;
  text-align: center;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0 0 0 .3);
  padding: 20px;
}
.month-name {
  background-color: orangered;
  color: white;
  font-size: 30px;
  padding: 10px;
  margin: 0;
}
```

### JavaScript (script.js)

The JavaScript fetches the current date using the `Date` object and updates the HTML elements dynamically. This ensures the calendar always shows the current day, month, and year without manual updates.

```javascript
const monthNameEl = document.getElementById('month-name');
const dayNameEl = document.getElementById('day-name');
const dayNumberEl = document.getElementById('day-number');
const yearEl = document.getElementById('year');

const date = new Date();
monthNameEl.innerText = date.toLocaleString("en", { month: "long" });
dayNameEl.innerText = date.toLocaleString("en", { weekday: "long" });
dayNumberEl.innerText = date.getDate();
yearEl.innerText = date.getFullYear();
```

## How to Use

1. **Clone or download** this repository to your local machine.
2. Open the `index.html` file in a browser to view the Mini Calendar.
3. The calendar will automatically display the current date.

## Customization

- You can easily modify the styles in the `style.css` file to fit your design preferences.
- To change the calendar's language or date format, modify the `toLocaleString()` method in the `script.js` file.
  
## Future Enhancements

Here are a few potential improvements that could be added to the Mini Calendar:
- Add navigation buttons to view previous or next months and years.
- Implement localization for multiple languages and date formats.
- Add support for different themes (dark mode, custom colors).

---

## Conclusion

The **Mini Calendar** is a straightforward yet useful widget that can easily be integrated into any web project. It leverages basic HTML, CSS, and JavaScript to create a dynamic display of the current date in a visually appealing format.

Feel free to modify and expand on this project to suit your specific needs. If you encounter any issues or have suggestions for improvements, don't hesitate to reach out!

---
