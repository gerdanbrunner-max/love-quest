# Love Quest: The Snatching of the Queen of Mushrooms

Love Quest is a single-page, static web application built as a retro-inspired narrative quiz game. The project combines an 8-bit aesthetic with structured game logic to create a level-based interactive experience. The application is fully client-side and requires no external libraries, frameworks, or backend services.

## Overview

This project is a browser-based interactive game structured around six progressive levels. The player completes a series of narrative-driven trials to unlock achievements and reach the final screen.

Core features include:
- Intro story and rules screen
- Password-protected entry (client-side validation)
- Six quiz-based levels with mixed input types
- Achievement overlay after each completed level
- Persistent retro-style HUD displaying level, collected items, and mistakes
- Dynamic UI feedback and sound effects
- Performance-based ranking logic

## Technology Stack

- HTML5
- CSS3
- Vanilla JavaScript (ES6+)
- Web Audio API (for sound effects)

The project is implemented as a single `index.html` file containing markup, styling, and scripting. No build tools, frameworks, or package managers are required.

## Architecture

The application follows a simple state-driven UI model.

Global state tracks:
- Current level
- Love Mushrooms collected
- Mistake count
- Unlock status (stored in `localStorage`)

Screens are conditionally rendered based on state:
- Intro screen
- Password gate
- Levels 1–6
- Achievement overlays
- Final victory screen

Input handling supports:
- Single-choice multiple selection
- Multi-select validation (exact match required)
- Free-text input with case-insensitive comparison and whitespace trimming

All validation is handled client-side.

## HUD and UI Behavior

A fixed top HUD displays:
- Current level (1–6)
- Love Mushrooms collected
- Witch Satisfaction (mistakes counter)

The HUD updates dynamically as the game state changes.

A persistent character element (the Witch) is anchored in a screen corner and generates contextual speech bubble messages based on:
- Incorrect answers
- Achievement unlocks
- Random timed intervals during active levels

## Audio Implementation

Sound effects are generated using the Web Audio API:
- Incorrect answer tone
- Correct answer chime
- Achievement unlock sound
- Final victory sound

No background music is included.

## File Structure

/
├── index.html  
└── README.md  

All functionality is embedded within `index.html`.

## Deployment

The project is deployed using GitHub Pages.

Deployment steps:
1. Push `index.html` to the `main` branch.
2. Enable GitHub Pages in repository settings:
   - Source: Deploy from branch
   - Branch: main
   - Folder: root
3. Access the deployed application at:
   https://<username>.github.io/<repository-name>/

## Local Development

No setup is required.

To run locally:
- Download the repository
- Open `index.html` in a modern browser

Ensure the HTML file includes:
<meta charset="UTF-8">

This is required for proper rendering of non-ASCII characters.

## Ranking Logic

Final rank is determined by total mistakes:

0–2: Love Legend  
3–5: Certified Haban  
6–9: Chaotic but Adorable  
10+: Witch’s Favorite  

## License

This project is a private personal application and is not distributed under a public license.
