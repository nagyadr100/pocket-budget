# Pocket Budget

A personal monthly budget tracker I use on my phone. One file (`index.html`) with HTML, CSS and JavaScript. Data is saved in the browser with `localStorage`. Hosted for free on GitHub Pages and added to my phone's home screen.

## About me

I'm a complete beginner at coding and I'm learning JavaScript while building this. You do most of the building, but I want to understand everything you change. Explain things in plain language and don't assume I know any terms.

## How to work with me

1. **Plan first.** Before changing code, explain your plan in a few bullet points and wait for my OK.
2. **Small steps.** One feature or fix at a time. Don't refactor or "clean up" things I didn't ask about.
3. **Explain after.** After every change, summarize what you changed and why, in beginner terms. Point out which basic concept it uses: variables, if/else, functions, arrays, objects, loops, or the DOM.
4. **Hint mode.** If I say "hint", don't write the code. Give me hints and let me try it myself, then review what I wrote.
5. **Commit and push.** After I confirm a change works, commit with a clear message in plain English and push to `main` so the live site updates.

## Rules for the code

- **One file, no build tools.** Keep everything in `index.html`. No frameworks (React etc.), no npm packages, no backend, no build step. It must work by just opening the file in a browser.
- **Never lose my data.** The storage key is `pocket-budget-v1`. If the saved data format changes, write code that upgrades the old data instead of resetting it. Never clear storage without asking me.
- **Phone first.** It must work well on a phone screen (about 400px wide) in both light and dark mode.
- **Keep the structure.** Follow the existing pattern: all data lives in `state`, every change calls `save()` then `render()`, and `render()` rebuilds the screen from `state`. Keep the five numbered comment sections and beginner-friendly comments.
- **Money.** Currency is euros, formatted with `Intl.NumberFormat("es-ES", ...)`. Accept both `12,50` and `12.50` as input. Round amounts to cents.
- **Check your work.** After a change, check that the page has no JavaScript errors and that adding, deleting and switching months still work.

## Roadmap (in order)

1. **Backup:** an "Export" button that shows all my data as text I can copy, and an "Import" box that restores it. Ask before overwriting existing data.
2. **Recurring expenses:** rent and subscriptions get added automatically each month, without creating duplicates.
3. **Monthly chart:** total spending per month for the last 6 months, with a simple hand-drawn SVG chart (no chart library).
4. **Savings goals:** set a goal (for example, a trip) with a target amount and date, log deposits, and show progress and how much I need to save per month.

## Deployment

GitHub Pages serves `index.html` from the root of the `main` branch. Pushing to `main` updates the live site within a few minutes.
