# OIBSIP – Task 1: Landing Page

This project is created as part of my **Oasis Infobyte Web Development Internship**.  
**Task 1** was to **create a landing page** using **HTML** and **CSS**.  

For this task, I chose to design a fashion-themed website named **“Fashiva”**, representing a modern, elegant fashion brand.

---

##  Project Idea

The **Fashiva Landing Page** is a simple yet visually pleasing webpage designed to showcase a fashion brand.  
It features multiple sections arranged in a single scrolling layout. Each section has been styled with a soft pastel theme and balanced spacing to maintain elegance.

The landing page includes:
- A **fixed navigation bar** for quick access to each section.  
- A **hero section** with a background image, welcoming text, and a call-to-action button.  
- A **collection section** displaying sample fashion items in a grid layout.  
- An **about section** describing the brand’s purpose and style.  
- A **footer** with copyright details and a smooth closing look.



---

##  Step-by-Step Building Process

###  1. File Setup
- I first created a new project folder named `OIBSIP_WebDevelopment_Task1`.
- Inside the folder, I created two main files:
  - `index.html` → for the structure and content of the webpage  
  - `style.css` → for the design and styling  

Then I linked the CSS file inside the `<head>` tag of `index.html` using:
```html
<link rel="stylesheet" href="style.css">
```
---

###  2. HTML Structure (index.html)

I began by building the overall structure using semantic HTML tags:

- > header → Contains the logo and navigation bar. 
  It is placed at the top and styled to stay fixed while scrolling.
```
<header>
    <h1>Fashiva</h1>
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#collection">Collection</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
</header>
```
- > section id="home" → Acts as the hero section with a headline and background image. 
  It displays a welcome message, a tagline and a call-to-action button.
```
<section id="home">
    <div class="hero">
        <h2>Welcome to Fashiva</h2>
        <p>Where elegance meets comfort.</p>
        <a href="#collection" class="btn">Explore Collection</a>
    </div>
</section>
```
- > section id="collection" → Showcases the fashion images in a simple grid layout.
    It uses <img> tags to showcase product pictures.

```
<section id="collection">
    <h2>Our Latest Collection</h2>
    <div class="gallery">
        <img src="image1.jpg" alt="Outfit 1">
        <img src="image2.jpg" alt="Outfit 2">
        <img src="image3.jpg" alt="Outfit 3">
    </div>
</section>
```
- > section id="about" → Provides a short description about the brand.
  It is a simple text written in a paragraph tag.
```
<section id="about">
    <h2>About Us</h2>
    <p>Fashiva is a modern fashion platform offering elegant and affordable designs for everyone. Our aim is to blend simplicity with style.</p>
</section>
```
- footer → Displayed at the bottom of the page to add closing text and copyright.
```
<footer>
    <p>&copy; 2025 Fashiva. All rights reserved.</p>
</footer>

```

---

### 3. CSS Styling (style.css)

After the html structure, I focused on styling to make it elegant and clean.

- Firstly, I used a universal selector to ensure uniform alignment and layout across all elements. The box-sizing: border-box makes width or height include padding and borders.
```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}
```
- The body selector is used to define the background colour, text colour, and line spacing.
```
body {
  background-color: #fffafc;
  color: #333;
  line-height: 1.6;
}
```
- For header,

→ Used position: fixed so it stays at the top while scrolling.
>→ display: flex aligns logo and navigation horizontally.
→ justify-content: space-between separates logo and nav evenly.
>→ Added padding and shadow for spacing and depth.
```
header {
  position: fixed;
  top: 0;
  width: 100%;
  background: rgb(255, 200, 220);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 50px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
  z-index: 10;
}
```
- The logo selector is used here to style the website name or logo with larger, bolder white text.
```
.logo {
  font-size: 24px;
  font-weight: 600;
  color: #fff;
}
```
 →nav ul is used to remove link underlines 
 > →nav a is used to make the links white and bold
 →nav a:hover slightly changes the colour for interactivity 
```
nav ul {
  list-style: none;
  display: flex;
  gap: 20px;
}

nav a {
  text-decoration: none;
  color: white;
  font-weight: 500;
}

nav a:hover {
  color: #ffe8f2;
}
```
- The hero section sets full viewport height(100vh) with a background image. It centers content using display: flex both vertically and horizontally and adds padding and white text.
```
.hero {
  height: 100vh;
  background: url('https://thumbs.dreamstime.com/b/stylish-array-colorful-dresses-hangers-chic-boutique-display-concept-fashionable-attire-trendy-clothing-shopping-389715022.jpg') center/cover no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white;
  padding: 0 20px;
}
```
- .hero-content h2 & .hero_content p controls the heading and paragraph sizes and spacing for better visual hierarchy.
```
.hero-content h2 {
  font-size: 48px;
  margin-bottom: 10px;
}

.hero-content p {
  font-size: 18px;
  margin-bottom: 20px;
}
```
- .btn creates a slightly rounded button with background colour, padding, and no underline whereas .btn:hover changes colour slightly for a clickable feel.
```
.btn {
  background: rgb(255, 170, 190);
  color: white;
  padding: 10px 20px;
  border-radius: 25px;
  text-decoration: none;
  font-weight: 500;
}

.btn:hover {
  background: rgb(255, 150, 180);
}
```
- The collection sections changes colours to match the theme and adds margin below for spacing.
```
.collection {
  padding: 80px 20px;
  text-align: center;
  background: #fff;
}

.collection h2 {
  color: rgb(255, 130, 160);
  margin-bottom: 30px;
}
```
- The gallery uses flex-wrap to make images wrao on smaller screens. It centres items and spaces them evenly.
```
.gallery {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}
```
- The .gallery .item makes each image box flexible (flex: 1 1 250px) with a size limit (max-width: 300px).
```
.gallery .item {
  flex: 1 1 250px;
  max-width: 300px;
}
```
- The .gallery img makes images responsive (width:100%) and rounds corners and adds subtle shadow for depth.
```
.gallery img {
  width: 100%;
  border-radius: 10px;
  box-shadow: 0 3px 6px rgba(0,0,0,0.1);
}
```
- .about adds padding, soft background colour, and centers content.
```
.about {
  padding: 80px 20px;
  background: rgb(255, 240, 245);
  text-align: center;
}
```
- .about h2 heading has themed colour and spacing whereas by using .about p paragraph text is centered and limited in width for neat alignment.
```
.about h2 {
  color: rgb(255, 100, 140);
  margin-bottom: 20px;
  font-size: 28px;
}

.about p {
  max-width: 700px;
  margin: 0 auto;
  font-size: 17px;
}
```
- Contact section centers all the text and adds spacing around the section.
```
.contact {
  padding: 80px 20px;
  text-align: center;
  background: #fff;
}

.contact h2 {
  color: rgb(255, 130, 160);
  margin-bottom: 15px;
}
```
- Footer section is displayed at the bottom of the page. It gives a pink background and white text and centers it and slightly reduces font size for a clean footer.
```
footer {
  text-align: center;
  background: rgb(255, 200, 220);
  color: white;
  padding: 15px;
  font-size: 14px;
}
```

---

### How to Run

1. Open the folder in Visual Studio Code.


2. Ensure both files (index.html and style.css) are in the same directory.


3. Open index.html in a browser or use Live Server to preview the webpage.

---

### Author

Syeda Rida Faseeh

> Oasis Infobyte Internship – Task 1: Landing Page
Built using HTML and CSS.