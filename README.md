# Future Vizion - Chrome Extension Page

Companion landing page for the **Future_Vizion Photo New Tab** Chrome extension by [Guillermo Alarcor](https://www.futurevizion.jp/). Every time you open a new tab, a handpicked high-resolution photograph replaces the default Chrome page.

**Live:** [future-vizion.cuatro.dev](https://future-vizion.cuatro.dev)

<p align="center">
    <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white" alt="HTML5" />
    <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white" alt="CSS3" />
    <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black" alt="JavaScript" />
    <img src="https://img.shields.io/badge/jQuery-0769AD?style=flat&logo=jquery&logoColor=white" alt="jQuery" />
    <img src="https://img.shields.io/badge/Deployed%20on-Vercel-black?style=flat&logo=vercel" alt="Deployed on Vercel" />
</p>

---

## What it is

This is the info page served inside the Chrome extension when the user clicks the settings panel. It covers:

- Artist biography and design philosophy
- FAQ (style, pricing, contact, how the extension works)
- Links to prints, contact form, and social channels

## User flow

```mermaid
graph LR
    A[User opens new tab] --> B[Extension injects photo]
    B --> C[User clicks settings icon]
    C --> D[Panel slides open]
    D --> E[This page loads inside the panel]
    E --> F[User browses FAQ or follows social links]
```

## Stack decisions

| Decision  | Choice             | Why                                                                    |
| --------- | ------------------ | ---------------------------------------------------------------------- |
| Framework | None               | Single static page, no routing or state needed                         |
| CSS       | Vanilla + minified | Design-heavy animations handled without runtime overhead               |
| JS        | jQuery + vanilla   | Lightweight enough; parallax and canvas background in one bundled file |
| Deploy    | Vercel             | Zero-config static hosting, custom domain via CNAME                    |

## Local setup

No build step required.

```bash
git clone git@github.com:LuigiEspinosa/future-vizion.git
cd future-vizion
# open index.html directly in a browser, or use any static file server:
npx serve .
```

## Build Phases

| Phase           | Status | Notes                                               |
| --------------- | ------ | --------------------------------------------------- |
| Design + assets | Done   | Minified CSS and JS, custom icon fonts              |
| HTML structure  | Done   | Single page, sliding panel, FAQ sections            |
| Animations      | Done   | Canvas background, parallax scroll, CSS transitions |
| Deploy          | Done   | Vercel + custom domain `future-vizion.cuatro.dev`   |
