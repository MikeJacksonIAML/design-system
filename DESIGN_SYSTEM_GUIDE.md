# Premium Design System Guide

## 🎨 **Design Philosophy**

This design system embodies **"Premium Professional with Subtle Sophistication"** - creating trust-building experiences through:

- **Dark Elegance**: Pure black foundations with glass morphism accents
- **Subtle Interactions**: Smooth, hardware-accelerated animations
- **Typography Hierarchy**: Playfair Display for impact, Lato for clarity
- **Accessibility-First**: Proper contrast, focus states, and reduced motion support

---

## 🚀 **Quick Start**

### 1. Include the CSS
```html
<link rel="stylesheet" href="design-system.css">
```

### 2. Set up your HTML structure
```html
<body class="bg-black font-body text-primary">
  <!-- Your content here -->
</body>
```

### 3. Use the components
```html
<!-- Hero Section -->
<section class="container py-4xl text-center">
  <h1 class="font-display text-hero text-primary">
    Your Hero Headline
  </h1>
  <p class="text-large text-secondary my-xl">
    Supporting description text
  </p>
  <button class="btn btn-primary hover-lift">
    Get Started
  </button>
</section>
```

---

## 🎯 **Core Components**

### **Glass Morphism Cards**
```html
<div class="glass-card glass-card-md hover-lift">
  <h3 class="font-display text-title text-primary">Card Title</h3>
  <p class="font-body text-body text-secondary">Card content goes here...</p>
</div>
```

**Variants:**
- `glass-card-sm` - Small padding
- `glass-card-md` - Medium padding (default)
- `glass-card-lg` - Large padding

### **Buttons**
```html
<!-- Primary Button -->
<button class="btn btn-primary hover-lift">Primary Action</button>

<!-- Glass Button -->
<button class="btn btn-glass hover-lift">Secondary Action</button>

<!-- Sizes -->
<button class="btn btn-primary btn-sm">Small</button>
<button class="btn btn-primary btn-lg">Large</button>
```

### **Typography**
```html
<!-- Display Text (Playfair Display) -->
<h1 class="font-display text-hero text-primary">Hero Headline</h1>
<h2 class="font-display text-display text-primary">Section Title</h2>

<!-- Body Text (Lato) -->
<p class="font-body text-body text-secondary">Body paragraph text</p>
<p class="font-body text-small text-muted">Caption or metadata</p>

<!-- Quotes -->
<blockquote class="font-display text-display italic text-primary text-center">
  "Your inspiring quote here"
</blockquote>
```

### **Carousel System**
```html
<div class="carousel-container">
  <!-- Edge Fades -->
  <div class="carousel-fade-left"></div>
  <div class="carousel-fade-right"></div>
  
  <!-- Track -->
  <div class="carousel-track">
    <div class="carousel-item">
      <div class="glass-card glass-card-md">Item 1</div>
    </div>
    <div class="carousel-item">
      <div class="glass-card glass-card-md">Item 2</div>
    </div>
    <div class="carousel-item">
      <div class="glass-card glass-card-md">Item 3</div>
    </div>
  </div>
  
  <!-- Navigation -->
  <div class="carousel-nav">
    <button class="carousel-btn" aria-label="Previous">←</button>
    <button class="carousel-btn" aria-label="Next">→</button>
  </div>
</div>
```

### **Active States & Highlighting**
```html
<!-- Testimonial with Active State -->
<div class="glass-card relative active-card">
  <!-- Corner Brackets (for active items) -->
  <div class="corner-bracket top-left"></div>
  <div class="corner-bracket top-right"></div>
  <div class="corner-bracket bottom-left"></div>
  <div class="corner-bracket bottom-right"></div>
  
  <blockquote class="font-body text-body italic text-primary">
    "This testimonial is highlighted as active"
  </blockquote>
  <footer class="text-small text-muted mt-md">
    <div class="font-medium">Customer Name</div>
    <div>Title, Company</div>
  </footer>
</div>

<!-- Inactive/Dimmed Cards -->
<div class="glass-card inactive-card">
  <p>This card is dimmed/inactive</p>
</div>
```

### **Scroll Animations**
```html
<!-- Elements that fade in on scroll -->
<div class="reveal" style="--delay: 0">
  <h2 class="font-display text-display">Fades in first</h2>
</div>

<div class="reveal reveal-stagger" style="--delay: 1">
  <p class="font-body text-body">Fades in second (100ms delay)</p>
</div>

<div class="reveal reveal-stagger" style="--delay: 2">
  <p class="font-body text-body">Fades in third (200ms delay)</p>
</div>
```

### **Marquee/Scrolling Content**
```html
<div class="marquee-container" style="--marquee-speed: 30s;">
  <div class="marquee-track">
    <!-- First set -->
    <div class="flex gap-xl">
      <img src="logo1.png" alt="Company 1" class="h-12">
      <img src="logo2.png" alt="Company 2" class="h-12">
      <img src="logo3.png" alt="Company 3" class="h-12">
    </div>
    <!-- Duplicate set for seamless loop -->
    <div class="flex gap-xl">
      <img src="logo1.png" alt="Company 1" class="h-12">
      <img src="logo2.png" alt="Company 2" class="h-12">
      <img src="logo3.png" alt="Company 3" class="h-12">
    </div>
  </div>
</div>
```

---

## 🎨 **Color System**

### **Usage Guidelines**

```css
/* Primary Colors */
--primary-blue: #188bf6;     /* CTAs, links, focus states */
--accent-orange: #FF6A00;    /* Active highlights, corner brackets */
--pure-white: #ffffff;       /* Primary text, important content */

/* Backgrounds */
--background-black: #000000; /* Main page background */
--surface-dark: #0f1217;     /* Card backgrounds, sections */

/* Text Hierarchy */
--text-primary: #ffffff;     /* Headlines, important text */
--text-secondary: #e5e7eb;   /* Body text, descriptions */
--text-muted: #9ca3af;       /* Captions, metadata */
--text-subtle: #6b7280;      /* Dividers, subtle elements */
```

### **When to Use Each Color**

- **Primary Blue** (`text-brand`): Hero taglines, CTA buttons, focus states
- **Accent Orange** (`text-accent`): Active states, corner brackets, highlights
- **Pure White** (`text-primary`): Main headlines, quotes, important content
- **Secondary Gray** (`text-secondary`): Body paragraphs, descriptions
- **Muted Gray** (`text-muted`): Captions, metadata, less important info
- **Subtle Gray** (`text-subtle`): Dividers, borders, background elements

---

## 📐 **Layout Patterns**

### **Container System**
```html
<!-- Standard content container -->
<div class="container container-xl">
  <h1>Content within max-width container</h1>
</div>

<!-- Full-width section -->
<section class="w-full bg-dark py-4xl">
  <div class="container container-lg">
    <h2>Full-width section with contained content</h2>
  </div>
</section>
```

### **Spacing Scale**
```html
<!-- Consistent spacing using the 8px grid -->
<div class="py-xl px-lg">        <!-- 32px vertical, 24px horizontal -->
<div class="my-2xl">             <!-- 48px top/bottom margin -->
<div class="p-md">               <!-- 16px padding all sides -->
```

### **Responsive Grid**
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-xl">
  <div class="glass-card glass-card-md">Item 1</div>
  <div class="glass-card glass-card-md">Item 2</div>
  <div class="glass-card glass-card-md">Item 3</div>
</div>
```

---

## ✨ **Animation Guidelines**

### **Hover Effects**
```html
<!-- Lift on hover -->
<div class="glass-card hover-lift">Lifts up on hover</div>

<!-- Scale on hover -->
<div class="glass-card hover-scale">Scales up slightly on hover</div>

<!-- Glow on hover -->
<div class="glass-card hover-glow">Glows on hover</div>
```

### **Loading States**
```html
<!-- Shimmer loading effect -->
<div class="glass-card loading-shimmer h-24"></div>
```

### **Transition Classes**
```html
<!-- Apply to elements that need smooth transitions -->
<div class="transition-all">Smooth all properties</div>
<div class="transition-transform">Smooth transforms only</div>
<div class="transition-opacity">Smooth opacity only</div>
```

---

## ♿ **Accessibility Features**

### **Focus Management**
```html
<!-- All interactive elements automatically get focus styles -->
<button class="btn btn-primary">Accessible button</button>
<a href="#" class="focus-visible">Accessible link</a>
```

### **Skip Links**
```html
<a href="#main-content" class="skip-link">Skip to main content</a>
```

### **Screen Reader Support**
```html
<span class="sr-only">Screen reader only text</span>
```

### **Reduced Motion**
The system automatically respects `prefers-reduced-motion` and disables animations for users who prefer reduced motion.

---

## 📱 **Responsive Design**

### **Breakpoint System**
- `sm`: 640px and up
- `md`: 768px and up  
- `lg`: 1024px and up
- `xl`: 1280px and up
- `2xl`: 1536px and up

### **Responsive Utilities**
```html
<!-- Hide on mobile, show on desktop -->
<div class="hidden lg:block">Desktop only content</div>

<!-- Different layouts per breakpoint -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
  <div>Responsive grid item</div>
</div>

<!-- Responsive text alignment -->
<h1 class="text-center lg:text-left">Centered on mobile, left on desktop</h1>
```

---

## 🛠️ **Customization**

### **CSS Custom Properties**
You can easily customize the system by overriding CSS variables:

```css
:root {
  /* Change primary color */
  --primary-blue: #your-brand-color;
  
  /* Adjust spacing scale */
  --space-xl: 3rem; /* Instead of 2rem */
  
  /* Modify transition timing */
  --duration-normal: 250ms; /* Instead of 300ms */
  
  /* Custom marquee speed */
  --marquee-speed: 20s; /* Faster scrolling */
}
```

### **Adding Custom Components**
```css
/* Your custom component using the design system */
.my-custom-card {
  /* Use system variables */
  background: var(--glass-bg);
  border: 1px solid var(--glass-border);
  border-radius: var(--radius-lg);
  padding: var(--space-lg);
  
  /* Use system transitions */
  transition: all var(--duration-normal) var(--ease-smooth);
}

.my-custom-card:hover {
  background: var(--glass-bg-hover);
  transform: translateY(-2px);
}
```

---

## 🎯 **Best Practices**

### **Do's**
✅ Use the spacing scale consistently (`--space-*` variables)  
✅ Apply hover effects to interactive elements  
✅ Use semantic HTML with design system classes  
✅ Test with `prefers-reduced-motion`  
✅ Maintain color contrast ratios  
✅ Use `font-display` for headlines, `font-body` for content  

### **Don'ts**
❌ Mix spacing units (stick to the scale)  
❌ Override transition durations arbitrarily  
❌ Use colors outside the defined palette  
❌ Forget focus states on interactive elements  
❌ Ignore responsive breakpoints  
❌ Use animations without reduced motion fallbacks  

---

## 📦 **Integration Examples**

### **React Component**
```jsx
const TestimonialCard = ({ quote, author, title, company, isActive }) => (
  <div className={`glass-card glass-card-md relative ${isActive ? 'active-card' : 'inactive-card'}`}>
    {isActive && (
      <>
        <div className="corner-bracket top-left"></div>
        <div className="corner-bracket top-right"></div>
        <div className="corner-bracket bottom-left"></div>
        <div className="corner-bracket bottom-right"></div>
      </>
    )}
    <blockquote className="font-body text-body italic text-primary">
      "{quote}"
    </blockquote>
    <footer className="text-small text-muted mt-md">
      <div className="font-medium">{author}</div>
      <div>{title}, {company}</div>
    </footer>
  </div>
);
```

### **Vue Component**
```vue
<template>
  <div 
    :class="[
      'glass-card glass-card-md relative transition-all',
      isActive ? 'active-card' : 'inactive-card'
    ]"
  >
    <template v-if="isActive">
      <div class="corner-bracket top-left"></div>
      <div class="corner-bracket top-right"></div>
      <div class="corner-bracket bottom-left"></div>
      <div class="corner-bracket bottom-right"></div>
    </template>
    
    <blockquote class="font-body text-body italic text-primary">
      "{{ quote }}"
    </blockquote>
    
    <footer class="text-small text-muted mt-md">
      <div class="font-medium">{{ author }}</div>
      <div>{{ title }}, {{ company }}</div>
    </footer>
  </div>
</template>
```

---

## 🌟 **Light Theme Support**

Your design system now includes comprehensive light theme support! Use the `design-system-light.css` extension for light backgrounds.

### **Quick Setup**
```html
<!-- Include both files -->
<link rel="stylesheet" href="design-system.css">
<link rel="stylesheet" href="design-system-light.css">
```

### **Usage Options**

#### **Manual Light Theme**
```html
<section class="theme-light">
  <div class="glass-card glass-card-md hover-lift">
    <h3 class="font-display text-title text-primary">Light Theme Card</h3>
    <p class="font-body text-body text-secondary">Perfect for light backgrounds</p>
  </div>
</section>
```

#### **Automatic Theme Detection**
```html
<section class="theme-auto">
  <!-- Automatically switches based on user's system preference -->
  <div class="glass-card glass-card-md">
    <h3 class="font-display text-title text-primary">Auto Theme Card</h3>
  </div>
</section>
```

#### **Adaptive Sections**
```html
<section class="theme-adaptive light-context">
  <!-- Works on both light and dark, currently set to light -->
  <div class="glass-card glass-card-md">Content here</div>
</section>
```

### **What Changes on Light Backgrounds**

✅ **Glass Cards**: Semi-transparent white with subtle dark borders  
✅ **Text Colors**: Dark text hierarchy for perfect readability  
✅ **Shadows**: Softer, more subtle shadows that work on light surfaces  
✅ **Buttons**: Inverted glass effects with proper contrast  
✅ **Corner Brackets**: Orange accents remain visible and vibrant  
✅ **Carousel Fades**: Edge gradients adapted for light backgrounds  
✅ **Focus States**: Blue focus rings with light-appropriate opacity  

### **Brand Colors Maintained**
- **Primary Blue** (`#188bf6`) - Works beautifully on both themes
- **Accent Orange** (`#FF6A00`) - Pops on light and dark backgrounds  
- **Typography** - Playfair Display + Lato preserved across themes

---

This design system provides everything you need to create premium, professional interfaces that build trust and engage users. The modular approach means you can use as much or as little as needed for each project, and now works seamlessly on both light and dark backgrounds.
