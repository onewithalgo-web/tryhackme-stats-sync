# TryHackMe Stats Sync

Fetches my TryHackMe rank, points, streak, rooms and badges every day and writes them into this README and `practice-log.md` using GitHub Actions.

<!-- THM-STATS:START -->
<!-- Do not edit this section directly; automatically synced by Denali Connect -->
### 🛡️ Live TryHackMe Profile Statistics

<div align="center">
  <a href="https://tryhackme.com/p/ndv.miso" target="_blank">
    <img src="https://tryhackme-badges.s3.amazonaws.com/ndv.miso.png" alt="TryHackMe Profile Badge" width="400" />
  </a>
</div>

<div align="center">
  <img src="https://img.shields.io/badge/Rank-%23N/A-00b4d8?style=for-the-badge&logo=tryhackme&logoColor=white" alt="THM Rank" />
  <img src="https://img.shields.io/badge/Rooms%20Completed-0-e63946?style=for-the-badge&logo=target&logoColor=white" alt="Rooms Completed" />
  <img src="https://img.shields.io/badge/Streak-0%20Days-ffb703?style=for-the-badge&logo=fire&logoColor=white" alt="Current Streak" />
  <img src="https://img.shields.io/badge/Points-0-2a9d8f?style=for-the-badge&logo=counter-strike&logoColor=white" alt="Total Points" />
</div>

#### 📊 Performance Overview

| Platform Metric | Value |
| :--- | :--- |
| 👤 **Hacker Profile** | [**`ndv.miso`**](https://tryhackme.com/p/ndv.miso) |
| 🏆 **Global Rank** | **Unranked** |
| 🔥 **Current Streak** | **0 days** |
| 📦 **Rooms Completed** | **0 rooms** |
| 🎖️ **Badges Earned** | **0 badges** |
| ⭐ **Total Score** | **0 pts** |
| ⚡ **Platform Rank / Tier** | **Active Learner** |
| 🕒 **Last Synchronized** | `2026-11-08 20:25:34 UTC` |

*Automated with [Denali Connect](https://github.com) • Updates daily at 00:00 UTC*
<!-- THM-STATS:END -->

## Setup

1. In **Settings > Secrets and variables > Actions**, add a secret `THM_USERNAME` with your TryHackMe username.
2. Optional: add `THM_SESSION_COOKIE` (your `connect.sid` cookie) for private room history. It grants access to your account, so skip it if unsure.
3. Open the **Actions** tab, choose **TryHackMe Stats Sync**, and click **Run workflow**.

It then runs daily at 00:00 UTC and only commits when something changed.

## Run locally

```bash
pip install -r requirements.txt
python main.py --mock --dry-run          # preview with sample data
python main.py -u YOUR_USERNAME --local  # update README and log on disk
python -m unittest discover tests        # tests
```
