# Hello Charu

A small Python project that prints a greeting and the current date.

Run it with:

```bash
python main.py
```

## Daily email with GitHub Actions

The `Daily greeting` workflow runs `main.py` every day at 00:00 UTC and emails
its output. It can also be started manually from the repository's **Actions**
tab.

Add these repository actions secrets under **Settings → Secrets and variables
→ Actions**:

- `GMAIL_USERNAME`: the Gmail address used to send the email.
- `GMAIL_APP_PASSWORD`: a Google app password for that account (requires
  2-Step Verification; do not use your regular Gmail password).
- `EMAIL_TO`: the destination email address.

The workflow sends through Gmail's SMTP server over SSL. Scheduled runs may be
delayed during periods of high GitHub Actions load.
