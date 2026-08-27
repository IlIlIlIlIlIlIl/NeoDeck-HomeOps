# Development

Upstream: <https://github.com/justynroberts/NeoDeck>

- Target hardware: LilyGo T-Deck Plus
- Build: `pio run`
- Keep `main` buildable; make changes on `feature/<name>` branches.
- Sync with upstream using `git fetch upstream`, `git checkout main`,
  `git merge upstream/main`, and `git push origin main`.

## Nordic terminal display test

After flashing and opening an SSH session, run:

```sh
printf 'åäö ÅÄÖ\n'
printf 'Hyvää päivää\n'
printf 'yö myöhään\n'
printf 'Eemilillä läksyjä\n'
printf '\033[31mHyvää päivää\033[0m\n'
printf '\033[32mÅÄÖ åäö\033[0m\n'
```

Confirm that each Nordic character occupies one cell, colors and adjacent ASCII
remain correct, and a Powerline-enabled prompt still renders its symbols.
Keyboard input for Nordic characters is intentionally out of scope.
