# kish-ping

Keeps the free-tier analytics API awake: GitHub Actions hits `/health` every
5 minutes so Render never spins the service down (its internal scheduler
handles snapshots + auto-reply scans). A weekly heartbeat commit keeps the
scheduled workflow from being auto-disabled after 60 days of repo inactivity.
