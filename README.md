# Weekly To-do

A playful single-page weekly todo app where completed tasks break into falling letters. The letters can be pushed around with a desk fan, pulled into a vacuum, or swept into a tornado and trash bin.

Live site: https://lingdad.github.io/todo-app

## Features

- Add tasks from the input field or by pressing Enter.
- Complete a task by clicking its round checkbox.
- Edit each task from the button on the right side of the row.
- Break a task into a second-level checklist, one item per line.
- Complete every subtask to automatically complete the main task.
- Export completed and open tasks as a weekly Markdown file.
- Watch completed task text scatter into animated letter particles.
- Use the floating tool launcher to activate:
  - Fan: blows settled letters across the screen.
  - Vacuum: pulls letters into the nozzle.
  - Tornado: swirls letters and can drop them into the trash bin.
- Sound effects are generated with the Web Audio API.
- Tasks are saved in the browser with `localStorage`.
- Main tasks and subtasks are stored together in the browser.
- Completed weekly tasks are saved as Markdown data in the browser and downloaded from the export button.

## Project Structure

```text
.
├── index.html   # HTML, CSS, and JavaScript for the app
└── README.md
```

This project intentionally keeps everything in `index.html`, with no build step and no external runtime dependencies.

## Run Locally

Open `index.html` directly in a browser:

```bash
open index.html
```

You can also serve the folder with any static file server:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy

The app is designed for GitHub Pages. Push changes to `main`, then GitHub Pages serves the static `index.html` file at:

https://lingdad.github.io/todo-app

## Notes

- The sample tasks are only added the first time the app runs in a browser.
- The visual effects can create many letter particles during long sessions, so performance may depend on browser and device speed.
- Audio starts after user interaction because browsers limit autoplaying sound.
