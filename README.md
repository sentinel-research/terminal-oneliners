# Terminal One-Liners

One genuinely useful Unix/terminal one-liner per ~20-second episode.
A coherent short-form series — specific, oddly-niche, repeatable.

By [Sentinel Research](https://github.com/sentinel-research).

## Episodes
| # | Topic | Command | File |
|---|-------|---------|------|
| 01 | Disk usage, human-sorted | `du -sh * \| sort -h` | [ep01-disk-usage.mp4](ep01-disk-usage.mp4) |
| 02 | Top 10 disk hogs, ranked | `du -sh * \| sort -h \| tail` | [ep02-top10-disk-hogs.mp4](ep02-top10-disk-hogs.mp4) |
| 03 | Biggest files system-wide | `find / -type f -size +100M 2>/dev/null \| xargs du -h \| sort -h \| tail` | [ep03-disk-hogs.mp4](ep03-disk-hogs.mp4) |
| 04 | Every listening port, one command | `lsof -nP -iTCP -sTCP:LISTEN` | [ep04-listening-ports.mp4](ep04-listening-ports.mp4) |
| 05 | Socket state + owning process | `ss -tulnp` | [ep05-socket-state.mp4](ep05-socket-state.mp4) |
| 06 | Filter a log for errors/warnings | `grep -E "ERROR\|WARN" app.log` | [ep06-log-errors.mp4](ep06-log-errors.mp4) |
| 07 | Top memory-consuming processes | `ps aux --sort=-%mem \| head` | [ep07-top-memory.mp4](ep07-top-memory.mp4) |
| 08 | Find the biggest files on disk | `du -ah / | sort -rh | head -10` | [ep08-biggest-files.mp4](ep08-biggest-files.mp4) |
| 09 | 10 largest files on disk (whole fs) | `find / -xdev -type f | xargs stat -c "%s {}" | sort -rn | head -10` | [ep09-largest-files.mp4](ep09-largest-files.mp4) |
| 10 | Find every zombie process | `ps aux \| grep Z` | [ep10-zombie-processes.mp4](ep10-zombie-processes.mp4) |

Each episode: a dark-terminal card with the command, its output, and a
one-line punchline. 1080p, ~20s, silent (the on-screen text carries the content).

> Also being posted to YouTube Shorts (channel pending Google cred).
