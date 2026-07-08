# Version control & deployment guide

Your repo is already initialized with a first commit. Here's the workflow from here.

## The one-time setup (publishing to GitHub)

Because the folder is named `haleyeidem.github.io`, GitHub treats it as your **user site** — it deploys automatically to `https://haleyeidem.github.io/` with zero configuration.

1. Go to https://github.com/new
2. Repository name: **haleyeidem.github.io** (must match exactly)
3. Keep it **Public**, don't add a README (you already have one)
4. Then in Terminal:

```bash
cd ~/Projects/haleyeidem.github.io
git remote add origin https://github.com/haleyeidem/haleyeidem.github.io.git
git push -u origin main
```

5. Wait ~1 minute. Your site is live at https://haleyeidem.github.io/

(Your shot-forest site stays at `haleyeidem.github.io/shot-forest` — project sites and the user site coexist.)

## The everyday loop

Every time you change something:

```bash
cd ~/Projects/haleyeidem.github.io
git status                      # see what changed
git add .                       # stage everything
git commit -m "describe the change"
git push                        # publish — site updates in ~1 min
```

That's it. Three commands: `add`, `commit`, `push`.

## Useful extras

```bash
git log --oneline        # history of your commits
git diff                 # see unstaged changes line by line
git restore index.html   # undo uncommitted changes to a file
```

## Good commit message habits

Short, present tense, says what changed: `add dills screenshots`, `rewrite odonata copy`, `fix mobile timeline overflow`.

## When you add the Dill screenshots

```bash
git add assets/
git commit -m "add dills litter log screenshots"
git push
```
