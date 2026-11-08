# TryHackMe Stats Sync

Fetches my TryHackMe rank, points, streak, rooms and badges every day and writes them into this README and `practice-log.md` using GitHub Actions.

<!-- THM-STATS:START -->
### TryHackMe: [ndv.miso](https://tryhackme.com/p/ndv.miso)

Capability score **42** · Silver league · Top 9% · Highest streak 13 days · **9 rooms completed**

| Room | Difficulty | Time |
| :--- | :--- | :--- |
| [Linux Fundamentals Part 1](https://tryhackme.com/room/linuxfundamentalspart1) | Info | 20 min |
| [SQL Injection](https://tryhackme.com/room/sqlinjectionlm) | Medium | 30 min |
| [Careers in Cyber](https://tryhackme.com/room/careersincyber5zy1sk0al) | Info | 10 min |
| [Inside a Computer System](https://tryhackme.com/room/insideacomputer) | Easy | 45 min |
| [Defensive Security Intro](https://tryhackme.com/room/defensivesecurityintroezn39) | Info | 15 min |
| [Search Skills](https://tryhackme.com/room/searchskillscS) | Easy | 15 min |
| [AI Threat Modelling Assessment](https://tryhackme.com/room/aithreatmodellingassessment) | Easy | 15 min |
| [Offensive Security Intro](https://tryhackme.com/room/offensivesecurityintroc101) | Easy | 15 min |
| [Defensive Security Intro (interactive)](https://tryhackme.com/room/defensivesecurityintroexp) | Easy | 10 min |

*Manual snapshot taken 2026-11-08. TryHackMe blocks automated requests, so this does not update itself.*
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
