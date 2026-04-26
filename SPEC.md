# Katana Stroke Accuracy Game - Specification

## Project Overview
- **Name**: Katana Strike
- **Type**: Browser-based accuracy game (single HTML file)
- **Core Functionality**: Player mimics sword cut strokes on canvas within 1 second time limit
- **Target Users**: Casual gamers testing precision/motor skills

## Game Mechanics

### Rounds (4 total)
1. **Horizontal** - Left to right horizontal cut
2. **Vertical** - Top to bottom vertical cut
3. **Right Diagonal** - Top-left to bottom-right diagonal
4. **Left Diagonal** - Top-right to bottom-left diagonal

### Gameplay Flow
1. Show target stroke animation (sword path) for 1.5 seconds
2. Player must click, drag, and release within 1 second to execute stroke
3. Score based on accuracy (0-100) comparing player stroke to target
4. If score >= 70, round cleared; otherwise round failed
5. After 4 rounds, show final score with Retry/Exit buttons

### Scoring
- Compare player stroke start/end points and path to target
- Score calculation: weighted average of endpoint accuracy (60%) + path deviation (40%)
- Clear threshold: 70 points per round

## UI/UX Specification

### Layout Structure
- Full viewport canvas centered
- Header: Game title + current round indicator
- Main area: Canvas (600x500px) with target and player strokes
- Footer: Score display + timer bar

### Color Palette
- **Background**: #0a0a0a (near black)
- **Canvas Background**: #1a1a1a (dark gray)
- **Target Stroke**: #ff4444 (red) with glow
- **Player Stroke**: #00ff88 (neon green) with glow
- **UI Text**: #ffffff (white)
- **Accent**: #ff8800 (orange) for timer
- **Timer Bar**: #ff4444 (red) to #00ff88 (green) gradient

### Typography
- **Font**: "Orbitron", sans-serif (Google Fonts - futuristic)
- **Title**: 28px bold
- **Score/Status**: 20px
- **Instructions**: 16px

### Visual Effects
- Target stroke: animated dash pattern flowing along path
- Player stroke: glowing trail effect
- Hit/miss flash animation on round end
- Smooth timer bar countdown
- Screen shake on miss

### Components
- Start button (initial state)
- Round indicator (Round 1/4, 2/4, etc.)
- Timer bar (1 second countdown)
- Score display per round
- Final score modal with Retry/Exit buttons
- Instruction text overlay

## Acceptance Criteria
1. ✓ Target stroke shows correct direction for each round
2. ✓ Player can click-drag-release to draw within 1 second
3. ✓ Score calculates accurately based on stroke similarity
4. ✓ Clear threshold properly gates progression
5. ✓ All 4 round types work correctly
6. ✓ Final score displays correctly
7. ✓ Retry resets to round 1
8. ✓ Exit shows thank you message