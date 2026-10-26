# Lab 02 — Linux User and Access Management

## Objective
Practice Linux user and group management, directory permissions,
shared group access, and permission troubleshooting.

## Environment
- OS: Ubuntu Linux
- Tools: useradd, groupadd, usermod, id, getent, chmod, chown, ls, namei
- Shared directory: /srv/lab02/shared
- Developer group: labdev

## Tasks Completed
1. Created the `labdev` group.
2. Created `labuser1` and `labuser2`.
3. Added both users to the `labdev` group.
4. Verified group membership using `id` and `getent`.
5. Created a shared directory at `/srv/lab02/shared`.
6. Set directory ownership to `root:labdev`.
7. Applied permission `2770` to enable shared group access and setgid inheritance.
8. Created `project-notes.txt` as `labuser1`.
9. Applied file permission `660`.
10. Verified that `labuser2` could append text to the shared file.

## Key Commands

```bash
sudo groupadd labdev
sudo useradd -m labuser1
sudo useradd -m labuser2
sudo usermod -aG labdev labuser1
sudo usermod -aG labdev labuser2

sudo mkdir -p /srv/lab02/shared
sudo chown root:labdev /srv/lab02/shared
sudo chmod 2770 /srv/lab02/shared

sudo -u labuser1 touch /srv/lab02/shared/project-notes.txt
sudo chmod 660 /srv/lab02/shared/project-notes.txt
sudo -u labuser2 sh -c 'echo "Shared access test" >> /srv/lab02/shared/project-notes.txt'
