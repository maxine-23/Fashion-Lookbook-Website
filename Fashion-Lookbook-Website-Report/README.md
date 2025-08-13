# Fashion Lookbook Website – Project Report

## 1. Title Page
**Project Title:** Fashion Lookbook Website  
**Submitted By:**  
- **Team Members:** Jyothika Merin Babu, Maxine Danica M, Sanjukta Banik  
- **Roll Number(s):** 2462334, 2462342, 2462361  
- **College Email ID:** jyothika.merin@btech.christuniversity.in, sanjukta.banik@btech.christuniversity.in, maxine.danica@btech.christuniversity.in  
- **Course:** UI/UX Design Fundamentals  
- **Instructor Name:** Dr Nagaveena  
- **Institution:** Christ University  
- **Date of Submission:** 13/08/2025  

## 2. Abstract
This project presents a **Fashion Lookbook website** built using pure HTML5 and CSS3. The goal was to design a visually engaging, responsive front‑end that showcases fashion imagery with interactive hover effects and lightweight pop‑up overlays—implemented without JavaScript. Core technologies include semantic HTML, modern CSS (Flexbox, Grid, transitions), and responsive techniques. The final outcome is a polished, fast‑loading lookbook with a two‑column gallery, diamond‑shaped call‑to‑action links, CSS‑only lightbox overlays, and a cohesive color system. This site is useful for presenting curated fashion collections, portfolio pieces, or brand campaigns while emphasizing accessibility, performance, and maintainability.

## 3. Objectives
- Design a user‑friendly interface following modern UI principles.  
- Develop a fully responsive layout using only HTML and CSS.  
- Implement structured HTML5 semantic elements for clarity and SEO.  
- Apply CSS for branding, layout, animations, and responsive behavior.  
- Ensure accessibility and readability across devices and viewports.

## 4. Scope of the Project
- Focused exclusively on front‑end design (no JavaScript or server‑side code).  
- Designed for desktop, tablet, and mobile viewports.  
- Implemented with open‑source tools and hand‑written code (no external UI libraries).  
- Assets include locally hosted images (WebP/AVIF/JPEG) referenced from the `assets/` folder.  

## 5. Tools & Technologies Used
| Tool / Technology | Purpose |
| --- | --- |
| HTML5 | Markup and content structure |
| CSS3 | Styling, layout, transitions, and effects |
| VS Code | Code editor |
| Chrome / Edge DevTools | Testing and debugging |
| Google Fonts | Web typography (Allura, Bitcount Prop Single) |

## 6. HTML Structure Overview
- Semantic sections used: `<header>`, `<section>`, and `<footer>`  
- Page organized into Header, Shapes (CTAs), Gallery, Popup Overlays, Contact, and Footer  
- Anchor links (`<a href="#popupN">`) drive CSS‑only overlays via `:target`  
- Images include `alt` text for accessibility and fixed height/width attributes for layout stability  
> **Note:** A dedicated `<nav>` and `<main>` can be added as an enhancement for even clearer semantics.

## 7. CSS Styling Strategy
- External stylesheet: `style.css` with modular sections and comments  
- Layout: Flexbox for the shapes bar; CSS Grid for the two‑column gallery  
- Interactivity: Hover transitions, shadow glow, and keyframe zoom for overlays  
- Responsiveness: Fluid grid; images use `object-fit: cover`  
- Typography: Google Fonts imported; consistent font stack fallback  
- Aesthetics: Gradients, rounded corners, soft shadows, and high‑contrast text

## 8. Key Features
| Feature | Description |
| --- | --- |
| Responsive Gallery | Two‑column grid that adapts to screen sizes |
| CSS‑Only Lightbox | `:target` overlays with blur and zoom animation; no JS |
| Interactive Shapes | Diamond‑rotated call‑to‑action links with hover scale |
| Visual Effects | Image hover scale and luminous box‑shadow glow |
| Accessibility | Alt text on images; readable color contrast in header/contact |

## 9. Challenges Faced & Solutions
| Challenge | Solution |
| --- | --- |
| Image overflow on smaller screens | Used `object-fit: cover`; recommended media queries to adjust sizes and grid columns |
| Click‑to‑zoom without JavaScript | Implemented `:target` overlays with `position: fixed`, backdrop blur, and a close link |
| Maintaining layout consistency | Employed Grid for gallery and Flex for shapes to avoid float issues |
| Typography rendering differences | Loaded web fonts with sensible fallbacks (`system-ui`) |

## 10. Outcome
- Delivered a clean, consistent, and visually engaging front‑end  
- All components (header, CTAs, gallery, overlays, contact, footer) function using only HTML and CSS  
- Strengthened understanding of responsive layout, visual hierarchy, and CSS animations  

## 11. Future Enhancements
- Add JavaScript for advanced interactivity (keyboard navigation, overlay carousel)  
- Implement a theme toggler (light/dark) with CSS variables  
- Introduce accessibility refinements (focus traps, ESC‑to‑close overlays)  
- Backend integration for a contact form and basic analytics  

## 12. Sample Code

### 12.1 HTML Code
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fashion Lookbook</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <h1>Welcome to 2025 Fashion Lookbook</h1>
    <p>"Fashion is the art of dressing dreams — a vibrant mix of style, culture, and creativity that speaks without words."</p>
</header>

<section class="shapes-section">
    <a href="#popup1" class="shape diamond">Fashion</a>
    <a href="#popup2" class="shape diamond">Style</a>
    <a href="#popup3" class="shape diamond">Luxury</a>
    <a href="#popup4" class="shape diamond">Trend</a>
    <a href="#popup5" class="shape diamond">Chic</a>
    <a href="#popup6" class="shape diamond">Glam</a>
</section>

<section class="gallery">
    <a href="#popup1"><img id="img1" src="assets/fashion3.jpeg" alt="Gallery Image 1" height="700" width="450"></a>
    <a href="#popup2"><img id="img2" src="assets/fashion6.avif" alt="Gallery Image 2" height="700" width="450"></a>
    <a href="#popup3"><img id="img3" src="assets/fashion1.webp" alt="Gallery Image 3" height="700" width="450"></a>
    <a href="#popup4"><img id="img4" src="assets/fashion4.webp" alt="Gallery Image 4" height="700" width="450"></a>
    <a href="#popup5"><img id="img5" src="assets/fashion5.webp" alt="Gallery Image 5" height="700" width="450"></a>
    <a href="#popup6"><img id="img6" src="assets/fashion2.webp" alt="Gallery Image 6" height="700" width="450"></a>
</section>

<div id="popup1" class="overlay">
    <a class="close" href="#">&times;</a>
    <img src="assets/fashion3.jpeg" alt="Gallery Image 1">
</div>
<div id="popup2" class="overlay">
    <a class="close" href="#">&times;</a>
    <img src="assets/fashion6.avif" alt="Gallery Image 2">
</div>
<div id="popup3" class="overlay">
    <a class="close" href="#">&times;</a>
    <img src="assets/fashion1.webp" alt="Gallery Image 3">
</div>
<div id="popup4" class="overlay">
    <a class="close" href="#">&times;</a>
    <img src="assets/fashion4.webp" alt="Gallery Image 4">
</div>
<div id="popup5" class="overlay">
    <a class="close" href="#">&times;</a>
    <img src="assets/fashion5.webp" alt="Gallery Image 5">
</div>
<div id="popup6" class="overlay">
    <a class="close" href="#">&times;</a>
    <img src="assets/fashion2.webp" alt="Gallery Image 6">
</div>

<section class="contact">
    <h2>Contact Us</h2>
    <p>Email: fashion2025@email.com</p>
    <p>Phone: +91 98765 43210</p>
</section>

<footer class="footer">
    <p>&copy; 2025 Fashion Lookbook. All Rights Reserved.</p>
</footer>

</body>
</html>
```

### 12.2 CSS Code
```css
@import url('https://fonts.googleapis.com/css2?family=Allura&family=Bitcount+Prop+Single:wght@100..900&display=swap');

* {
    margin: 0;
    padding: 0;
    font-family: "Bitcount Prop Single", system-ui;
}

html {
    scroll-behavior: smooth;
}

body {
    text-align: center;
    margin: 0;
    background: linear-gradient(135deg, #ffecd2, #fcb69f);
    background-image: url(assets/news.jpg);
}

header {
    padding: 50px;
    font-size: 25px;
    background: #000000;
    color: white;
    border-bottom: 5px solid #ffffff;
}

.shapes-section {
    display: flex;
    justify-content: center;
    gap: 30px;
    margin: 30px 0;
    font-size: larger;
}

.shape {
    padding: 20px;
    border: 5px solid #000000;
    background-color: grey;
    color: white;
    font-weight: bold;
    text-decoration: none;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: transform 0.3s, background 0.3s;
}

.diamond {
    transform: rotate(45deg);
    width: 80px;
    height: 80px;
}

.diamond span {
    transform: rotate(-45deg);
    display: block;
}

.shape:hover {
    transform: scale(1.1);
    background: #000000;
}

.gallery {
    display: flex;
    justify-content: center;
    gap: 15px;
    padding: 40px;
    flex-wrap: wrap;
}

.gallery img {
    border: 15px solid #000000;
    border-radius: 15px;
    transition: transform 0.4s ease, filter 0.4s ease, box-shadow 0.4s ease;
    object-fit: cover;
}

.gallery img:hover {
    transform: scale(1.15) rotate(2deg);
    filter: brightness(1.2) saturate(1.3);
    box-shadow: 0 10px 20px rgba(0,0,0,0.3);
}

.overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,0.8);
    backdrop-filter: blur(8px);
    display: none;
    justify-content: center;
    align-items: center;
    z-index: 1000;
}

.overlay:target {
    display: flex;
}

.overlay img {
    max-width: 95%;
    max-height: 95%;
    border-radius: 10px;
    animation: zoomIn 0.3s ease;
    box-shadow: 0 0 30px rgba(255,255,255,0.8);
    transition: box-shadow 0.3s ease;
}

.overlay img:hover {
    box-shadow: 0 0 50px rgba(255,255,255,1);
}

.close {
    position: absolute;
    top: 20px;
    right: 30px;
    font-size: 40px;
    color: white;
    text-decoration: none;
}

@keyframes zoomIn {
    from { transform: scale(0.7); opacity: 0; }
    to { transform: scale(1); opacity: 1; }
}

.contact {
    padding: 50px;
    background-color: gray;
    color: white;
    font-size: 25px;
    border-top: 5px solid #ffffff;
    border-bottom: 5px solid #ffffff;
}

.footer {
    padding: 20px;
    background: #000000;
    color: white;
    text-align: center;
}
```

## 13. Conclusion
The **Fashion Lookbook Website** demonstrates how an appealing, interactive experience can be achieved using only HTML and CSS. Building the two‑column gallery, diamond CTAs, and CSS‑only overlays reinforced core front‑end concepts such as layout composition, responsive design, and motion principles. This mini‑project strengthened practical skills in semantic structuring, maintainable styling, and accessibility‑first thinking—valuable for larger UI/UX and web development work.

## 14. References
- L&T LMS: https://learn.lntedutech.com/Landing/MyCours  
- MDN Web Docs – HTML & CSS References  
- Google Fonts – Web Typography Guidelines  
