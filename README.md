# GAMELAND

GAMELAND is a responsive, single-page browser arcade starring Pebbles the Penguin. The static site has a 12-game catalog, arcade filters, VIP rewards, and a canvas fallback for games whose standalone page is not present.

**Play:** [sabtyo.github.io/wencher](https://sabtyo.github.io/wencher/)

## What’s here

- Search, categories, tags, popularity/rating/name sorting, trending and new collections, and favorites.
- A points wallet with a 20-game daily earning limit, Pebbles’ happiness, and Gold, Platinum, and Diamond VIP tiers.
- A game player that loads a local game page when available and otherwise starts a built-in canvas fallback.
- A browser-local admin console, panic disguise, and Pebbles Hub.

## Run locally

From the repository root, start a static web server:

```sh
python -m http.server 8000
```

Then open [localhost:8000](http://localhost:8000/). Serving the page over HTTP lets the player check for standalone game pages; opening `index.html` directly may cause the browser to use the canvas fallback instead.

## Repository layout

```text
wencher/
├── index.html      # GitHub Pages entry point and application
├── README.md       # Project overview and local run instructions
└── CHANGELOG.md    # Versioned release notes
```

The catalog references optional game pages under `games/` (for example, `games/hextris/index.html` and `games/2048/index.html`). Those game bundles are not included in this repository yet. The page keeps its catalog URLs and provides a playable canvas fallback when a referenced page is unavailable.

## Browser data and scope

The site is a static front end with no server-side account or save service. The guest profile, points, VIP tier, favorites, and Pebbles’ happiness are stored in this browser’s `localStorage` under `gameland_users_db`; they do not sync across browsers or devices. The admin gate and console are client-side demonstration features, not secure authentication or shared moderation.

See [CHANGELOG.md](CHANGELOG.md) for release history.
