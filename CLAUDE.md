# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A standalone Minesweeper game implemented as a single HTML file with embedded CSS and JavaScript. No build system or dependencies required.

## Running the Game

Open `minesweeper.html` directly in a web browser. No build, install, or server needed.

## Architecture

Single-file design (~1,300 lines) with two main JavaScript classes:

### SoundSystem Class
- Manages audio using Web Audio API with procedural sound generation
- Sound types: click, reveal, flag, unflag, explosion, win, chord, hint
- Lazy initialization with toggle support

### Minesweeper Class
Core game engine handling:
- **State**: 2D arrays for board, revealed/flagged/questioned cells, game flags
- **Game logic**: Mine placement (first-click safe zone), flood-fill reveal, win detection
- **Input**: Mouse (left-click reveal, right-click flag, double-click chord) and keyboard (arrows navigate, Space/Enter reveal, F flag, R restart, H hint)
- **Hint system**: Deduces safe cells and definite mines; falls back to random safe cell
- **Persistence**: Statistics stored in localStorage per difficulty

### Difficulties
| Level | Grid | Mines |
|-------|------|-------|
| Easy | 9x9 | 10 |
| Medium | 16x16 | 40 |
| Hard | 16x30 | 99 |

## Key Implementation Details

- **Mine placement**: Random with collision detection, excludes 3x3 area around first click
- **Win condition**: All non-mine cells revealed (auto-flags remaining mines)
- **localStorage keys**: `minesweeper_easy`, `minesweeper_medium`, `minesweeper_hard` storing `{played, won, bestTime}`
- **PWA support**: Service worker and manifest generated dynamically at runtime

## Technologies

Vanilla HTML5/CSS3/JavaScript (ES6+), Web Audio API, CSS Grid, localStorage, Service Workers
