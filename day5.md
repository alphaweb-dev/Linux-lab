git log
git log --oneline
git show <commit-id>
git show <commit-id1> <commit-id2>
history
!! (repeat last command)
!<number> (run a command from history)
tail -n 20 /var/log/syslog
less /var/log/auth.log

### git log --oneline (latest 5 commits)

b945995 Added day 5 lab notes
6fbc458 Added day 4 lab notes
e4e9fa1 Added day 3 lab notes
28e6ce6 Added day 2 lab notes
3638cf1 Added day 1 lab notes

### git show HEAD (details of last commit)

commit b945995ba2a8210208be3dc9a7fe53625c05b293
Author: alphaweb-dev <olasegun272@gmail.com>
Date:   Wed Oct 1 20:33:51 2025 +0100

    Added day 5 lab notes

### history (last 10 commands)

less /var/log/auth.log
EOF

  318  cat day5.md
  319  echo -e "\n### git log --oneline (latest 5 commits)\n" >> day5.md
  320  git log --oneline -n 5 >> day5.md
  321  echo -e "\n### git show HEAD (details of last commit)\n">> day5.md
  322  git show --quiet HEAD >> day5.md
  323  echo -e "\n### history (last 10 commands)\n" >> day5.md
  324  history | tail -n 10 >> day5.md

### tail -n 10 /var/log/syslog

Oct  2 01:53:30 Solomon 50-motd-news[453]:    https://ubuntu.com/engage/secure-kubernetes-at-the-edge
Oct  2 01:53:30 Solomon systemd[1]: motd-news.service: Deactivated successfully.
Oct  2 01:53:30 Solomon systemd[1]: Finished Message of the Day.
Oct  2 01:53:55 Solomon systemd-resolved[131]: Clock change detected. Flushing caches.
Oct  2 01:57:48 Solomon systemd-resolved[131]: message repeated 6 times: [ Clock change detected. Flushing caches.]
Oct  2 01:57:48 Solomon systemd[1]: Starting Cleanup of Temporary Directories...
Oct  2 01:57:48 Solomon systemd[1]: systemd-tmpfiles-clean.service: Deactivated successfully.
Oct  2 01:57:48 Solomon systemd[1]: Finished Cleanup of Temporary Directories.
Oct  2 01:58:21 Solomon systemd-resolved[131]: Clock change detected. Flushing caches.
Oct  2 02:01:06 Solomon systemd-resolved[131]: message repeated 5 times: [ Clock change detected. Flushing caches.]

### last sudo auth entries (auth.log)

Oct  1 23:17:01 Solomon CRON[697]: pam_unix(cron:session): session opened for user root(uid=0) by (uid=0)
Oct  1 23:17:01 Solomon CRON[697]: pam_unix(cron:session): session closed for user root
Oct  2 01:42:23 Solomon systemd-logind[192]: New seat seat0.
Oct  2 01:42:25 Solomon login[285]: pam_unix(login:session): session opened for user alphaweb(uid=1000) by (uid=0)
Oct  2 01:42:26 Solomon systemd-logind[192]: New session 1 of user alphaweb.
Oct  2 01:42:26 Solomon systemd: pam_unix(systemd-user:session): session opened for user alphaweb(uid=1000) by (uid=0)
Oct  2 02:01:26 Solomon sudo: alphaweb : TTY=pts/0 ; PWD=/home/alphaweb/portfolio ; USER=root ; COMMAND=/usr/bin/tail -n 10 /var/log/syslog
Oct  2 02:01:26 Solomon sudo: pam_unix(sudo:session): session opened for user root(uid=0) by (uid=1000)
Oct  2 02:01:26 Solomon sudo: pam_unix(sudo:session): session closed for user root
Oct  2 02:04:12 Solomon sudo: alphaweb : TTY=pts/0 ; PWD=/home/alphaweb/portfolio ; USER=root ; COMMAND=/usr/bin/tail -n 10 /var/log/auth.log
