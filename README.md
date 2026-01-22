<think>
First, the user is asking for code for a "Product Showcase Website". This mirrors the previous request for the Festival/Event Landing Page code.

</think>### Overview
Below is a complete, responsive code example for a basic Product Showcase Website. It includes a hero section, product gallery with a simple carousel, testimonials, and a contact form. Built with vanilla HTML, CSS, and JavaScript for simplicity and no external dependencies. The design is mobile-first, with basic interactivity like a product slider and form handling. You can copy-paste this into an HTML file and open it in a browser to test.

Key features implemented:
- Hero banner with CTA.
- Product gallery with a basic image carousel.
- Testimonials section.
- Simple inquiry form (no backend; for demo purposes).
- Responsive layout using CSS Grid and Flexbox.

### HTML Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Product Showcase</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header id="hero">
        <div class="hero-content">
            <h1>Discover Our Premium Gadgets</h1>
            <p>Innovative tech for everyday life.</p>
            <button id="cta-btn">Shop Now</button>
        </div>
    </header>

    <section id="products">
        <h2>Featured Products</h2>
        <div class="carousel">
            <button class="prev" onclick="changeSlide(-1)">&#10094;</button>
            <div class="carousel-container">
                <div class="slide active">
                    <img src="https://via.placeholder.com/400x300?text=Smart+Watch" alt="Smart Watch">
                    <h3>Smart Watch</h3>
                    <p>$199 - Track your fitness and stay connected.</p>
                </div>
                <div class="slide">
                    <img src="https://via.placeholder.com/400x300?text=Wireless+Headphones" alt="Wireless Headphones">
                    <h3>Wireless Headphones</h3>
                    <p>$149 - Immersive sound on the go.</p>
                </div>
                <div class="slide">
                    <img src="https://via.placeholder.com/400x300?text=Portable+Charger" alt="Portable Charger">
                    <h3>Portable Charger</h3>
                    <p>$49 - Never run out of power.</p>
                </div>
            </div>
            <button class="next" onclick="changeSlide(1)">&#10095;</button>
        </div>
    </section>

    <section id="testimonials">
        <h2>What Our Customers Say</h2>
        <div class="testimonial">
            <p>"Amazing quality and fast delivery!"</p>
            <cite>- John Doe</cite>
        </div>
        <div class="testimonial">
            <p>"Best gadgets I've ever owned."</p>
            <cite>- Jane Smith</cite>
        </div>
    </section>

    <section id="contact">
        <h2>Inquire About Products</h2>
        <form id="inquiry-form">
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea placeholder="Your Message" required></textarea>
            <button type="submit">Send Inquiry</button>
        </form>
        <p id="message"></p>
    </section>

    <footer>
        <p>&copy; 2023 Product Showcase. All rights reserved.</p>
        <p>Follow us on <a href="#">Social Media</a></p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
```

### CSS Styles (styles.css)
```css
/* Reset and base styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #333;
    background-color: #f4f4f4;
}

/* Hero section */
#hero {
    background: url('https://via.placeholder.com/1920x600?text=Product+Hero') no-repeat center/cover;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: white;
    position: relative;
}

#hero::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(0, 0, 0, 0.5);
}

.hero-content {
    position: relative;
    z-index: 1;
    max-width: 600px;
}

#hero h1 {
    font-size: 3rem;
    margin-bottom: 1rem;
}

#hero p {
    font-size: 1.2rem;
    margin-bottom: 2rem;
}

#cta-btn {
    background: #4caf50;
    color: white;
    border: none;
    padding: 1rem 2rem;
    font-size: 1.2rem;
    cursor: pointer;
    border-radius: 5px;
    transition: background 0.3s;
}

#cta-btn:hover {
    background: #45a049;
}

/* Products section */
#products {
    padding: 2rem;
    max-width: 1200px;
    margin: 0 auto;
    text-align: center;
}

#products h2 {
    margin-bottom: 2rem;
    font-size: 2rem;
}

.carousel {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
}

.carousel-container {
    width: 400px;
    overflow: hidden;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

.slide {
    display: none;
    text-align: center;
    padding: 1rem;
}

.slide.active {
    display: block;
}

.slide img {
    width: 100%;
    height: auto;
    border-radius: 10px;
}

.prev, .next {
    background: #333;
    color: white;
    border: none;
    padding: 1rem;
    cursor: pointer;
    font-size: 1.5rem;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
}

.prev { left: 0; }
.next { right: 0; }

/* Testimonials section */
#testimonials {
    background: #e0e0e0;
    padding: 2rem;
    text-align: center;
}

#testimonials h2 {
    margin-bottom: 2rem;
    font-size: 2rem;
}

.testimonial {
    margin-bottom: 1rem;
    padding: 1rem;
    background: white;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

/* Contact section */
#contact {
    padding: 2rem;
    max-width: 600px;
    margin: 0 auto;
    text-align: center;
}

#contact h2 {
    margin-bottom: 2rem;
    font-size: 2rem;
}

#inquiry-form {
    display: flex;
    flex-direction: column;
    gap: 1rem;
}

#inquiry-form input, #inquiry-form textarea {
    padding: 0.5rem;
    border: 1px solid #ccc;
    border-radius: 5px;
}

#inquiry-form button {
    background: #4caf50;
    color: white;
    border: none;
    padding: 0.5rem;
    cursor: pointer;
    border-radius: 5px;
}

/* Footer */
footer {
    background: #222;
    color: white;
    text-align: center;
    padding: 1rem;
}

/* Responsive design */
@media (max-width: 768px) {
    #hero h1 {
        font-size: 2rem;
    }
    .carousel-container {
        width: 100%;
        max-width: 300px;
    }
    .prev, .next {
        padding: 0.5rem;
        font-size: 1rem;
    }
}
```

### JavaScript Functionality (script.js)
```javascript
// Carousel functionality
let currentSlide = 0;
const slides = document.querySelectorAll('.slide');

function showSlide(index) {
    slides.forEach((slide, i) => {
        slide.classList.toggle('active', i === index);
    });
}

function changeSlide(direction) {
    currentSlide = (currentSlide + direction + slides.length) % slides.length;
    showSlide(currentSlide);
}

showSlide(currentSlide); // Initial display

// Form submission (demo only)
document.getElementById('inquiry-form').addEventListener('submit', function(e) {
    e.preventDefault();
    const message = document.getElementById('message');
    message.textContent = 'Thank you for your inquiry! We\'ll get back to you soon.';
    message.style.color = '#4caf50';
    this.reset();
});
```

### How to Use and Extend
- **Setup**: Save the HTML as `index.html`, CSS as `styles.css`, and JS as `script.js` in the same folder. Open `index.html` in a browser.
- **Customization**: Replace placeholder image URLs with real product images. Add more slides to the carousel by duplicating `.slide` divs in HTML.
- **Enhancements**: Integrate a backend (e.g., via Node.js or PHP) for form submissions and product data. Add e-commerce features with libraries like Stripe.js. For advanced interactivity, use frameworks like React for dynamic galleries.
- **Testing**: Check responsiveness on mobile devices. Use browser dev tools to inspect elements.
- **Performance**: Minify CSS/JS for production. This code is lightweight and loads quickly.

If you need modifications, such as adding more sections, integrating APIs, or comparing to the event page code, provide details!
