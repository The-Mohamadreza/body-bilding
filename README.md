<div align="center">

# 🏋️ IRONFORGE

### *Forge Your Limits — Elite Strength Studio*

<img src="https://img.shields.io/badge/HTML5-000000?style=for-the-badge&logo=html5&logoColor=D4AF37" />
<img src="https://img.shields.io/badge/CSS3-000000?style=for-the-badge&logo=css3&logoColor=D4AF37" />
<img src="https://img.shields.io/badge/JavaScript-000000?style=for-the-badge&logo=javascript&logoColor=D4AF37" />
<img src="https://img.shields.io/badge/Vanilla_JS-No_Frameworks-000000?style=for-the-badge&logoColor=D4AF37" />

<img src="https://img.shields.io/badge/status-live-D4AF37?style=flat-square&labelColor=000000" />
<img src="https://img.shields.io/badge/license-MIT-D4AF37?style=flat-square&labelColor=000000" />
<img src="https://img.shields.io/badge/responsive-yes-D4AF37?style=flat-square&labelColor=000000" />

<br />

**A cinematic, high-performance landing page for an elite strength & conditioning studio.**
**Built with pure HTML, CSS & JavaScript — zero frameworks, zero build step.**

</div>

<br />

<div align="center">
<img src="https://img.shields.io/badge/▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬-black?style=flat-square" />
</div>

<br />

## ✦ Overview

**IRONFORGE** is a single-page marketing site for a private strength studio, designed with an editorial, high-contrast aesthetic — black backgrounds, burnt-orange accents, and bold condensed typography.

The page ships as three clean, decoupled files, unpacked from a single minified build into readable source:

```
ironforge/
├── index.html    → Structure & content
├── style.css     → Design system, layout & animations
└── script.js     → Interactivity, chat engine & booking logic
```

No build tools. No bundler. Just open `index.html` and it runs.

<br />

## ✦ Features

| | |
|---|---|
| ⏳ **Animated Preloader** | A percentage-counter loading screen with a filling progress bar before the page reveals itself |
| 🧭 **Sticky Blur Navigation** | Glassmorphism nav bar that condenses on scroll, plus a full-screen mobile menu |
| 🖼 **Grayscale Cinematic Imagery** | Desaturated, high-contrast hero and section imagery for a premium editorial feel |
| 🏋️ **Program Cards** | Three signature programs (Hypertrophy, Shred, Foundation) with specs, descriptions & CTAs |
| 🧑‍🏫 **Coach Profiles** | Hover-reveal credential cards for each staff coach |
| ↔️ **Before/After Slider** | A draggable comparison slider (mouse + touch) showcasing real transformation results |
| 📅 **Weekly Class Schedule** | A responsive grid timetable of classes by day and time slot |
| 📝 **Trial Booking Form** | A styled lead-capture form with instant-feedback submit state |
| 💬 **AI-Style Chat Widget** | A built-in keyword-intent chatbot ("Coach Maya") that understands goals, pricing questions, objections, and guides users toward booking a trial — entirely in vanilla JS, no external API |
| 📱 **Fully Responsive** | Mobile-first breakpoints down to small phones, including an adaptive chat window and schedule table |
| ♿ **Reduced Motion Aware** | Respects user motion preferences via CSS custom properties and transitions |

<br />

## ✦ Tech Stack

<div align="center">

<img src="https://img.shields.io/badge/HTML5-Semantic_Markup-000000?style=flat-square&logo=html5&logoColor=D4AF37&labelColor=000000" /><br/>
<img src="https://img.shields.io/badge/CSS3-Custom_Properties_%7C_Grid_%7C_Flexbox_%7C_Animations-000000?style=flat-square&logo=css3&logoColor=D4AF37&labelColor=000000" /><br/>
<img src="https://img.shields.io/badge/JavaScript-Vanilla_ES6+-000000?style=flat-square&logo=javascript&logoColor=D4AF37&labelColor=000000" /><br/>
<img src="https://img.shields.io/badge/Font_Awesome-Icons-000000?style=flat-square&logo=fontawesome&logoColor=D4AF37&labelColor=000000" /><br/>
<img src="https://img.shields.io/badge/Google_Fonts-Anton_%7C_Oswald_%7C_Barlow_Condensed_%7C_JetBrains_Mono-000000?style=flat-square&logo=googlefonts&logoColor=D4AF37&labelColor=000000" />

</div>

<br />

## ✦ Getting Started

**No installation. No dependencies. No `npm install`.**

```bash
# 1. Clone the repository
git clone https://github.com/your-username/ironforge-studio.git

# 2. Move into the project folder
cd ironforge-studio

# 3. Open it in your browser
open index.html      # macOS
start index.html      # Windows
xdg-open index.html   # Linux
```

Or serve it locally for the full experience (recommended, since web fonts and icons load faster over a local server):

```bash
npx serve .
# or
python3 -m http.server 8000
```

Then visit **`http://localhost:8000`**.

<br />

## ✦ Project Structure

```
📦 ironforge-studio
 ┣ 📜 index.html      → Page structure: nav, hero, programs, coaches,
 ┃                       transformation stories, schedule, booking & footer
 ┣ 🎨 style.css        → Design tokens, layout, components, responsive rules,
 ┃                       loader, chat widget & scroll-reveal animations
 ┗ ⚙️  script.js        → Preloader logic, scroll reveal engine, before/after
                          slider, booking form, and the chat intent engine
```

<br />

## ✦ Customization

Everything starts at the top of `style.css`:

```css
:root {
  --bg: #0a0a0a;          /* base background        */
  --orange: #ff5e1a;      /* primary accent / CTA    */
  --orange-bright: #ff7a3d;
  --silver: #b8b8b8;      /* secondary text          */
}
```

Programs and coaches live directly in the markup inside `index.html` — duplicate a `.program-card` or `.coach-card` block to add a new one.

The chat widget's brain lives in `script.js` as a simple, editable intent list:

```js
const INTENTS = [
  {
    id: "pricing",
    kws: ["price", "cost", "membership", "how much"],
    reply: () => "Memberships start at <strong>$189/mo</strong>...",
    chips: () => ["Book a trial", "Compare programs"]
  },
  // add your own intents here
];
```

Each intent matches on keywords and returns a reply plus quick-reply chip suggestions — no external AI API required.

<br />

## ✦ Browser Support

<div align="center">

<img src="https://img.shields.io/badge/Chrome-✓-000000?style=flat-square&logo=googlechrome&logoColor=D4AF37" />
<img src="https://img.shields.io/badge/Firefox-✓-000000?style=flat-square&logo=firefox&logoColor=D4AF37" />
<img src="https://img.shields.io/badge/Safari-✓-000000?style=flat-square&logo=safari&logoColor=D4AF37" />
<img src="https://img.shields.io/badge/Edge-✓-000000?style=flat-square&logo=microsoftedge&logoColor=D4AF37" />

</div>

<br />

## ✦ License

Distributed under the **MIT License**. Feel free to use, modify, and build on top of it.

<br />

<div align="center">

<img src="https://img.shields.io/badge/▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬-black?style=flat-square" />

<br />

</div>
