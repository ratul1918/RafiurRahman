# Rafiur Rahman — Portfolio

A personal portfolio for a CSE student, development learner, vibe coder, and aspiring researcher exploring artificial intelligence, machine learning, and computer vision.

**Live site:** [RafiurRahman](https://ratul1918.github.io/RafiurRahman/)

## What’s inside

- Responsive editorial design with warm accents, animated artwork, scroll reveals, and reduced-motion support.
- Light and dark themes: follows the device preference initially and remembers a visitor’s selection locally.
- Recent work: The LightHouse, Cha Ghor, CollabForge, and Elite Pitch, with repository links and clear project statuses.
- Selected web and mobile projects, with illustrative visuals labeled as interface studies.
- A dedicated research section for early exploration in AI, ML, and computer vision.
- Personal background, learning interests, milestones, and links to GitHub, LinkedIn, and Codeforces.
- Contact through an email link and a copy-address button. There is no contact-form backend.

Research interests are presented as a learning journey, not completed publications or established expertise. Project information is maintained manually; dates reflect repository activity rather than a live GitHub feed.

## Stack

The current page uses **React 18, TypeScript, Vite, Motion, Lucide icons, and plain CSS**. Project illustrations and the animated hero sculpture are built with HTML/CSS. The portrait is bundled locally. Fonts are loaded from Google Fonts with local fallbacks.

The repository retains older template components and dependencies, but the current page does not render them.

## Run locally

Use Node.js 22 LTS and npm.

```sh
git clone https://github.com/ratul1918/RafiurRahman.git
cd RafiurRahman
npm ci
npm run dev
```

Open the local URL printed by Vite, normally `http://localhost:3000`.

```sh
npm run typecheck
npm run build
npm run preview
```

- `typecheck` validates the active application and its imported components.
- `build` creates the production site in `dist/`.
- `preview` serves that production build locally; use the URL it prints.

No environment variables or API keys are required. The application uses section anchors such as `/#research`, rather than separate page routes.

## CV

[View or download the CV](https://ratul1918.github.io/RafiurRahman/cv/rafiur-rahman-cv.pdf). The homepage includes a download link and an About-section PDF link.

The editable LaTeX source is `public/cv/rafiur-rahman-cv.tex`. To rebuild it after editing (requires a LaTeX installation):

```sh
mkdir -p /tmp/portfolio-cv-build
pdflatex -interaction=nonstopmode -halt-on-error -output-directory=/tmp/portfolio-cv-build public/cv/rafiur-rahman-cv.tex
pdflatex -interaction=nonstopmode -halt-on-error -output-directory=/tmp/portfolio-cv-build public/cv/rafiur-rahman-cv.tex
cp /tmp/portfolio-cv-build/rafiur-rahman-cv.pdf public/cv/rafiur-rahman-cv.pdf
```

Review the generated PDF before committing. Vite copies `public/cv/` into the production build; GitHub Actions uses the committed PDF.

## Edit content

| File | Purpose |
| --- | --- |
| `src/pages/Home.tsx` | Introduction, navigation, theme control, selected projects, background, toolkit, contact, and footer |
| `src/components/RecentWork.tsx` | Recent projects, demo links, interests, and milestones |
| `src/components/Research.tsx` | AI, ML, and computer vision research interests and learning plans |
| `src/index.css` | Layout, animations, responsive breakpoints, and both themes |
| `src/assets/` | Local portrait image |
| `index.html` | Page title, social metadata, and initial theme selection |
| `.github/workflows/pages.yml` | Build and deploy the portfolio to GitHub Pages |

Keep descriptions and statuses accurate when updating projects. Only add demo links that point to an actual deployment. Contact links open the visitor’s email client; copying an address does not send a message.

## Deployment

GitHub Actions publishes the Vite production build to GitHub Pages on pushes to `main`. See [DEPLOYMENT.md](DEPLOYMENT.md) for deployment and search indexing details.

## Validation notes

The active application has a dedicated TypeScript configuration in `tsconfig.app.json`. Running the original repository-wide `npx tsc --noEmit` also checks unused legacy UI templates, which contain pre-existing version-suffixed import errors. The old lint command likewise requires an ESLint setup that is not included; use the documented typecheck and production build for this application.

## Credits

React, Vite, Motion, and Lucide power the current implementation. See [src/Attributions.md](src/Attributions.md) for retained template attributions.
