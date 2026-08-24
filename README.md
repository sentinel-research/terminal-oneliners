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
| 92 | What is a one-line arithmetic sequence with a custom step? | `seq 1 3 20` | [ep92-seq.mp4](ep92-seq.mp4) |
| 93 | What is a one-line exact-decimal calculator (no float drift)? | `echo '0.1+0.2' | bc` | [ep93-bc.mp4](ep93-bc.mp4) |
| 94 | What is a one-line way to make a unique temp dir (no name collision)? | `mktemp -d` | [ep94-mktemp.mp4](ep94-mktemp.mp4) |
| 95 | How do I get a file mtime as raw epoch for scripting? | `stat -c %Y /etc/hostname` | [ep95-stat-y.mp4](ep95-stat-y.mp4) |
| 96 | How do I make a 100M file that uses 0M of real disk (sparse)? | `truncate -s 100M big && du -m big` | [ep96-truncate.mp4](ep96-truncate.mp4) |
| 97 | How do I silently compare two files and only print on a match? | `cmp -s a1.txt b1.txt && echo identical` | [ep97-cmp.mp4](ep97-cmp.mp4) |
| 98 | How do I copy a file and set its permissions in one atomic step? | `install -m 600 a b && stat -c %A b` | [ep98-install.mp4](ep98-install.mp4) |
| 99 | How do I extract one column from every line of a file? | `cut -d: -f1 pw.txt` | [ep99-cut.mp4](ep99-cut.mp4) |
| 100 | MILESTONE — How do I sum 1 through 100 with three tools in one line? | `seq 1 100 | paste -sd+ | bc` | [ep100-gauss.mp4](ep100-gauss.mp4) |
| 101 | How do I see exactly which lines differ between two files? | `diff x1.txt x2.txt` | [ep101-diff.mp4](ep101-diff.mp4) |
| 102 | How do I sort file sizes like 2K, 3M, 100M in true order? | `sort -h sz.txt` | [ep102-sorth.mp4](ep102-sorth.mp4) |
| 103 | How do I fingerprint a file so any change is detectable? | `sha256sum /etc/hostname` | [ep103-sha256.mp4](ep103-sha256.mp4) |
| 104 | How do I find which user owns a file? | `stat -c %U /etc/hostname` | [ep104-stat-u.mp4](ep104-stat-u.mp4) |
| 105 | How do I turn a relative path into one absolute, normalized path? | `realpath ./README.md` | [ep105-realpath.mp4](ep105-realpath.mp4) |
| 106 | How do I send output to the screen AND a file at the same time? | `echo hello | tee out.txt` | [ep106-tee.mp4](ep106-tee.mp4) |
| 107 | How do I drop the header line from a CSV before processing? | `tail -n +2 data.csv` | [ep107-tail-plus.mp4](ep107-tail-plus.mp4) |
| 108 | How do I sort lines by the first number, 1 before 10? | `sort -k1 -n pairs.txt` | [ep108-sort-kn.mp4](ep108-sort-kn.mp4) |
| 109 | How do I grab exactly the first 10 bytes of a file? | `head -c 10 ab.txt` | [ep109-head-c.mp4](ep109-head-c.mp4) |
| 110 | How do I read a line backwards, character by character? | `rev rv.txt` | [ep110-rev.mp4](ep110-rev.mp4) |
| 111 | How do I turn base64 back into the original text? | `echo aGVsbG8= | base64 -d` | [ep111-base64-d.mp4](ep111-base64-d.mp4) |
| 112 | How do I strip all the digits out of a string? | `echo a1b2c3 | tr -d [:digit:]` | [ep112-tr-d.mp4](ep112-tr-d.mp4) |
| 113 | How do I round a number to 2 decimal places in the shell? | `printf %.2f 3.14159` | [ep113-printf-f2.mp4](ep113-printf-f2.mp4) |
| 114 | How do I get just the byte count, with no filename? | `wc -c < wcsrc.txt` | [ep114-wc-c-lt.mp4](ep114-wc-c-lt.mp4) |
| 115 | How do I extract one specific line by its line number? | `sed -n 2p rows.txt` | [ep115-sed-n2p.mp4](ep115-sed-n2p.mp4) |
| 116 | How do I get just the folder part of a path? | `dirname /usr/local/bin/node` | [ep116-dirname.mp4](ep116-dirname.mp4) |
| 117 | How do I cut every line down to its first 3 characters? | `cut -c1-3 cutsrc.txt` | [ep117-cut-c.mp4](ep117-cut-c.mp4) |
| 118 | How do I run a command once for every line, substituting the line in? | `xargs -I {} echo "fruit: {}" < fruits.txt` | [ep118-xargs-I.mp4](ep118-xargs-I.mp4) |
| 119 | How do I suppress the trailing newline from echo? | `echo -n hello; echo world` | [ep119-echo-n.mp4](ep119-echo-n.mp4) |
| 120 | How do I check if a file exists, and act only if it does? | `test -f wcsrc.txt && echo exists` | [ep120-test-f.mp4](ep120-test-f.mp4) |
| 121 | How do I find the exact path the shell will run for a command? | `command -v bash` | [ep121-command-v.mp4](ep121-command-v.mp4) |
| 122 | How do I do arithmetic on a variable in the shell? | `let x=7+5; echo $x` | [ep122-let-arithmetic.mp4](ep122-let-arithmetic.mp4) |
| 123 | How do I extract only the matching substrings, not whole lines? | `grep -oE 'un[a-z]+ed' words.txt` | [ep123-grep-oE.mp4](ep123-grep-oE.mp4) |
| 124 | How do I exclude lines containing a pattern from a file? | `grep -v DEBUG app.log` | [ep124-grep-v.mp4](ep124-grep-v.mp4) |
Each episode: a dark-terminal card with the command, its output, and a
one-line punchline. 1080p, ~20s, silent (the on-screen text carries the content).

| 125 | How do I collapse repeated spaces into a single space? | `tr -s ' ' < rep.txt` | [ep125-tr-s.mp4](ep125-tr-s.mp4) |
| 125 | How do I collapse repeated spaces into a single space? | `tr -s ' ' < rep.txt` | [ep125-tr-s.mp4](ep125-tr-s.mp4) |
| 126 | How do I print only the first N lines of a file? | `head -n 2 five.txt` | [ep126-head-n.mp4](ep126-head-n.mp4) |
| 127 | How do I print a file type as a human-readable string? | `stat -c %F rep.txt` | [ep127-stat-F.mp4](ep127-stat-F.mp4) |
| 128 | How do I do math inline without a variable? | `echo $(( 6*7 ))` | [ep128-echo-arith.mp4](ep128-echo-arith.mp4) |
| 129 | How do I check if a file is already sorted without re-sorting it? | `sort -c unsorted.txt` | [ep129-sort-c.mp4](ep129-sort-c.mp4) |
| 130 | How do I list the lines present in BOTH of two sorted files? | `comm -12 a.txt b.txt` | [ep130-comm-12.mp4](ep130-comm-12.mp4) |
| 131 | How do I check whether the last command succeeded? | `false; echo $?` | [ep131-echo-dollar-question.mp4](ep131-echo-dollar-question.mp4) |
| 132 | How do I print a file size in bytes as a bare number? | `stat -c %s rep.txt` | [ep132-stat-s.mp4](ep132-stat-s.mp4) |
| 133 | How many lines in a log match a pattern, without printing them? | `grep -c ERROR app.log` | [ep133-grep-c.mp4](ep133-grep-c.mp4) |
| 134 | How do I get the alphabetically-first item in an unsorted file? | `sort items.txt | head -1` | [ep134-sort-head1.mp4](ep134-sort-head1.mp4) |
| 135 | How do I count characters, not bytes, in a UTF-8 file? | `wc -m < uni.txt` | [ep135-wc-m.mp4](ep135-wc-m.mp4) |
| 136 | How do I get the alphabetically-last item in an unsorted file? | `sort items.txt | tail -1` | [ep136-sort-tail1.mp4](ep136-sort-tail1.mp4) |
| 137 | How do I run a command that survives my shell logout? | `nohup echo hi` | [ep137-nohup-echo.mp4](ep137-nohup-echo.mp4) |
| 138 | How do I print just my numeric user id, without the name? | `id -u` | [ep138-id-u.mp4](ep138-id-u.mp4) |
| 139 | Which lines in a file are duplicated? | `sort dupes.txt | uniq -d` | [ep139-uniq-d.mp4](ep139-uniq-d.mp4) |
| 140 | Which lines appear exactly once, with no duplicates? | `sort dupes.txt | uniq -u` | [ep140-uniq-u.mp4](ep140-uniq-u.mp4) |
| 141 | How do I sort numbers numerically, not as text? | `sort -n nums.txt` | [ep141-sort-n.mp4](ep141-sort-n.mp4) |
| 142 | How do I get only the first line that matches a grep pattern? | `grep -m1 ERROR app.log` | [ep142-grep-m1.mp4](ep142-grep-m1.mp4) |
| 143 | How do I replace every character EXCEPT one specific character? | `tr -c b X < trc.txt` | [ep143-tr-c.mp4](ep143-tr-c.mp4) |
| 144 | How do I see which line numbers a pattern matches on? | `grep -n listen cfg.txt` | [ep144-grep-n.mp4](ep144-grep-n.mp4) |
| 145 | How do I see the line after each grep match? | `grep -A1 ERROR app.log` | [ep145-grep-A1.mp4](ep145-grep-A1.mp4) |
| 146 | How do I see the line BEFORE each grep match? | `grep -B1 ERROR app.log` | [ep146-grep-B1.mp4](ep146-grep-B1.mp4) |
| 147 | How do I grep for whole words only (not substrings)? | `grep -w cat gw.txt` | [ep147-grep-w.mp4](ep147-grep-w.mp4) |
| 148 | How do I list lines present ONLY in the first of two sorted files? | `comm -23 a.txt b.txt` | [ep148-comm-23.mp4](ep148-comm-23.mp4) |
| 149 | How do I get my username (not the numeric uid)? | `id -un` | [ep149-id-un.mp4](ep149-id-un.mp4) |
> Also being posted to YouTube Shorts (channel pending Google cred).
