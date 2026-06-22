# Daily Job Digest

Automated job search assistant that runs on GitHub Actions and emails a daily digest every morning.

---

## Setup: Add GitHub Secrets

Go to your repo on GitHub:

**Settings → Secrets and variables → Actions → New repository secret**

Add these three secrets:

| Secret name | What to paste |
|---|---|
| `GMAIL_USERNAME` | Your full Gmail address — e.g. `you@gmail.com` |
| `GMAIL_APP_PASSWORD` | Your Gmail App Password (see below) |
| `RECIPIENT_EMAIL` | The email address where you want the digest delivered |

---

## How to get a Gmail App Password

`GMAIL_APP_PASSWORD` is **not** your Gmail login password.

1. Go to [myaccount.google.com](https://myaccount.google.com)
2. Security → 2-Step Verification (must be enabled)
3. Scroll to the bottom → **App passwords**
4. Choose app: **Mail** / Device: **Other** (name it anything)
5. Click **Generate** — copy the 16-character code
6. Paste that code as the value of `GMAIL_APP_PASSWORD`

---

## Running manually

Once secrets are added, go to **Actions → Daily Job Digest → Run workflow** to trigger a test run immediately without waiting for the scheduled time.

The digest runs automatically every day at **07:00 UTC** (08:00 BST in summer).
