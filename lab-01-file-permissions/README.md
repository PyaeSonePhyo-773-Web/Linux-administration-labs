# Lab 01 — Linux File System and Permissions

## Objective

Practice Linux file and directory management, file operations, and Linux permission control.

## Environment

- OS: Ubuntu Linux
- Lab type: Local hands-on lab
- Shell: Bash

## Commands Practiced

| Command | Purpose |
|---|---|
| `pwd` | Display the current directory |
| `ls -lR` | List files and directories recursively |
| `mkdir` | Create directories |
| `touch` | Create empty files |
| `cp` | Copy files |
| `mv` | Move or rename files |
| `chmod` | Change file permissions |
| `stat` | Inspect file permissions and metadata |

## Tasks Completed

1. Created a project directory structure.
2. Created and organized files.
3. Copied a file into a backup directory.
4. Renamed a file using `mv`.
5. Changed script permissions using `chmod`.
6. Verified permissions using `stat`.
7. Tested script execution with different permission settings.

## Test Results

### Test 1 — Execute Permission Enabled

- Permission: `700`
- Expected result: Script executes successfully.
- Actual result: Success.

### Test 2 — Execute Permission Disabled

- Permission: `600`
- Expected result: Execution is denied.
- Actual result: `Permission denied`.

### Test 3 — Permission Restored

- Permission: `700`
- Actual result: Script executes successfully again.

## Key Learnings

- Organized files using Linux directory commands.
- Practiced copying and renaming files.
- Learned how Linux permission bits control access.
- Verified script execution and permission failures.
- Practiced troubleshooting by changing permissions and retesting.

## Evidence

- `screenshots/` — Terminal screenshots demonstrating the lab.
- `test-results/` — Saved outputs from permission and execution tests.

## Conclusion

This lab demonstrated how Linux file permissions affect script execution and how to troubleshoot an execution failure by inspecting and correcting permissions.
