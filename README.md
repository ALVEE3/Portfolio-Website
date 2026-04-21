# Ahadul Islam Chowdhury — Personal Portfolio

![Portfolio Preview](https://img.shields.io/badge/Status-Live-gold?style=flat-square&labelColor=111)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

A bold, dark-themed personal portfolio website for **Ahadul Islam Chowdhury (Alvee)** — a Software Engineer based in Dhaka, Bangladesh. Built with pure vanilla HTML, CSS, and JavaScript. No frameworks, no build tools, no dependencies. Just ship it.

---

## ✨ Features

### Core Portfolio Sections
- **Hero** — Name, tagline, profile photo with animated pulse ring, and CTA buttons
- **About** — Personal bio with animated stat cards (years of experience, projects, etc.)
- **Tech Stack** — Categorized skill grid with SVG logo icons for Languages, Frontend, Backend, Blockchain, DevOps, Databases, and Practices
- **Projects** — Featured project cards with stack tags and links; expandable to a full 10-project showcase page
- **Experience** — Animated timeline of work history
- **Contact** — Email with one-click copy, social links (GitHub, LinkedIn, Facebook) with pulse animations

### Multi-Page System
The site uses a lightweight client-side page switcher (no router, no SPA framework) — three pages in one HTML file:
- `main-page` — The main portfolio
- `projects-page` — Full project showcase (10 projects)
- `about-page` — Full background: education history + detailed work experience

### 🕷️ Alvee — The Interactive Spider Mascot
The signature easter egg of this portfolio. A custom SVG spider named **Alvee** follows your cursor around the page and has multiple interactive states:

| State | Description |
|---|---|
| **FOLLOWING** | Alvee tracks your mouse with smooth easing and leg-crawl animation |
| **PLAYING** | Alvee goes rogue — moves autonomously, dodging your shots |
| **DEAD** | Alvee collapses in place after being defeated; can be revived by clicking |

**Welcome Bubble Sequence** — On first load, Alvee introduces himself with a timed dialogue sequence:
1. *"Welcome, I am Alvee"*
2. *"I'll be your Tour Guide.."*
3. *(10s pause)* *"If you don't want me to follow, you can kill me by playing The Game"*

**Secret Swarm** — Click on Alvee 5 times quickly to trigger the swarm: 100 mini-spiders explode across the entire page with random movement, screen earthquake animation, and a dramatic sound effect for 10 seconds.

### 🎮 Let's Play — Mini Game
Click the **"Let's Play"** button on the hero section to launch a browser-based shooter mini-game:

- Enter your name to start
- **Objective:** Hit Alvee 10 times within 30 seconds
- **Controls:** Move mouse to aim the tank at the bottom of the screen; click to shoot
- **Win:** Alvee dies — visually collapses with greyscale filter, curled legs, and a twitching dead animation. Fireworks explode on screen.
- **Lose:** Timer runs out — laughing emoji rain falls across the screen
- **Revive:** Click on the dead Alvee to bring him back to life

### 🔊 Web Audio API Sound Effects
All game sounds are generated procedurally using the Web Audio API — no external audio files required:

| Action | Sound |
|---|---|
| Shoot | Square wave with pitch drop |
| Hit | Sawtooth burst |
| Win | Ascending sine arpeggio |
| Lose | Sawtooth descending tone |
| Revive | Sine frequency sweep |

---

## 📁 Project Structure

```
index.html          # Entire site — single file
│
├── Styles          # All CSS in <style> block (CSS custom properties, animations, responsive)
│
├── Pages           # Three .page divs, toggled via JS
│   ├── #main-page
│   ├── #projects-page
│   └── #about-page
│
└── Scripts         # Two <script> blocks at end of body
    ├── Page utilities  (showPage, goTo, scroll observer, email copy)
    └── Spider + Game   (Alvee mascot, mini-game, swarm, audio, bubbles)
```

---

## 🎨 Design System

All design tokens are CSS custom properties defined on `:root`:

| Token | Value | Usage |
|---|---|---|
| `--gold` | `#c9a84c` | Primary accent — borders, headings, icons |
| `--gold-light` | `#e8c96a` | Hover states, highlights |
| `--gold-dark` | `#9a7a2e` | Subtle accents, outlines |
| `--gold-glow` | `rgba(201,168,76,.15)` | Background glows |
| `--bg` | `#080808` | Main background |
| `--bg2` | `#101010` | Section alternate background |
| `--bg3` | `#181818` | Card backgrounds |
| `--text` | `#f0f0f0` | Body text |
| `--muted` | `#888` | Secondary text |

---

## 🚀 Getting Started

No build step. No npm install. Just open the file.

```bash
# Clone the repository
git clone https://github.com/ALVEE3/portfolio.git

# Open in browser
open index.html
```

Or simply drag `index.html` into any browser window.

**To deploy:**
- Drop `index.html` onto [Netlify Drop](https://app.netlify.com/drop)
- Push to GitHub and enable **GitHub Pages**
- Upload to any static hosting (Vercel, Cloudflare Pages, etc.)

---

## 🛠️ Customization

### Update personal info
All content is inline in the HTML. Search for the following to update:

| What | Where to find it |
|---|---|
| Name / tagline | `#hero` section |
| Profile photo | `<img class="hero-photo" src="...">` |
| About text | `#about` section |
| Stat numbers | `.stat-card` elements |
| Projects | `.project-card` elements in `#projects` and `#projects-page` |
| Experience | `.exp-item` elements in `#experience` |
| Education | `.edu-item` elements in `#about-page` |
| Email | `href` and `onclick` on `.contact-email` |
| Social links | `.social-links` in `#contact` |

### Add/remove skill icons
Each skill category is a `.skill-cat` div inside `.skills-grid`. Skill icons use inline SVGs from [Simple Icons](https://simpleicons.org/).

---

## 📱 Responsive Design

The layout adapts to mobile via a single media query at `680px`:
- Navigation links hidden on small screens
- Hero layout stacks vertically (photo above content)
- Profile photo scales down from `280px` to `180px`
- All grids reflow naturally via `auto-fit` / `minmax`

---

## 🧩 Browser Compatibility

| Feature | Requirement |
|---|---|
| CSS Custom Properties | All modern browsers |
| IntersectionObserver | Chrome 58+, Firefox 55+, Safari 12.1+ |
| Web Audio API | Chrome 35+, Firefox 25+, Safari 14.1+ |
| `navigator.clipboard` | HTTPS required; falls back to `execCommand` |
| CSS `-webkit-text-stroke` | All modern browsers |

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🙋 Author

**Ahadul Islam Chowdhury**
Software Engineer · Dhaka, Bangladesh

- GitHub: [@ALVEE3](https://github.com/ALVEE3)
- LinkedIn: [ahadul-islam-chowdhury](https://www.linkedin.com/in/ahadul-islam-chowdhury-1805221b7/)
- Email: alvee678876@gmail.com

---

*Built with ❤️ and zero dependencies.*
