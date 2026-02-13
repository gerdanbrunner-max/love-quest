# Love Quest

Love Quest is a retro arcade-style browser game with a whimsical fairy-tale narrative.  
Built with vanilla HTML, CSS, and JavaScript, it blends pixel-art aesthetics, interactive storytelling, sound effects, and multi-level quest progression into a playful, story-driven experience.

Designed as a personal interactive adventure, the game combines nostalgia, humor, and cozy romance with arcade-inspired UI.

---

## Live Demo

https://gerdanbrunner-max.github.io/love-quest/

---

## Features

- Prologue + 7 main quests + final screen
- Typewriter storyteller text animation
- Sound effects system:
  - Typing tick (plays during text animation)
  - Shared quest jingle
  - Grand final jingle
  - Correct / incorrect answer chime
- Sound effects enabled by default
- Mobile support:
  - SPACE key continues on desktop
  - Tap anywhere on the main panel continues on mobile
- Themed pixel-art banners per quest
- Floating themed background decorations per quest
- Dynamic ranking system on final screen
- Love Mushroom collection mechanic
- Witch Satisfaction Index tracking
- Retro arcade UI styling with CRT-inspired effects

---

## Gameplay Overview

The player progresses through a sequence of quests to rescue the Princess Wife from the Witch of Long Distance.

Each quest includes:
- A storyteller introduction (animated via typewriter effect)
- A themed banner
- Floating decorative background elements unique to the quest
- A question or challenge
- A reward system (Love Mushrooms)

The final screen summarizes:
- Total Love Mushrooms collected
- Witch Satisfaction Index
- Final rank with custom explanation text

---

## Project Structure

/assets  
  /banners     → Quest header pixel-art banners  
  /deco        → Floating themed decoration elements  
  /sfx         → Sound effects (typing tick, jingles, etc.)  

index.html     → Main game file (HTML, CSS, JS combined)  
README.md  

---

## Banner Naming Convention

assets/banners/

prologue.png  
quest0_gate.png  
quest1_fluorescents.png  
quest2_berlin.png  
quest3_string.png  
quest4_nida.png  
quest5_letter.png  
quest6_flowers_ring.png  
quest7_food.png  
final_home.png  

Banners are:
- Centered
- Responsive
- Contained within the panel
- Scaled appropriately across screen sizes

---

## Decoration System

assets/deco/

Each quest defines its own decorative elements through the theming system.

Decoration logic:
- Assigned per quest
- Positioned dynamically
- Animated with vertical floating effect
- Rendered behind main panel content
- Scaled consistently across all themes

Themes include:
- intro
- quest0
- quest1
- quest2
- quest3
- quest4
- quest5
- quest6
- quest7
- final

---

## Audio Implementation

Audio files are stored in:

assets/sfx/

Includes:
- Typewriter tick
- Quest jingle
- Final grand jingle
- Correct answer sound
- Incorrect answer sound

Audio behavior:
- Sounds unlock on first user interaction
- Typing sound plays during storyteller animation
- Quest jingle plays at start of each quest
- Grand jingle plays on final screen
- Missing audio files will produce 404 errors

Sound effects are enabled by default.

---

## Interaction Logic

Desktop:
- SPACE key advances story and prompts

Mobile:
- Tapping on the main panel advances progression
- Interactive elements (buttons, inputs, options) are ignored
- Unified continue handler prevents double triggers

The on-screen text remains "PRESS SPACE TO CONTINUE" for stylistic consistency.

---

## Deployment

Hosted via GitHub Pages.

Settings:
- Deploy from main branch
- Root directory publishing

Important:
Use relative asset paths:

Correct:
assets/banners/prologue.png

Incorrect:
 /assets/banners/prologue.png

Direct asset URLs:
https://gerdanbrunner-max.github.io/love-quest/assets/...

---

## Technical Notes

- Single-file architecture (index.html)
- Vanilla JavaScript
- No frameworks
- Pixel-art rendering using image-rendering: pixelated
- CRT-inspired visual effects
- Responsive layout for desktop and mobile

---

## License

Personal project. Not intended for commercial use.
