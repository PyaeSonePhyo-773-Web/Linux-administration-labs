# Lab 03 - Process & Service Management

## What I learned
- Checked running processes with `ps`, `top`, and `pgrep`
- Managed services using `systemctl`
- Checked service logs with `journalctl`
- Used `ss` and `lsof` to find processes using a port

## Troubleshooting

Nginx failed to start because port 80 was already in use by Apache2.

I checked the Nginx logs with `journalctl` and tested the configuration with `nginx -t`. The configuration was valid, so I checked port 80 using `ss` and `lsof` and found Apache2 listening on it.

After stopping Apache2, I checked the services again. Nginx was running and `systemctl --failed` showed no failed units.

## Commands used

```bash
ps aux | head -10
top
pgrep -a nginx
systemctl --failed
systemctl status nginx --no-pager
sudo journalctl -u nginx -n 30 --no-pager
sudo nginx -t
sudo ss -ltnp 'sport = :80'
sudo lsof -i :80
```

## Test Results

Command outputs are saved in `test-results/`.

## Skills practiced
Linux process management, systemd, log analysis, port troubleshooting.
