# SFAIwala — Cleaning Services Website

A responsive, multi-page marketing website for a home and commercial cleaning service. Visitors can browse the service catalogue, read about the business, and send an enquiry that opens a pre-filled WhatsApp message to the business.

Built with **React 19**, **Vite 7**, **Tailwind CSS 4** and **React Router 7**.

## Features

- **Five routes:** Home (`/`), About (`/about`), Services (`/service`), Contact (`/contact`) and a booking Form (`/form`)
- **Service catalogue** covering 20+ services, including deep home, kitchen, bathroom, sofa, carpet, mattress, water-tank, office and hotel cleaning
- **Enquiry and booking forms** that build a message and open WhatsApp (`wa.me`) with the details pre-filled, so no backend is needed
- **Floating WhatsApp button** available across the site
- **Image slider** and work gallery on the home page
- **Embedded map** on the contact page
- Scroll-to-top on route change, shared Navbar and Footer
- Linting with ESLint 9 (React Hooks and React Refresh rules)

## Tech stack

| Area | Tools |
|---|---|
| UI | React `^19.1.0`, React DOM `^19.1.0` |
| Routing | React Router DOM `^7.7.0` |
| Styling | Tailwind CSS `^4.1.11` (via `@tailwindcss/vite`) |
| Icons | Lucide React `^0.525.0`, Remix Icon `^4.6.0` |
| Build tool | Vite `^7.0.4`, `@vitejs/plugin-react` `^4.6.0` |
| Linting | ESLint `^9.30.1` |

## Project structure

```text
sfaiwala/
├── public/images/        # Service and gallery images, logo
├── src/
│   ├── components/       # Navbar, Footer, Slider, Work, ScrollToTop
│   ├── pages/            # Home, About, Service, Contact, Form
│   ├── utility/          # Button, Map, Whatsapp (floating button)
│   ├── App.jsx           # Router and layout
│   ├── main.jsx          # Entry point
│   └── index.css         # Tailwind entry and global styles
├── index.html
├── vite.config.js
├── eslint.config.js
└── package.json
```

## Getting started

Requires Node.js 18 or newer.

```bash
git clone https://github.com/Abhishek7258/sfaiwala.git
cd sfaiwala
npm install
npm run dev
```

The dev server runs at http://localhost:5173.

## Scripts

| Command | What it does |
|---|---|
| `npm run dev` | Start the Vite dev server |
| `npm run host` | Start the dev server exposed on your network (test on a phone) |
| `npm run build` | Create a production build in `dist/` |
| `npm run preview` | Serve the production build locally |
| `npm run lint` | Run ESLint |

## Deployment

`npm run build` outputs a static site in `dist/`, which works on Netlify, Vercel, GitHub Pages or any static host. Because the app uses client-side routing (`BrowserRouter`), configure the host to fall back to `index.html` for unknown paths so refreshing `/service` or `/contact` works.

## Customising

- Services, copy and images live in `src/pages/` and `public/images/`.
- The business WhatsApp number is set in `src/pages/Form.jsx`, `src/pages/Contact.jsx` and `src/utility/Whatsapp.jsx`. Update all three together.
