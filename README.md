# Schultz Brutalist UI

> **Schultz Brutalist UI: An uncompromising, zero-dependency CSS framework for technical developer tools. Pure monochrome, sharp 90° edges, hard block shadows, and Code Brutalism.**

This framework provides the aesthetic foundation for Schultz Software's developer tools and web applications. It is engineered for maximum readability, high visual authority, and zero runtime lag.

---

## 🎨 Core Design Principles (100% Zero-Dependency)

Modern developer tool design (popularized by Linear, Vercel, Raycast, and Club Matto) moves away from bloated SaaS templates, heavy JavaScript frameworks, and slow external webfonts toward **Tactile & Code Brutalism**. 

**Strict Guarantee:** Every single principle and component in this framework is **100% Zero-Dependency** (0 NPM packages, 0 KB JavaScript, 0 external font CDNs, 0 external icon packs).

### 1. Code Brutalism & Technical Mono (Native System Stack)
* **Terminal as Primary Interface:** Developers and data engineers trust interfaces that reflect their daily terminal and IDE workflow. Rather than decorative graphics, live ASCII tables, shell commands, and syntax payloads are front and center.
* **Monospace Without Font Downloads:** Uses the operating system's native monospace stack (`ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace`). Instant zero-latency rendering with zero external Google Fonts requests.

### 2. Tactile Brutalism & Hard Offsets (Pure CSS3)
* **Sharp 90° Geometry (`border-radius: 0`):** Rounded corners feel soft and informal. Sharp right angles convey architectural solidity and engineering discipline.
* **Solid Block Shadows (No Blur):** Shadows are solid, unblurred offsets (`box-shadow: 4px 4px 0px #000000` or `6px 6px 0px #000000`).
* **Mechanical Push Feedback:** Interactive elements physically push down on click/hover (`transform: translate(2px, 2px)`) as their shadow collapses, mimicking the tactile action of a heavy mechanical keyboard switch without any animation JavaScript.

### 3. Architectural Blueprint Grid (Pure CSS Gradient)
* **Visible Construction Lines:** Rather than hiding structure in blank whitespace, technical pages embrace a faint 24px blueprint/graph-paper grid (`.sbrutalist-blueprint-bg`). Rendered via pure CSS `linear-gradient` without SVG or image file requests.

### 4. Hardware Haptics & Mechanical Keycaps (Native `<kbd>`)
* **Tactile Shortcuts:** Terminal and CLI tools thrive on keyboard shortcuts. Keycaps styled with `<kbd class="sbrutalist-kbd">` simulate real keycaps with crisp borders and drop shadows using native semantic HTML tags.

### 5. Engineering Readouts & Telemetry (Pure CSS Shapes)
* **High-Trust Status Badges:** Key architectural specs (`ARCH: x86_64-musl`, `ZERO-DEP`, `OFFLINE-FIRST`) are surfaced in high-contrast badges (`.sbrutalist-spec-pill`). Status dots are pure CSS circles (`border-radius: 50%`) with zero icon fonts (no FontAwesome, no Lucide).

### 6. Machine Experience (MX) & Zero-Lag Architecture
* **Zero JavaScript Dependency:** The framework requires 0 KB of client JavaScript. It renders instantly, avoids hydration delays, and provides clean semantic HTML that is easily indexed by search engines and AI crawlers.

---

## 🌈 Color Palette

### Monochrome Base
* **Background (Body):** `#FFFFFF` (Pure white) or `.sbrutalist-blueprint-bg` (24px technical grid)
* **Primary Text & Borders:** `#000000` (Pure black for maximum contrast and legibility)
* **Terminal Background:** `#050505` (Deep dark slate) with `#141414` header bar

### Intentional Action Accents (Use Sparingly!)
* **Primary Action & Terminal Prompt (Green):** `#00C853`
* **Warning & Pro Badges (Yellow):** `#FFD600`
* **Danger & Destructive Actions (Red):** `#FF3860`

---

## 💻 Component Library & Code Examples

### 1. The Terminal Component (CLI Previews)
Authentic terminal window with window controls, command prompt, and horizontal scrolling.
```html
<div class="sbrutalist-terminal">
    <div class="sbrutalist-terminal-header">
        <div class="sbrutalist-terminal-dots">
            <span class="sbrutalist-terminal-dot"></span>
            <span class="sbrutalist-terminal-dot"></span>
            <span class="sbrutalist-terminal-dot"></span>
        </div>
        <span>bash — tablemock</span>
        <button class="sbrutalist-copy-btn">COPY</button>
    </div>
    <div class="sbrutalist-terminal-body">
        <pre><span class="sbrutalist-terminal-prompt">$</span> tablemock -p users -r 10000 --seed 42 -o users.csv
🚀 Starting generation of 10000 rows into 'users.csv'...
✅ Successfully generated 10000 rows
📦 File saved to: users.csv</pre>
    </div>
</div>
```

### 2. Mechanical Keyboard Keycaps (`<kbd>`)
Tactile physical keycaps for displaying CLI/TUI shortcuts.
```html
<p>
    Controls:
    <kbd class="sbrutalist-kbd">Enter</kbd> Run
    <kbd class="sbrutalist-kbd">+</kbd> Add
    <kbd class="sbrutalist-kbd">t</kbd> Type
    <kbd class="sbrutalist-kbd">q</kbd> Quit
</p>
```

### 3. Engineering Spec Pills & Telemetry
Status pills for displaying machine specs and live states.
```html
<span class="sbrutalist-spec-pill">
    <span class="status-dot"></span>ENGINE: RUST
</span>
<span class="sbrutalist-spec-pill">
    <span class="status-dot"></span>BINARY: STATIC MUSL
</span>
```

### 4. The Brutalist Box (Cards & Containers)
Container with 2px solid border and 6px solid offset shadow.
```html
<div class="sbrutalist-box">
    <h2 class="sbrutalist-h2">Buffered Streaming Engine</h2>
    <p class="sbrutalist-p">Direct row-by-row output for generating large CSV and TSV datasets.</p>
</div>
```

### 5. Interactive Action Buttons (The "Push" Effect)
```html
<!-- Primary Black Button -->
<a href="#buy" class="sbrutalist-btn-black">Buy Pro (69 €) &rarr;</a>

<!-- Accent Green Button -->
<button class="sbrutalist-btn-primary">Generate Data</button>

<!-- Secondary White Button -->
<button class="sbrutalist-btn-secondary">Download Basis</button>
```

### 6. B2B Pricing Cards
High-impact pricing boxes for clear distinction between Free Trial and Commercial Pro tiers.
```html
<div class="sbrutalist-pricing-card featured">
    <div>
        <span class="sbrutalist-badge sbrutalist-badge-invert">PRO 69 €</span>
        <h3 class="sbrutalist-h2">PRO EDITION</h3>
        <div class="sbrutalist-price-tag">69 €</div>
        <div class="sbrutalist-price-sub">One-Time Perpetual License</div>
        <ul class="sbrutalist-feature-list">
            <li><span class="bullet">✓</span><div class="feature-text">Unlimited Rows &amp; Columns</div></li>
            <li><span class="bullet">✓</span><div class="feature-text">CSV &amp; TSV Formats</div></li>
            <li><span class="bullet">✓</span><div class="feature-text">Commercial Developer License</div></li>
        </ul>
    </div>
    <a href="#checkout" class="sbrutalist-btn-black">Buy Pro License &rarr;</a>
</div>
```

### 7. Technical Comparison Tables
High-contrast comparison tables with dark headers.
```html
<table class="sbrutalist-table">
    <thead>
        <tr>
            <th>Feature</th>
            <th>Basis Edition</th>
            <th style="background-color: #222;">Pro Edition</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Max Rows</td>
            <td>1,000 Rows</td>
            <td><strong>Unlimited</strong></td>
        </tr>
    </tbody>
</table>
```

### 8. Architectural Blueprint Background Grid
To enable the subtle 24px technical grid, add the class to the `<body>` element:
```html
<body class="sbrutalist-blueprint-bg">
    <!-- Page Content -->
</body>
```

### 9. Disabled & Coming-Soon States
For pre-release products or deactivated sections, use the disabled modifier classes to visually grey out elements and prevent user interaction (`pointer-events: none`):
```html
<!-- Disabled Card / Section -->
<div class="sbrutalist-box sbrutalist-disabled">
    <span class="sbrutalist-badge sbrutalist-badge-disabled">COMING SOON</span>
    <h2 class="sbrutalist-h2">Upcoming Product</h2>
    <span class="sbrutalist-btn-disabled">Coming Soon</span>
</div>

<!-- Disabled Inline Link -->
<span class="sbrutalist-link-disabled">CSVREPORT (Coming Soon)</span>
```

---

## 📂 Showroom & Live Demo

The interactive showroom is located in `showroom/`:
* **`showroom/index.html`**: Complete living showcase demonstrating every component and principle.
* **`showroom/sbrutalist.css`**: The compiled, standalone CSS stylesheet.
* **`showroom/template.html`**: Clean starter boilerplate.

Open `showroom/index.html` in any browser to inspect the components and test hover interactions.
