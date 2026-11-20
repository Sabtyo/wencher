# Changelog

Notable changes to GAMELAND are documented here.

## [1.0.0] - 2026-11-19

First semantic-versioned release of the current GAMELAND static site. The previously published legacy `Web` release and tag remain unchanged.

### Added

- A responsive, single-page arcade with a 12-item catalog, search, category and tag filters, sorting, trending/new collections, and favorites.
- VIP shop tiers, wallet and daily earning limit, Pebbles’ happiness and feeding, and the Pebbles Hub.
- A player view that loads a referenced local game page when available and otherwise provides a canvas fallback.
- A client-side admin console, panic disguise, and fullscreen game player.
- A root README with project layout, local preview instructions, and an explanation of the site’s browser-local data model.

### Preserved

- The GitHub Pages entry point remains `index.html`, and catalog game URLs retain their `games/.../index.html` paths.
- Existing browser profile storage continues to use the `gameland_users_db` localStorage key and the established user fields.
