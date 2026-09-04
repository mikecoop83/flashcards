# Times Tables

A standalone, responsive webpage for practicing multiplication with numbers from 0 through 12. Works on phones, tablets, and desktops, including offline.

## Getting started

Download or clone this repository and open `index.html` in a browser. No installation, build step, or server is required.

## Features

- Randomized questions covering all 169 factor pairs from 0–12 before repeating.
- Compact on-screen number pad with clear and backspace, without opening the mobile keyboard. Physical keyboard input and digit-only paste are also supported when the answer field is focused.
- The number pad and microphone stay visible but disabled after a correct answer or reveal, keeping the controls in place until the next question.
- Correct answers out of total questions, plus a percentage once you’ve answered a question.
- Unlimited retries or the option to reveal the answer after a mistake.
- Blue light and dark themes with a horizontal switch. Initially follows your device’s theme and remembers your selection when browser storage is available.
- A **Reset score** button to the right of the score, with a confirmation prompt before clearing your score and shuffling the questions.

## Voice input

Tap **Speak answer**, allow microphone access, and say a number in English (for example, “fifty-six”). The recognized number fills the answer field; review it and tap **Check answer** yourself. Tap **Stop listening** to cancel.

Voice input uses the browser’s speech recognition service and may send audio to that service. Browser support varies and an internet connection may be required. Use an HTTPS-hosted copy for mobile testing. The number pad remains available if voice input is unsupported or microphone access is denied.

## Scoring

Each question counts once, on the first valid answer. Only answers correct on the first try increase the correct count. Retrying or revealing an answer does not change that question’s score. Empty or invalid answers do not count.

Your score is saved in this browser and restored when you reload or return. Choose **Reset score** to reset the saved score and shuffle the questions. Each visit starts with a new question. If browser storage is unavailable, you can still practice, but your score will only last until you reload.

## Editing

All HTML, CSS, and JavaScript live in `index.html`. Edit the file and refresh your browser to see changes. There are no external dependencies.
