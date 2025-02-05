# ColorRoulette

## Overview
ColorRoulette is an Arduino-based LED game that follows a sequence of LED patterns based on user input. The game consists of different rounds, where players interact with buttons to control LED sequences.

## Components
- Arduino board
- 12 LEDs (3 per color: Red, Yellow, Blue, Green)
- 2 push buttons (Play and Reset)
- 1 buzzer
- Resistors (220Ω each for LEDs)

## Pin Configuration
| Component       | Arduino Pin |
|---------------|------------|
| Red1         | 2  |
| Red2         | 6  |
| Red3         | 10 |
| Yellow1      | 3  |
| Yellow2      | 7  |
| Yellow3      | 11 |
| Blue1        | 4  |
| Blue2        | 8  |
| Blue3        | 12 |
| Green1       | 1  |
| Green2       | 5  |
| Green3       | 9  |
| Buzzer       | 13 |
| Play Button  | A1 |
| Reset Button | A0 |

## Features
- **Round 1:** LEDs light up in sequence (Red → Yellow → Blue → Green). The user presses the Play button to select a color, and the selected LED is stored in `ResultGameOne`.
- **PerColor Mode:** LEDs of the same color light up together (e.g., all Red LEDs, then all Blue LEDs, etc.).
- **PerCircle Mode:** LEDs light up in a circular order with a delay of 200ms in the pattern (Circle 1 → Circle 2 → Circle 3 → Circle 2 → Circle 1), repeating three times.
- **Reset Mode:** When the Reset button is pressed, random LED patterns are displayed (e.g., `RedOnlyLights`, `Spiral`, `OuterFirst`), which continue until the Play button is pressed to start the game.

## Setup
1. Connect the components according to the pin configuration.
2. Upload the Arduino code to your board.
3. Power on the Arduino.
4. Press the Play button to start the game.
5. Press the Reset button to display random LED patterns until a new game starts.

## Code Structure
- `setup()`: Initializes all pin modes.
- `loop()`: Manages game logic and button interactions.
- `round1()`: Handles the first round LED sequence and stores user selection.
- `PerColor()`: Lights up all LEDs of the same color in sequence.
- `PerCircle()`: Implements the circular lighting pattern.
- `resetPattern()`: Displays random LED patterns when the game is reset.

## Notes
- All LEDs use 220Ω resistors to maintain uniform brightness.
- The game logic can be extended to include additional rounds and challenges.

## Future Enhancements
- Adding more complex LED sequences.
- Implementing a scoring system.
- Using an LCD display for feedback.

---
### Created by: [Your Name/Team Name]
