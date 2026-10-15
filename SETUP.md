# SETUP.md — GitHub Profile README Setup Guide

> Complete setup instructions for the `Sxrxya` special profile repository.

---

## 1. Create the Special Profile Repository

GitHub renders a special `README.md` when you create a **public repository whose name exactly matches your username**.

1. Go to [https://github.com/new](https://github.com/new)
2. Set **Repository name** to exactly: `Sxrxya`
3. Set visibility to **Public**
4. Do **not** initialize with a README (you will push the files yourself)
5. Click **Create repository**

---

## 2. Push the Files

From the `Sxrxya/` folder on your machine, run:

```bash
git init
git add .
git commit -m "feat: add premium GitHub profile README"
git branch -M main
git remote add origin https://github.com/Sxrxya/Sxrxya.git
git push -u origin main
```

After this, visit [https://github.com/Sxrxya](https://github.com/Sxrxya) — your profile page will display the README automatically.

---

## 3. Enable GitHub Actions

1. Go to your repository: `https://github.com/Sxrxya/Sxrxya`
2. Click the **Actions** tab
3. If prompted, click **"I understand my workflows, go ahead and enable them"**

---

## 4. Run the Snake Workflow

The contribution snake animation requires a one-time manual trigger:

1. In your repository, go to **Actions → Generate Contribution Snake**
2. Click **Run workflow → Run workflow** (green button)
3. Wait ~60 seconds for the job to complete
4. The workflow will create an `output` branch and publish:
   - `github-contribution-grid-snake.svg` (light mode)
   - `github-contribution-grid-snake-dark.svg` (dark mode)

After a successful run, the snake animation in your README will display correctly.

> ⚠️ **The snake image will appear broken until the workflow runs successfully at least once.**  
> This is expected — it is not a bug in the README.

---

## 5. Verify the Generated SVG

After the workflow completes, verify the image is accessible:

- Light: `https://raw.githubusercontent.com/Sxrxya/Sxrxya/output/github-contribution-grid-snake.svg`
- Dark: `https://raw.githubusercontent.com/Sxrxya/Sxrxya/output/github-contribution-grid-snake-dark.svg`

Open each URL in your browser. You should see an animated snake SVG over your contribution graph.

---

## 6. Troubleshooting Broken Images

| Symptom | Likely Cause | Fix |
|---|---|---|
| Snake image is broken | Workflow has not run yet | Trigger the workflow manually (Step 4) |
| Snake image is broken after workflow ran | `output` branch not created | Check Actions logs for errors; re-run if needed |
| Stats widgets show 0 / blank | GitHub API rate-limited | Wait a few minutes and hard-refresh |
| Streak widget broken | `demolab.com` service temporarily down | Wait and refresh; no action needed |
| Typing SVG not animating | Cached static image | Hard-refresh (`Ctrl+Shift+R`) |
| Profile README not showing on profile | Repository is private or named incorrectly | Ensure repo name is exactly `Sxrxya` and is **Public** |

---

## 7. External Widgets — Third-Party Dependencies

The following elements in your README depend on external services:

| Widget | Service | URL |
|---|---|---|
| Animated Header Banner | capsule-render.vercel.app | [source](https://github.com/kyechan99/capsule-render) |
| Typing SVG | readme-typing-svg.demolab.com | [source](https://github.com/DenverCoder1/readme-typing-svg) |
| Profile View Counter | komarev.com/ghpvc | [source](https://github.com/antonkomarev/github-profile-views-counter) |
| GitHub Stats | github-readme-stats.vercel.app | [source](https://github.com/anuraghazra/github-readme-stats) |
| Top Languages | github-readme-stats.vercel.app | [source](https://github.com/anuraghazra/github-readme-stats) |
| Streak Counter | streak-stats.demolab.com | [source](https://github.com/DenverCoder1/github-readme-streak-stats) |
| Contribution Snake | Platane/snk (self-hosted via Actions) | [source](https://github.com/Platane/snk) |

> All third-party services are free and community-maintained. They may occasionally experience downtime.

---

## 8. Update Project Repository Links

The project cards in the README use the following repository links. If your actual repository names differ, update the links in `README.md`:

| Project | Expected URL |
|---|---|
| DocuMind-AI | `https://github.com/Sxrxya/DocuMind-AI` |
| Cognitive Agent Platform | `https://github.com/Sxrxya/Cognitive-Agent-Platform` |
| AEGIS Disaster AI | `https://github.com/Sxrxya/AEGIS-20AI-20DISASTER` |
| Cleara API | `https://github.com/Sxrxya/Cleara-API` |
| HireSense AI | `https://github.com/Sxrxya/HIRESENSE-AI` |
| Gojan AI Voice Assistant | `https://github.com/Sxrxya/Gojan-AI-Voice-Assistant` |

---

## 9. Publish Checklist

- [ ] Repository `Sxrxya` created as **public** on GitHub
- [ ] Files pushed to `main` branch
- [ ] Profile README visible at `https://github.com/Sxrxya`
- [ ] GitHub Actions enabled in the repository
- [ ] Snake workflow triggered manually and completed successfully
- [ ] `output` branch created with snake SVGs
- [ ] Snake animation visible in the README
- [ ] All project repository links verified and updated if needed
- [ ] Stats widgets loading (may take a few minutes after first push)
