# Minesweeper

A classic Minesweeper game that works on both desktop and mobile browsers.

**Play now: https://bahree.github.io/minesweeper/**

## How to Play

The goal is to reveal all cells that don't contain mines. Numbers indicate how many mines are adjacent to that cell.

### Desktop Controls

| Action | Control |
|--------|---------|
| Reveal cell | Left-click |
| Flag/unflag mine | Right-click |
| Chord (reveal adjacent) | Double-click on number, or middle-click |
| Navigate | Arrow keys |
| Reveal (keyboard) | Space or Enter |
| Flag (keyboard) | F |
| Restart | R |
| Hint | H or click Hint button |

### Mobile/Touch Controls

| Action | Control |
|--------|---------|
| Reveal cell | Tap |
| Flag/unflag mine | Long-press (~300ms) |
| Chord (reveal adjacent) | Double-tap on revealed number |

## Features

- Three difficulty levels: Easy (9x9), Medium (16x16), Hard (16x30)
- Responsive design that adapts to any screen size
- Touch-friendly controls for mobile devices
- Hint system that uses logic to find safe cells
- Sound effects (can be muted)
- Statistics tracking (games played, win rate, best time)
- Works offline (PWA support)

## Cheat Codes

Type these on your keyboard after starting a game:
- `xyzzy` - Toggle mine visibility
- `panda` - Toggle mine visibility

## Technologies

Pure HTML/CSS/JavaScript - no dependencies or build steps required.
