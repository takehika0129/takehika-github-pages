---
title: "Build a Basic HTML/CSS/JavaScript Single-Page Website (2025/02/12)"
description: ""
---

#### [Visit (https://github.com/takehika0129/no4-single-page-website)](https://github.com/takehika0129/no4-single-page-website)

# **Concept**
This is a simple website that features dynamic background color changes and a quote generator. By combining HTML, CSS, and JavaScript, I built a lightweight and engaging user experience with minimal but effective interactivity.

# **Features**
- 🎨 **Background Color Change**: A button allows users to change the background color randomly from a predefined set of colors.
- 📝 **Quote Generator**: Another button displays a motivational quote from a predefined list, cycling through each time it’s clicked.
- ✨ **Smooth Transitions**: I implemented a fade-in effect for the quotes to create a better user experience.

# **Challenges & Solutions**  
- **Preventing Repeated Background Colors**: Initially, the random color selection often resulted in the same color appearing consecutively. To fix this, I modified the JavaScript function to ensure the new color is different from the previous one.

Solution:
```sh
let lastColor = null;
function getRandomColor() {
    let randomColor;
    do {
        randomColor = colors[Math.floor(Math.random() * colors.length)];
    } while (randomColor === lastColor);
    lastColor = randomColor;
    return randomColor;
}
```

# **Future Improvements**
- **Expand the Quote Collection**: Right now, the quotes are hardcoded. I could integrate an API to fetch new quotes dynamically.
- **More Interactive Elements**: Incorporate animations or additional UI elements to enhance engagement.

---
[Back to All Prototypes](../index.md)
