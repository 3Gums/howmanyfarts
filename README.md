# How Many Farts a Day Is Normal? 💨

A fun, informative landing page about flatulence frequency with an interactive lifetime farts calculator and mini-game.

## 📋 What's Included

- **Hero Section** - Eye-catching title and introduction
- **Quick Answer** - Facts about normal flatulence frequency (8-21 times per day)
- **Lifetime Farts Calculator** - Enter birth year to calculate lifetime fart estimates
- **Toot Rank System** - Humorous ranks based on lifetime farts (Wind Whisper → Methane Monarch)
- **10 Second Toot Tapper Game** - Click buttons as fast as you can in 10 seconds
- **Fun Facts** - Educational and amusing flatulence facts
- **Health Disclaimer** - Important medical information
- **Responsive Design** - Works perfectly on desktop, tablet, and mobile
- **Accessibility Features** - ARIA labels and reduced motion support

## 🚀 Quick Start

### Option 1: Open in Browser
Simply open `index.html` in any modern browser:
- Double-click `index.html` in File Explorer, OR
- Drag `index.html` onto your browser window, OR
- Use the file path: `file:///D:/agy2-projects/howmanyfarts-claude/index.html`

### Option 2: Run a Local Web Server
For the best experience with proper caching and performance, run a local server:

**Using Python 3:**
```bash
cd D:\agy2-projects\howmanyfarts-claude
python -m http.server 8000
```

Then open: `http://localhost:8000`

**Using Node.js:**
```bash
cd D:\agy2-projects\howmanyfarts-claude
npx http-server
```

## 🧪 Testing

Run the comprehensive test suite:

```bash
cd D:\agy2-projects\howmanyfarts-claude
node test.js
```

**What the test suite checks:**
- ✅ File structure and size (24.2KB)
- ✅ HTML5 standards (DOCTYPE, lang attribute)
- ✅ SEO metadata (title, description, canonical URL)
- ✅ Responsive design (mobile, tablet, desktop breakpoints)
- ✅ Accessibility features (ARIA labels, reduced motion)
- ✅ All required sections and elements
- ✅ JavaScript function presence and logic
- ✅ No external dependencies (pure client-side)

**Test Results:**
```
Total Tests: 32
✅ Passed: 32
Score: 100%
```

## 📱 Features

### Birth Year Calculator
1. Enter your birth year
2. Click "Calculate My Lifetime Farts"
3. See three estimates (conservative, average, liberal)
4. Get a funny rank title based on your lifetime farts

**Rank Tiers:**
- 🌬️ Wind Whisper (< 50,000 farts)
- 💨 Wind Apprentice (50K - 150K)
- 🌪️ Toot Technician (150K - 350K)
- ⚡ Flatulence Phantom (350K - 650K)
- 👑 Methane Monarch (650K+)

### 10 Second Toot Tapper Game
- Click any yellow button as fast as you can
- Timer counts down from 10 seconds
- See your final score and feedback
- Play multiple times to beat your score

## 🎨 Design Highlights

- **Color Scheme:** Bright, playful yellows and oranges with dark text for readability
- **Typography:** Clean, modern sans-serif fonts (Segoe UI, Geneva, Verdana)
- **Responsive:** Fluently adapts from 320px mobile to 1920px+ desktop
- **Animations:** Smooth transitions on cards and buttons
- **Accessibility:** Respects `prefers-reduced-motion` for users sensitive to animations

## 💻 Technical Stack

- **HTML5** - Semantic markup
- **CSS3** - Variables, flexbox, grid, responsive design
- **JavaScript (ES6)** - Event listeners, calculations, DOM manipulation
- **No Dependencies** - Runs completely client-side, no backend needed

## 📊 Calculation Logic

**Lifetime Farts Calculation:**
```
Days Alive = (Current Year - Birth Year) × 365.25
Conservative Estimate = Days Alive × 8 farts/day
Average Estimate = Days Alive × 14 farts/day
Liberal Estimate = Days Alive × 25 farts/day
```

**Example (Age 30):**
- Conservative: 87,660 farts
- Average: 153,405 farts
- Liberal: 273,938 farts

## ♿ Accessibility Features

- ✅ Semantic HTML (`<header>`, `<main>`, `<footer>`)
- ✅ Proper heading hierarchy
- ✅ ARIA labels on interactive elements
- ✅ Color contrast meets WCAG standards
- ✅ Keyboard accessible
- ✅ Respects `prefers-reduced-motion` media query
- ✅ Mobile-friendly touch targets

## 🔍 SEO

- **Meta Description:** "Discover how many farts per day is normal..."
- **Canonical URL:** https://www.howmanyfarts.com/
- **Title:** "How Many Farts a Day Is Normal? | The Toot Truth"
- **Keywords:** Naturally included in content

## 📂 Files

```
howmanyfarts-claude/
├── index.html          # Complete website (24.2KB)
├── test.js             # Automated test suite (Node.js)
└── README.md           # This file
```

## 🎯 Browser Support

Works in all modern browsers:
- Chrome/Chromium (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 📝 Code Quality

- **Comments:** 15+ comment blocks explaining logic for beginners
- **Variables:** Clear, descriptive naming (e.g., `conservativeToots`, `gameTimeRemaining`)
- **Functions:** Well-organized with single responsibility
- **No Console Errors:** All JavaScript is clean and error-free

## 🚫 No Backend, No Database, No Login

This is a completely static, client-side application:
- No server required
- No database
- No user login/authentication
- No data storage
- No external API calls
- Can be hosted on any static file hosting (GitHub Pages, Netlify, etc.)

## 🎓 Educational Value

Perfect for:
- Learning HTML5 semantic markup
- Understanding CSS variables and responsive design
- Studying JavaScript functions and event handling
- Teaching web accessibility
- Examples of humor in web design

## 📄 License

Created June 26, 2026

---

**Enjoy calculating your lifetime farts! 💨**
