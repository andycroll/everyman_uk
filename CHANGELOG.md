# Change Log
All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

## [1.1.0] - 2026-11-03

### Changed
- Uses cinebase 5.9: performances take the raw `title:`, so audience labels become variants, and series prefixes such as `Met Opera:` become the performance's `event`.

### Fixed
- A partner credit after a dash, such as `Primetime - Presented by Deeper Into Movies`, no longer leaves `Primetime -`.
- An event screening label, such as `Sunrise Event Screening - ` before `The Hunger Games: Sunrise on the Reaping`, is removed.

## [1.0.0] - 2026-10-31

### Added
- `EverymanUk::Cinema.all` and `EverymanUk::Cinema.new(id)` for Everyman's open UK cinemas, read from the theatre list in the everymancinema.com daily build, with addresses, postcodes and `latitude`/`longitude`.
- `EverymanUk::Performance.at(id, from:, to:)`, from one schedule request for the whole range plus one request per 50 films, with booking links, variants, languages, festivals and film years from titles, following cinebase 5.5.
- Built on `cinebase/boxoffice`, the client for Webedia "Movies Pro" websites that Showcase shares.
- Hand-written fixtures, a live shape test that checks real responses without storing them, and GitHub Actions CI and release workflows.
