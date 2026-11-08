# TryHackMe Stats Sync

Fetches my TryHackMe rank, points, streak, rooms and badges every day and writes them into this README and `practice-log.md` using GitHub Actions.

<!-- THM-STATS:START -->
*Waiting for the first sync.*
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
