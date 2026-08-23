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
| 51 | What is the HTTP status of each endpoint? | `curl -so /dev/null -w "%{http_code}\n" x.io x.io/v2` | [ep51-curl-status.mp4](ep51-curl-status.mp4) |
| 52 | Encode this into something safe for a URL | `echo "hello world" | base64` | [ep52-base64-encode.mp4](ep52-base64-encode.mp4) |
| 53 | Print just the username and shell columns | `awk -F: '{print $1, $7}' /etc/passwd` | [ep53-awk-cols.mp4](ep53-awk-cols.mp4) |
| 54 | Bundle a whole folder into one file | `zip -r backup.zip cfg` | [ep54-zip-folder.mp4](ep54-zip-folder.mp4) |
| 55 | Line this messy list up into neat columns | `column -t users.txt` | [ep55-column-t.mp4](ep55-column-t.mp4) |
| 56 | Combine two files, line by line | `paste names.txt ages.txt` | [ep56-paste-join.mp4](ep56-paste-join.mp4) |
| 57 | Turn this text into lowercase | `echo "HELLO WORLD" | tr "[:upper:]" "[:lower:]"` | [ep57-tr-lowercase.mp4](ep57-tr-lowercase.mp4) |
| 58 | Read this backwards, line by line | `echo "abc def xyz" | rev` | [ep58-rev-backwards.mp4](ep58-rev-backwards.mp4) |
| 59 | What primes does this number break into? | `factor 10002000` | [ep59-factor-primes.mp4](ep59-factor-primes.mp4) |
| 60 | Merge two lists that share a key | `join names_age.txt names_city.txt` | [ep60-join-merge.mp4](ep60-join-merge.mp4) |
| 61 | Count up by 2 from 0 to 10 | `seq 0 2 10` | [ep61-seq-range.mp4](ep61-seq-range.mp4) |
| 62 | Do this math without leaving the shell | `echo "scale=2; 22/7" | bc` | [ep62-bc-math.mp4](ep62-bc-math.mp4) |
| 63 | Flip the order of the lines | `tac steps.txt` | [ep63-tac-reverse.mp4](ep63-tac-reverse.mp4) |
| 64 | Number every line of a file | `nl sample.txt` | [ep64-nl-number.mp4](ep64-nl-number.mp4) |
| 65 | What is in each list, and what is in both | `comm c1.txt c2.txt` | [ep65-comm-setdiff.mp4](ep65-comm-setdiff.mp4) |
| 66 | What is the file, byte for byte | `od -c mini.txt` | [ep66-od-bytes.mp4](ep66-od-bytes.mp4) |
| 67 | Keep only the unique values, sorted | `sort -u fruits2.txt` | [ep67-sort-unique.mp4](ep67-sort-unique.mp4) |
| 68 | Copy just the first 4 bytes of a file | `dd if=blob.bin bs=1 count=4` | [ep68-dd-carve.mp4](ep68-dd-carve.mp4) |
| 69 | How full is every mounted volume | `df -h` | [ep69-df-disk.mp4](ep69-df-disk.mp4) |
| 70 | Where does this character first appear | `expr index "hello world" d` | [ep70-expr-index.mp4](ep70-expr-index.mp4) |
| 71 | What readable text is hiding in this binary | `strings mini.bin` | [ep71-strings-bin.mp4](ep71-strings-bin.mp4) |
| 72 | What user am I running as | `whoami` | [ep72-whoami.mp4](ep72-whoami.mp4) |
| 73 | What block devices and partitions does this box have | `lsblk` | [ep73-lsblk-devices.mp4](ep73-lsblk-devices.mp4) |
| 74 | Which groups am I a member of | `id -G` | [ep74-id-groups.mp4](ep74-id-groups.mp4) |
| 75 | How big is this directory, all told | `du -sh /tmp/to_repo` | [ep75-du-size.mp4](ep75-du-size.mp4) |
| 76 | What is this environment variable set to | `printenv HOME` | [ep76-printenv.mp4](ep76-printenv.mp4) |
| 77 | What OS is this box actually running | `cat /etc/os-release` | [ep77-os-release.mp4](ep77-os-release.mp4) |
| 78 | How many CPU cores does this box have | `nproc` | [ep78-nproc-cores.mp4](ep78-nproc-cores.mp4) |
| 79 | How long has this box been up, in plain english | `uptime -p` | [ep79-uptime.mp4](ep79-uptime.mp4) |
| 80 | **80-episode MILESTONE** - how do I get just the file name out of a path | `basename /tmp/ep80/ep80_video.mp4` | [ep80-basename.mp4](ep80-basename.mp4) |
| 81 | How do I get a checksum and size for a file | `cksum ck.txt` | [ep81-cksum.mp4](ep81-cksum.mp4) |
| 82 | How do I get just the directory part of a path | `dirname` | [ep82-dirname.mp4](ep82-dirname.mp4) |
| 83 | How do I get the 32-hex MD5 of a file | `md5sum ck.txt` | [ep83-md5sum.mp4](ep83-md5sum.mp4) |
| 84 | How many processes match a name, fast | `pgrep -c bash` | [ep84-pgrep.mp4](ep84-pgrep.mp4) |
| 85 | How do I pick a random number in a range | `shuf -i 1-100 -n 1` | [ep85-shuf.mp4](ep85-shuf.mp4) |
| 86 | List a directory one name per line | `ls -1 ~/mission/wallet` | [ep86-ls1.mp4](ep86-ls1.mp4) |
| 87 | `tty` | how do I find out if stdin is a real terminal? | [ep87-tty.mp4](ep87-tty.mp4) |
| 88 | `readlink -f /tmp/m_link` | follow a symlink chain to its true target — `ep88-readlink.mp4` | [88](ep88-readlink.mp4) |
| 89 | Which binaries would the shell run for a name? | `type -a cat` | [ep89-type.mp4](ep89-type.mp4) |
| 90 | **MILESTONE** | Chunk a file into fixed-size pieces, then prove every piece landed | `split -l 2 splitme.txt part_ && ls -1 part_*` | [ep90-split.mp4](ep90-split.mp4) |
| 91 | What permission bits does my shell subtract from new files? | `umask` | [ep91-umask.mp4](ep91-umask.mp4) |
Each episode: a dark-terminal card with the command, its output, and a
one-line punchline. 1080p, ~20s, silent (the on-screen text carries the content).

> Also being posted to YouTube Shorts (channel pending Google cred).
