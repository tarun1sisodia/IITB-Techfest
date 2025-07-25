# NeuroGrove Landing Page

Welcome to the **NeuroGrove** landing page project! This README explains the structure, features, and technologies used in the HTML and CSS for this visually rich, interactive website.

---

## 🌱 Project Overview

NeuroGrove is a conceptual landing page for an AI-powered plant communication platform. The site is designed to be visually engaging, modern, and interactive, using only HTML and CSS (no JavaScript required for the main effects).

---

## 📁 File Structure

- `index.html` — The main HTML file containing the page structure and content.
- `styles.css` — The main stylesheet with all custom styles and animations.
- `animations.css` — (Optional) Contains reusable animation keyframes and classes.

---

## 🏗️ HTML Structure

### Key Sections

- **Particle System & Color Orbs:** Decorative animated backgrounds for a futuristic, organic feel.
- **Navigation Bar:** Fixed at the top, includes logo, navigation links, and a theme toggle button.
- **Hero Section:** 
  - Animated title with glitch, bounce, and gradient effects.
  - Subtitle with animated underline.
  - Neural background and floating neural nodes for a tech-inspired look.
- **Value Proposition:** 
  - Animated section title with typewriter effect.
  - Main description with word-by-word animated underline (CSS-only, no JS).
  - Stats grid showing platform impact.
  - Features grid with interactive cards.
- **Call to Action:** Buttons for joining the waitlist or watching a demo.
- **Social Proof:** Testimonial from a researcher.
- **SVG Neural Connections:** Animated SVG paths for a neural network vibe.

---

## 🎨 CSS Features & Techniques

### 1. **Custom Properties (CSS Variables)**
- Used for colors and easy theming:
  ```css
  :root {
      --primary-color: #00ff88;
      --secondary-color: #1a365d;
      --accent-color: #0a4d4a;
      --background-color: #051f1e;
      --text-color: #ffffff;
  }
  ```

### 2. **Particle & Orb Animations**
- `.particle-system` and `.color-orbs` use keyframe animations for floating, glowing effects.
- Each particle/orb has its own delay and duration for a natural, organic look.

### 3. **Navigation Bar**
- Fixed, semi-transparent with blur and animated logo.
- Navigation links have animated underlines on hover.

### 4. **Hero Title & Subtitle**
- `.hero-title` uses glitch and bounce keyframes for a techy, attention-grabbing effect.
- `.subtitle-underline` uses a glowing animated gradient.

### 5. **Neural Background & Nodes**
- `.neural-background` uses layered radial gradients and a pulsing animation.
- `.neural-node` elements float gently using keyframes.

### 6. **Typewriter Effect**
- `.typing-text` animates the section title as if being typed out, with a blinking cursor.

### 7. **Animated Word-by-Word Underline**
- Each word in the main description is wrapped in `<span class="highlight-word">`.
- CSS uses `::before` pseudo-elements and `@keyframes word-highlight` to animate an underline for each word, one after another, using `nth-child` selectors for staggered delays.
    ```css
    .highlight-word::before {
        content: '';
        position: absolute;
        left: 0;
        bottom: 0;
        width: 100%;
        height: 2px;
        background: #00ff88;
        opacity: 0.8;
        z-index: 1;
        transform: scaleX(0);
        transform-origin: left;
        border-radius: 1px;
        animation: word-underline 0.4s cubic-bezier(.77,0,.18,1) forwards;
    }
    @keyframes word-underline {
        to { transform: scaleX(1); }
    }
    /* Each word gets a unique delay: */
    .highlight-word:nth-child(1)::before  { animation-delay: 1.2s; }
    .highlight-word:nth-child(2)::before  { animation-delay: 1.6s; }
    /* ...and so on */
    ```

### 8. **Features Grid & Cards**
- Responsive grid layout.
- Feature cards have hover shimmer and glow effects.

### 9. **Buttons & CTA**
- Primary and secondary buttons with gradients, glows, and ripple effects on interaction.

### 10. **Responsive Design**
- Multiple media queries for mobile, tablet, and large screens.
- Font sizes, paddings, and grid layouts adjust for different devices.

### 11. **Accessibility & Reduced Motion**
- Uses `@media (prefers-reduced-motion: reduce)` to minimize animations for users who prefer it.

---

## 🚀 How the Animated Underline Works

- **Each word** in the main description is wrapped in a `<span class="highlight-word">`.
- The underline for each word animates in sequence, creating a "reading guide" effect.
- No JavaScript is used; all delays are handled via CSS `nth-child` selectors.

---

## 🧩 How to Customize

- **Colors:** Change the `:root` variables for instant theme updates.
- **Animation Speed:** Adjust the `animation-delay` and `animation-duration` in the `.highlight-word` CSS.
- **Content:** Edit `index.html` to update text, features, or testimonials.

---

## 💡 Inspiration

This project demonstrates how far you can go with **pure HTML and CSS** for interactive, animated, and modern web design—no JavaScript required for the main effects!

---

**Enjoy