# NoN Agent OS

The growth agents for NoN (getnon.in) and InnovaChem SEO (innovachem.in), set up to run on a schedule with Claude Code.

## How it works

```
Every week:   Ashutosh drops exports in inputs/  (about 5 minutes)
                     |
Scheduled tasks (Claude Code, cloud) run the agents on their own
                     |
Each run writes reports/<date>-<agent>.md and opens pull requests for Brand Brain changes
                     |
Monday plan (operator) tells Ashutosh: top 3 actions + decisions waiting on him
                     |
Ashutosh approves -> he (or Claude, with his OK) makes the change in ShopDeck / Ads Manager
```

Nothing is published, sent or spent without Ashutosh's approval. See `CLAUDE.md`.

## Folders

| Folder | What is in it |
| --- | --- |
| `CLAUDE.md` | Rules every run follows |
| `brand-brain/` | The 7 Brand Brain files: the single source of truth |
| `.claude/skills/` | The 16 agents as Claude Code skills |
| `shared/` | Shared operating contract, evidence, approval and handoff rules |
| `inputs/` | Weekly exports you drop in (orders, Meta ads, reviews) |
| `reports/` | What the agents write |
| `schedules/SCHEDULED-TASKS.md` | The prompts to paste into each scheduled task |
| `agents/`, `claude/` | Earlier run brief and the 23 Nov creative-run summary (reference only; the skills in `.claude/skills/` are the source) |

## One-time setup (about 30 minutes)

1. **Create the repo (Ashutosh).** Sign in to GitHub, click New repository, name it `non-agent-os` and choose **Private**. Then upload this whole folder:
   - Easiest: install GitHub Desktop, add this folder as a repository, and publish it as private.
   - Or drag the folders into "uploading an existing file" on github.com. The `.claude` folder is hidden on Windows, so GitHub Desktop is safer.
2. **Give Priyanka access (Ashutosh).** On the repo, go to Settings, then Collaborators, then Add people, and add Priyanka's GitHub account. Scheduled tasks run under the Claude account that creates them, and that account needs access to the repo.
3. **Connect GitHub to Claude Code (whoever creates the tasks).** At claude.ai/code, connect GitHub and install the Claude GitHub app on the `non-agent-os` repo when asked.
4. **Create the scheduled tasks.** At claude.ai/code/routines, click New. Pick the repo, set the time, paste a prompt from `schedules/SCHEDULED-TASKS.md`, turn on notifications and save. Use **Run now** once on each task to test it.
5. **Optional connectors.** Google Drive, if you'd rather drop exports there than in `inputs/`. A Meta ads connector (Adspirer, Windsor.ai or Supermetrics) removes the weekly Meta export.

## Weekly routine

- **Sunday or Monday morning (Ashutosh, about 5 minutes):** upload the ShopDeck order export (names and phones removed) to `inputs/shopdeck-orders/`. While ads run, also upload the Meta ad-level export to `inputs/meta-ads/`.
- **Monday 8:40-10:20 am:** the scheduled tasks run, and the Monday plan arrives as a notification.
- **Monday or Tuesday (Ashutosh):** read the plan, merge or close the Brand Brain pull requests, and approve or reject the proposed actions.

## Keep in mind

- The repo holds business data (costs, prices). Keep it **private**.
- Order exports can contain customer names and phones. Remove those columns before uploading.
- Scheduled tasks use the Claude plan's usage. Seven tasks, mostly monthly, is light.
- The laptop doesn't need to be on: cloud scheduled tasks run on Anthropic's servers.
