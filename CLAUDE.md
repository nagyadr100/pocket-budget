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

1. **Edit an expense:** tap an expense in the list to change its amount, category, date or note, instead of deleting and re-adding it.
2. **Spanish in Quick add:** understand Spanish words too, like `ayer` (yesterday), `hoy` (today), `lunes`…`domingo` (weekdays), and category words like `comida` or `cena`. Good one to try in hint mode.
3. **Category breakdown:** for the month on screen, a simple hand-drawn SVG chart showing which categories the money went to (no chart library).
4. **Merge restore:** a second Restore option that adds the expenses from a backup that are missing, instead of replacing everything. Makes moving data between phone and laptop safe. Ask before changing any data.
5. **Spreadsheet export:** a button that gives my expenses as CSV text I can paste into Google Sheets or Excel.
6. **AI extras (optional, decide later):** use my own Claude API key (stored only on my device, never in the code) to read a receipt photo into the Add expense form, or to give a short plain-language review of my month. Always let me check before anything is saved, and only send the data the feature needs.

## Done

- Backup: copy all data as text, restore it (replaces everything, asks first, with Undo).
- Monthly expenses: added automatically at the start of each month, without duplicates.
- 6-month chart: spending per month with a budget line; tap a bar to jump to that month.
- Quick add: type "lunch 12,50 yesterday" and the form fills itself in (no AI).
- Savings goals: target and date, deposits and withdrawals, how much to save per month.

The saved data (key `pocket-budget-v1`) holds `budgets`, `expenses`, `recurring` and `goals`. Older saved data or backups may be missing the newer lists, so always treat a missing list as empty.

## Deployment

GitHub Pages serves `index.html` from the root of the `main` branch. Pushing to `main` updates the live site within a few minutes.
