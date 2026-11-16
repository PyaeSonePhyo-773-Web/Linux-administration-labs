# Lab 05 - Disk & Filesystem Management

## What I learned

- Checked disk and partition information using `lsblk`
- Checked disk usage with `df -hT`
- Viewed mounted filesystems using `findmnt`
- Created a 100 MB virtual disk image
- Connected the image using a loop device
- Created an ext4 filesystem using `mkfs.ext4`
- Practised mounting and unmounting a filesystem
- Verified that files remained after remounting

## Practical Test

I created a virtual disk image and connected it to a loop device.

After creating an ext4 filesystem, I mounted it at `/mnt/lab-storage` and created a test file.

I then unmounted and mounted the filesystem again to verify that the test file was still there.

All tests were completed successfully.

## Commands Used

```bash
lsblk
lsblk -f
df -hT
findmnt
losetup
mkfs.ext4
mount
umount
```

## Test Results

Command outputs and test evidence are saved in this lab directory.

## Skills Practiced

Linux disk management, filesystems, loop devices, mounting and unmounting.
