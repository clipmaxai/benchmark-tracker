# AI Benchmark Tracker 📊

Live AI model benchmark leaderboard tracking performance across MMLU, HumanEval, SWE-Bench, ARC AGI, and more.

## Features

- Dark-theme dashboard with sortable columns
- Filter by provider, search by model name
- Top scores highlighted in green
- Mobile responsive
- Data stored in `data/benchmarks.json` — easily updated via cron

## Deploy to GitHub Pages

1. Push this folder to a GitHub repo
2. Go to Settings → Pages → Source: Deploy from branch (`main`, `/` root)
3. Site is live at `https://<user>.github.io/<repo>/`

## Auto-update Scores

```bash
python scripts/update_scores.py
```

Wire up real sources in the script, then add a cron job:

```bash
0 */6 * * * cd /path/to/benchmark-tracker && python scripts/update_scores.py && git add -A && git commit -m "chore: update scores" && git push
```
