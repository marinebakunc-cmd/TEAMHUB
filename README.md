# TEAMHUB

Platform for idea validation — **StartupLaunch**, an end-to-end hub for
university student entrepreneurs. Five guided stages, faculty mentors, and a
marketplace, with views for students, mentors, and program admins.

## Running the project

Requires [Node.js](https://nodejs.org/) 18+.

```bash
npm install      # install dependencies
npm run dev      # start the dev server at http://localhost:5173
```

Other scripts:

```bash
npm run build    # production build into dist/
npm run preview  # serve the production build locally
```

## Project layout

The original artifact was exported as a single concatenated file
(`Incubation_acceleration`). It has been split into a runnable Vite + React
project:

| Path                | Contents                                              |
| ------------------- | ----------------------------------------------------- |
| `index.html`        | Vite entry document                                   |
| `src/main.jsx`      | The full React app (all screens + the preview panel)  |
| `src/styles.css`    | Design system and component styles                    |
| `vite.config.js`    | Vite + React plugin configuration                     |

The original export referenced a `tweaks-panel.jsx` script that was not
included in the bundle. It has been reconstructed at the top of `src/main.jsx`
as a small floating **Controls** panel (bottom-right) for switching theme,
density, demo stage, and role.
