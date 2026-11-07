# Lab 04 - System Monitoring

## What I learned

- Checked system uptime and load average using `uptime`
- Monitored RAM and swap usage with `free`
- Checked CPU information using `nproc` and `lscpu`
- Monitored running processes with `top`
- Checked disk usage using `df` and `du`
- Monitored system performance with `vmstat`
- Checked listening ports using `ss`
- Monitored network interfaces with `ip`

## System Information

- OS: Ubuntu Linux
- CPU: AMD Ryzen 7 5800U
- CPU cores: 8
- Logical CPUs: 16
- RAM: 6.6 GiB

## Commands used

```bash
uptime
free -h
nproc
lscpu
top
df -h
du -sh ~/projects/linux-administration-labs
vmstat 1 5
ss -tuln
ip -s link
```

## Observations

- System load was low during testing.
- Approximately 1.9 GiB of memory was available.
- Root filesystem usage was around 5%.
- CPU was mostly idle during the `vmstat` test.
- SSH (22) and HTTP (80) ports were listening.
- No network receive errors were reported in the interface statistics.

## Test Results

Command outputs are saved in the `test-results/` directory.

Screenshots are saved in the `screenshots/` directory.

## Skills practiced

Linux system monitoring, CPU and memory analysis, disk management, process monitoring, and network diagnostics.
