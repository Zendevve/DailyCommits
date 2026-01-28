# DailyCommits

Automated hourly commit tracker using GitHub Actions 🤖

## What This Does

This repository uses GitHub Actions to automatically:
- Create or update a `commit_number.md` file
- Increment the commit counter
- Push changes to the repository every hour (24 commits per day)

## How It Works

The workflow runs on a schedule defined in `.github/workflows/daily_commit.yml`:
- **Default**: Runs every hour, 24 times per day (`cron: '0 * * * *'`)
- **For less frequent commits**: Change the cron to `'0 0 * * *'` for once per day at midnight UTC

## Setup Instructions

1. **Enable GitHub Actions**
   - Go to your repository **Settings** → **Actions** → **General**
   - Under "Workflow permissions", select **Read and write permissions**
   - Save changes

2. **Push the workflow file**
   ```bash
   git add .github/workflows/daily_commit.yml
   git commit -m "Add automated daily commit workflow"
   git push
   ```

3. **Verify it's running**
   - Go to the **Actions** tab in your repository
   - You should see the workflow listed
   - It will run automatically based on the schedule

## Customization

You can customize the workflow by editing `.github/workflows/daily_commit.yml`:
- **Change the schedule**: Modify the `cron` value
- **Change the commit message**: Edit line 31
- **Change the file content**: Modify what gets written to `commit_number.md`

## Why?

- Keeps your GitHub profile active
- Great for testing GitHub Actions
- Fun automation project
- Demonstrates CI/CD concepts

---

*Note: This is an automated repository. Commits are made by GitHub Actions.*
