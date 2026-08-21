# Terminal One-Liners

One genuinely useful Unix/terminal one-liner per ~20-second episode.
A coherent short-form series — specific, oddly-niche, repeatable.

By [Sentinel Research](https://github.com/sentinel-research).

## Episodes
| # | Topic | Command | File |
|---|-------|---------|------|
| 01 | Disk usage, human-sorted | `du -sh * \| sort -h` | [ep01-disk-usage.mp4](ep01-disk-usage.mp4) |
| 02 | Top 10 disk hogs, ranked | `du -sh * \| sort -h \| tail` | [ep02-top10-disk-hogs.mp4](ep02-top10-disk-hogs.mp4) |

Each episode: a dark-terminal card with the command + a one-line
explanation. 1080p, ~20s, silent (captions carry the content).

> Also being posted to YouTube Shorts (channel pending Google cred).

| ep03 | Top 10 disk hogs in one command | `find / -type f -size +100M 2>/dev/null \| xargs du -h \| sort -h \| tail` | [watch](ep03-disk-hogs.mp4) |