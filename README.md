# Astro Starter Kit: Basics

```sh
npm create astro@latest -- --template basics
```

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/withastro/astro/tree/latest/examples/basics)
[![Open with CodeSandbox](https://assets.codesandbox.io/github/button-edit-lime.svg)](https://codesandbox.io/p/sandbox/github/withastro/astro/tree/latest/examples/basics)
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/withastro/astro?devcontainer_path=.devcontainer/basics/devcontainer.json)

> 🧑‍🚀 **Seasoned astronaut?** Delete this file. Have fun!

![just-the-basics](https://github.com/withastro/astro/assets/2244813/a0a5533c-a856-4198-8470-2d67b1d7c554)

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
│   └── favicon.svg
├── src/
│   ├── layouts/
│   │   └── Layout.astro
│   └── pages/
│       └── index.astro
└── package.json
```

To learn more about the folder structure of an Astro project, refer to [our guide on project structure](https://docs.astro.build/en/basics/project-structure/).

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).

# Teknisk dokumentation for TankeStrøm

Når man er flere der bidrager til en kodebase, lærer man hurtigt, at ens sædvanlige måder at gøre tingene på ikke nødvendigvis er logisk for alle. Dokumentationen sikrer, at vores fælles kodebase forbliver overskuelig, er let at arbejde med og til at forstå for alle, og at vi undgår konflikter og har nemmere ved at hjælpe hinanden undervejs.

## Projektstruktur:

Komponenter inkluderer fx:
EventCard.astro – visning af events på forsiden
SingleEventCard.astro – visning af detaljeret event
TimelineCard.astro – bruges til foreningens historiske milepæle
IndexHero.astro, AboutHero.astro, EventlistHero.astro – hero-sektioner

Pages inkluderer:
index.astro – forside
about.astro – Om TankeStrøm
eventlist.astro – listevisning af events
[slug].astro – dynamisk rute til single event-visning

Boilerplate og styling:
CSS-filer og globale styles ligger i /src/style/
Billeder er placeret i /public/img/webp/
JS bruges ikke i større omfang pga. Astro’s fokus på statiske sider. Dog ses mest js på Menu.astro

## Navngivning:

Filnavne: små bogstaver + \_ (fx ai_bot.astro)
Komponenter: PascalCase (fx ProfileCard.astro)
Billeder: snake_case i .webp-format (fx foredragsraekke1.webp)
Commits: på engelsk i bydeform: add, remove, change, fix, update + hvad
Branches: beskrivende og versionsbaserede (fx menu-v3, about-v4)

## Git branches og ## Arbejdsflow:

Alle arbejder i egne branches navngivet efter funktion (fx scroll-UpcomingEventCard)
Branches merges via pull requests for at sikre versionsstyring og overskuelighed
Commits skal være beskrivende og små – ingen store “fix-all”-commits
Vi undgår konflikter ved at opdele ansvar:
A har fx arbejdet på eventlist, menu, about, singleview osv
B har haft ansvar for index-components, footer osv

## Kode:

CSS: klassenavne bruges til styling (ingen ID’er). Naming convention: kebab-case.
Kommentarer: bruges minimalt
Responsivt design: sikret med @media og clamp() i CSS.
Astro: komponentbaseret struktur med genbrug og lav redundans.

# Dokumentation af props, slots og layouts

Slots bruges primært til fleksibel struktur i fx Layout.astro.
Props sendes mellem komponent og page
Layout.astro bruges som global wrapper og importeres på alle pages:
