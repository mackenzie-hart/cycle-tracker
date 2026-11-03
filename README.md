# Cycle Planner

A single-page planner and habit tracker that follows your menstrual cycle. It works out your phase for any day from your period start dates, then shows phase-based suggestions for energy, movement, food, rest, work, and social life. You log a daily check-in, and the Patterns tab compares what you log with the guide.

Phase guidance describes general patterns and gentle suggestions, not rules or medical advice.

## Use it

Open the site, go to **Cycle**, and add your recent period start dates. Two or three is enough for the planner to start learning your cycle length. Everything you enter is saved in your own browser (localStorage). There is no server, account, or tracking, and nothing is sent anywhere.

Because data lives in the browser, it is separate for each browser and device. Use **Export backup** and **Import backup** on the Cycle tab to keep a copy or move to another device.

## Publish with GitHub Pages

1. Push this repository to GitHub.
2. In the repository, open Settings, then Pages.
3. Under Build and deployment, choose Deploy from a branch, pick `main` and `/ (root)`, and save.
4. After a minute the site is live at `https://<your-username>.github.io/<repository-name>/`.

Do not commit your own period dates or backups to a public repository. The site starts empty on purpose.

## Edit it

Everything is in `index.html`, with no build step.

- `PHASES` in the script holds the phase guide text and the one-line focus for each phase.
- The `:root` block at the top of the stylesheet holds the colors, with a dark-mode variant below it.
- `phaseFor` holds the phase rules (menstrual, follicular, ovulatory, early luteal, late luteal) based on cycle length and period length.
- `defaults()` holds the starting settings, including habit names.
