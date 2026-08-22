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
| 11 | See what is listening (sockets/ports) | `ss -tulnp` | [ep11-listening-sockets.mp4](ep11-listening-sockets.mp4) |
| 12 | Find the disk hogs, no rm -rf | `du -sh /home/* 2>/dev/null` | [ep12-disk-hogs.mp4](ep12-disk-hogs.mp4) |
| 13 | Test reachability + latency | `ping -c 4 1.1.1.1` | [ep13-ping-latency.mp4](ep13-ping-latency.mp4) |
| 14 | Latest files, newest first | `ls -lht | head` | [ep14-ls-lht.mp4](ep14-ls-lht.mp4) |
| 15 | Disk space, by filesystem | `df -hT` | [ep15-df-hT.mp4](ep15-df-hT.mp4) |
| 16 | Ports + who owns them | `netstat -tulpn` | [ep16-netstat-tulpn.mp4](ep16-netstat-tulpn.mp4) |
| 17 | Peek at a log end, no pager | `tail -n 20 app.log` | [ep17-tail-n20.mp4](ep17-tail-n20.mp4) |
| 18 | System health, one frame | `top -bn1 | head` | [ep18-top-bn1.mp4](ep18-top-bn1.mp4) |
| 19 | Inode check: can I make files? | `df -i` | [ep19-df-i.mp4](ep19-df-i.mp4) |
| 20 | Locate files by pattern, fast | `find /home -name *.log` | [ep20-find-name-log.mp4](ep20-find-name-log.mp4) |
| 21 | Pull fields out of a delimited file | `cut -d: -f1,3 /etc/passwd` | [ep21-cut-fields.mp4](ep21-cut-fields.mp4) |
| 22 | Count how often each line repeats | `sort app.log \| uniq -c` | [ep22-uniq-c.mp4](ep22-uniq-c.mp4) |
| 23 | Which process holds a port | `lsof -i:443` | [ep23-lsof-port.mp4](ep23-lsof-port.mp4) |
| 24 | Search every file, with line numbers | `grep -rn TODO .` | [ep24-grep-rn-todo.mp4](ep24-grep-rn-todo.mp4) |
| 25 | Count the lines in each file | `wc -l *.log` | [ep25-wc-l-logs.mp4](ep25-wc-l-logs.mp4) |
| 26 | Peek inside an archive, no extract | `tar -tzf backup.tgz` | [ep26-tar-tzf.mp4](ep26-tar-tzf.mp4) |
| 27 | Delete a whole class of files, safely | `find . -name *.tmp -delete` | [ep27-find-delete.mp4](ep27-find-delete.mp4) |
| 28 | Is the service actually running? | `systemctl status nginx` | [ep28-systemctl-status.mp4](ep28-systemctl-status.mp4) |
| 29 | Every copy of a command on PATH | `which -a git` | [ep29-which-a.mp4](ep29-which-a.mp4) |
| 30 | What did I just run? | `history | tail` | [ep30-history-tail.mp4](ep30-history-tail.mp4) |
| 31 | How much RAM is actually free? | `free -h` | [ep31-free-h.mp4](ep31-free-h.mp4) |
| 32 | Permissions, size, and timestamps of a file | `stat app.log` | [ep32-stat-log.mp4](ep32-stat-log.mp4) |
| 33 | Did the download come through intact? | `md5sum release.tar.gz` | [ep33-md5sum.mp4](ep33-md5sum.mp4) |
| 34 | Look at the raw bytes of a file | `xxd -l 48 /usr/bin/git` | [ep34-xxd-raw.mp4](ep34-xxd-raw.mp4) |
| 35 | What kind of file is this, really? | `file /usr/bin/git README.md photo.png` | [ep35-file-magic.mp4](ep35-file-magic.mp4) |
| 36 | What changed between two files? | `diff old.conf new.conf` | [ep36-diff-conf.mp4](ep36-diff-conf.mp4) |
| 37 | What jobs am I scheduled to run? | `crontab -l` | [ep37-crontab-l.mp4](ep37-crontab-l.mp4) |
| 38 | Which process is eating the most CPU? | `ps -eo pid,pcpu,pmem,comm --sort=-pcpu` | [ep38-ps-pcpu.mp4](ep38-ps-pcpu.mp4) |
| 39 | Run a command on a remote box, no password | `ssh -i key user@host uptime` | [ep39-ssh-key.mp4](ep39-ssh-key.mp4) |
| 40 | How long is this document, in words? | `wc -w README.md` | [ep40-wc-w.mp4](ep40-wc-w.mp4) |
| 41 | What have I actually committed lately? | `git log --oneline -5` | [ep41-git-log.mp4](ep41-git-log.mp4) |
| 42 | How does this month look, on a calendar? | `cal` | [ep42-cal-month.mp4](ep42-cal-month.mp4) |
| 43 | Which ports is this box listening on? | `ss -tlnp` | [ep43-ss-ports.mp4](ep43-ss-ports.mp4) |
| 44 | What OS and kernel is this box running? | `uname -a` | [ep44-uname-a.mp4](ep44-uname-a.mp4) |
| 45 | What is the current time, UTC and epoch? | `date -u; date +%s` | [ep45-date-utc.mp4](ep45-date-utc.mp4) |
| 46 | How do I sort these lines by number? | `sort -rn prices.txt` | [ep46-sort-rn.mp4](ep46-sort-rn.mp4) |
| 47 | Give me just the first column of this file | `cut -d: -f1 /etc/passwd` | [ep47-cut-field.mp4](ep47-cut-field.mp4) |
| 48 | Replace a value in the file, in place | `sed -i s/8080/9090/ app.conf` | [ep48-sed-replace.mp4](ep48-sed-replace.mp4) |
| 49 | How many times did I run this? | `history | grep deploy` | [ep49-history-grep.mp4](ep49-history-grep.mp4) |
| 50 | Pull a field out of a JSON file | `jq ".users[] | .email" users.json` | [ep50-jq-field.mp4](ep50-jq-field.mp4) |

Each episode: a dark-terminal card with the command, its output, and a
one-line punchline. 1080p, ~20s, silent (the on-screen text carries the content).

> Also being posted to YouTube Shorts (channel pending Google cred).
