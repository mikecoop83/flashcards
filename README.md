# Times Table Club

A standalone, responsive webpage for practicing multiplication with numbers from 0 through 12. Works on phones, tablets, and desktops, including offline.

## Getting started

Download or clone this repository and open `index.html` in a browser. No installation, build step, or server is required.

## Features

- Randomized questions covering all 169 factor pairs from 0–12 before repeating.
- Digits-only answer input with a numeric keyboard on mobile devices.
- Correct answers out of total questions, plus a percentage once you’ve answered a question.
- Unlimited retries or the option to reveal the answer after a mistake.
- Blue light and dark themes with a horizontal switch. Initially follows your device’s theme and remembers your selection when browser storage is available.
- A **Start fresh** button to reset your score and shuffle the questions.

## Scoring

Each question counts once, on the first valid answer. Only answers correct on the first try increase the correct count. Retrying or revealing an answer does not change that question’s score. Empty or invalid answers do not count.

Practice scores reset when the page is reloaded.

## Editing

All HTML, CSS, and JavaScript live in `index.html`. Edit the file and refresh your browser to see changes. There are no external dependencies.
