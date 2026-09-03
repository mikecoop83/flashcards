# Times Tables

## Project structure

- `index.html` contains the entire app: HTML, CSS, and JavaScript.
- `favicon.ico` and `apple-touch-icon.png` contain the blue multiplication-sign icons. The Apple icon is square; iOS applies its own corner mask.
- `README.md` documents setup, features, and scoring. Update it when user-facing behavior changes.
- Keep the app standalone with no required build step, framework, external dependencies, or backend. Core practice must work when opening `index.html` directly and offline. Voice input may require a supported browser, HTTPS, and a network connection.

## Code map and state

- `newQuestion()` selects and displays a question; `finish()` completes the equation and shows the next-question control.
- `editAnswer()` handles keypad, physical-keyboard, and paste edits. The form's submit handler validates answers and updates scoring; `updateScore()` renders the totals and percentage.
- `parseSpokenNumber()` converts recognized English numbers to digits. Speech callbacks check the active recognition session to ignore stale events; `stopListening()` cancels it.
- `applyTheme()` updates the theme and switch state. Its initialization runs in the document head to avoid flashing the wrong theme.
- Questions, answers, and scores live only in memory and reset on reload. Only the theme preference persists, using the `times-table-theme` key in `localStorage`.
- Use this map to locate relevant code before editing; it does not replace reading that code.

## Current behavior and design

These describe how the app works today, not permanent requirements. Preserve them during unrelated work, but update them when the requested change calls for different behavior or design. Keep this guide aligned with the implementation.

- Questions shuffle all 169 ordered factor pairs from 0–12 before repeating.
- Each question counts once, on its first valid submission. Only first-try correct answers increase the correct count. Invalid input, retries, and answer reveals do not add to the total.
- The percentage appears only when the total is greater than zero.
- The equation keeps its question mark after an incorrect attempt and shows the answer after a correct attempt or reveal.
- The mobile keyboard stays closed. An on-screen number pad provides digits, clear, and backspace; physical keyboard and digits-only paste are also supported.
- Voice input fills the answer without submitting it or selecting the recognized number. The cursor stays at the end.
- Voice capture is canceled on manual edits or question changes, and stale recognition events are ignored. The number pad remains usable when voice input fails.
- The theme initially follows the device and remembers an explicit light/dark choice when storage is available. Unavailable storage does not interrupt practice.
- The name is “Times Tables,” with a blue theme and a white multiplication sign on a blue square.
- The layout is compact and responsive for phones and iPads, with accessible labels, visible keyboard focus, and comfortable touch targets.
- The microphone button sits to the right of the answer input at the same height. “Your answer” is centered over the input alone.
- The light/dark control is a horizontal switch, with reduced-motion support.

## Validation and workflow

- Validate the behavior affected by a change. For logic changes, exercise relevant scoring, retry, reveal, reset, and input paths. For voice changes, check parsing, cancellation, stale events, and error handling.
- Check responsive layout and both themes when changing presentation. Be explicit about whether actual browser/device or microphone testing was performed; mocked checks do not establish real speech-recognition support.
- There is no configured build or test runner. Avoid adding tooling solely for a small change, and avoid timing-dependent tests.
- Commit and push only when requested. The GitHub repository is `mikecoop83/flashcards`, with `main` as the default branch. If switching GitHub accounts for a push, restore the previously active account afterward.
