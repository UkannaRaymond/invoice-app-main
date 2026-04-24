# Invoice App

A responsive full-stack invoice management application built with React + TypeScript with `localStorage` persistence. The app allows users to create, manage, and track invoices with a smooth and accessible user experience.

## Stack

- React
- TypeScript
- Vite
- LocalStorage for data persistence

---

## Live Demo

🔗 [View on Vercel](https://invoice-app-main-phi.vercel.app)

---

## How to Run Locally

### Option 1 — Clone the repo

```bash
git clone https://github.com/UkannaRaymond/invoice-app-main.git
cd invoice-app-main
```

```bash
npm install
npm run dev
```

## Production Build

```bash
npm run build
```

---

## Project Architecture

```
src
├── components
│ ├── button # Reusable button components and related logic
│ ├── forms # Invoice input forms and validation handling
│ ├── offCanvas # Drawer components for creating/editing invoices
│ └── modal # Confirmation modal (e.g., delete actions)
├── pages
│ ├── dashboard # Invoice list view with filtering functionality
│ ├── invoice # Individual invoice detail page
│ └── errors # Error handling pages (e.g., 404, fallback UI)
└── services
├── api # Thin abstraction layer over storage (future backend-ready)
└── storage # LocalStorage-based invoice CRUD operations
```

---

## How Data Is Stored

Invoices are seeded from the bundled Figma-style data on first load and then saved in `localStorage` under the `invoice-app-invoices` key.

This means:

- creating an invoice updates browser storage immediately
- editing an invoice persists after refresh
- deleting an invoice removes it from storage
- marking an invoice as paid updates the saved record

## Deployment

This app is ready for static hosting on Vercel or Netlify.

### Vercel

1. Push the repository to GitHub.
2. Import the repo in Vercel.
3. Set the build command to `npm run build`.
4. Set the output directory to `dist`.
5. Deploy.

## Notes

- The app keeps the original visual design and routing structure from the starter repo.
- Theme preference is also persisted locally.
- No backend or external API is required.

## Potential Future Improvements

Backend integration (Node/Express or database)
Authentication (user-specific invoices)
Export invoices as PDF
Pagination or virtualized lists
Unit and integration testing (Jest, React Testing Library)

## 📱 Responsiveness

Mobile: 320px+
Tablet: 768px+
Desktop: 1024px+

Layouts adapt dynamically with no horizontal overflow and consistent spacing.

## 🌓 Theme Support

Light and Dark mode available
Theme preference stored in LocalStorage
All components adapt to selected theme

👤 **Author**

Ukanna Raymond | Frontend | Backend

This project is part of my portfolio, showcasing frontend skills for a fullstack role. If you have questions, feedback, or would like to collaborate, feel free to get in touch!
