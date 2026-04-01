Create a self-contained HTML web game for children aged 8–10 to practice math skills.
The game should be fully playable in a single HTML file (inline CSS and JS, no external dependencies).
                                                                                                                                                                                            
Gameplay & Content
- Filename: index.html
- Application language selection: Hebrew (default), English
  - When language is Hebrew then make sure that the exercise/operations/values are from left to right
- Cover core math operations: addition, subtraction, multiplication, division
- In the opening screen the user can select:
  - The min (default=1) and max (default=10) numbers to use in the operations. Negative numbers are allowed.
  - The available operations to use.
  - Add a checkbox on the start screen if to allow subtraction result lower than 0. This checkbox will be enabled only if 'subtraction' opoeration is selected.
- Questions presented one at a time with multiple-choice answers (4 options)
- Include a score counter and a progress bar or level indicator
- Subtraction:
  - Do not generate questions that substruct a zero.
  - Do not generate questions of a number aubstracting same number.
- Do not repeat questions, unless answer previously failed.
- For a failed answer, wait 3 seconds befor moving to next question.
- On the side of the page, there shall be an image of a racing track and a red-filled circle at the begining of the track.
  - For a correct answer, the user will advance the character to next point in the track.
  - For a wrong answer, the user will get back to the previous point, but no further back than the starting point.
  - Total points on the track: 10
  - The game ends only when the user reaches the last point on the track.

UI / UX Requirements
- Large, readable font (minimum 18px body, 28px+ for math questions)
- High-contrast color scheme — bright but not garish (e.g., white background, navy text, colorful accent buttons)
- Buttons must be large and touch-friendly (min 48×48px tap targets), suitable for tablets and mouse
- Friendly, rounded design language — rounded corners, soft shadows, no harsh edges
- Celebratory feedback on correct answers (e.g., green flash, star emoji, short encouraging message like "Great job!")
- Gentle feedback on wrong answers (e.g., red shake animation, "Try again!" — never harsh or discouraging)
- Animated transitions between questions (slide or fade)
- Sound feedback using the Web Audio API (no external files):
  - Correct answer: short upbeat chime (ascending tones)
  - Wrong answer: low soft "boing" or descending tone (gentle, not startling)
  - Level up / streak milestone: brief fanfare sequence
  - Button click: subtle tick sound for tactile feel
  - Mute toggle button visible on all screens so the child (or parent) can silence audio.
    Place this button in the right-top corner of the form.
- A simple start screen with the child's name input (Default=Spiderman), and a "Play!" button
- A results screen at the end showing score, stars earned (1–3), and a "Play Again" button
- Questions presented as a "Hive" like, each with outline to distinguish between the options.

Accessibility
- Keyboard navigable (Tab + Enter to select answers)
- No time pressure by default (optional countdown timer checkbox on the start screen)
- Avoid flashing/strobing animations