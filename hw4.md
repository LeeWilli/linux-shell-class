Please create hw4 directory in your root and use bash files to finish the following exercises through one or more bash scripts. It's good to write each bash file for each problem and name it with the index of problem, like 1.sh, 2.sh, etc. 

You need to write a correspondent test script for each problem with Bats（Bash Automated Testing System）(e.g., 1_test.bats). You can run it to verify the correctness of your answer through the following command
```bash
$bats 1_test.bats
```
For the usage of Bats, you can read the [text](https://github.com/LeeWilli/linux-shell-class/blob/main/Bats.md).

For regular expressions, you may reference chapter 20 of our textbook or [Data Wrangling](https://missing.csail.mit.edu/2020/data-wrangling/)

The problems are the following:

1. Write a script that enumerates the system’s users and groups from 
/etc/passwd and /etc/group (or their network database equivalents). 
For each user, print the user’s UID and the groups of which the user is a 
member.

2. Using regular expressions, write a script or pipe commands to parse a date 
in the form produced by the date command (e.g., Tue Oct 20 18:09:33 
PDT 2009) and extract the time and convert it to AM/PM system (e.g., 06:09:33 PM). 

3. Write a script that displays a one-screen summary of status data related 
to the following categories: CPU, memory, disk, or network. 

4. Find the number of words (in /usr/share/dict/words) that contain at least three `a` s and don’t have a `'s` ending. What are the three most common last two letters of those words? sed’s y command, or the tr program, may help you with case insensitivity. How many of those two-letter combinations are there? And for a challenge: which combinations do not occur?

5. Find your average, median, and max system boot time over the last ten boots. Use journalctl on Linux and log show on macOS, and look for log timestamps near the beginning and end of each boot. On Linux, they may look something like:
```bash
Logs begin at ...
```
and
```bash
systemd[577]: Startup finished in ...
```
if you can't run `journalctl`, you may not be in `systemd-journal` group. You need to download [journal.log](https://github.com/LeeWilli/linux-shell-class/blob/main/journal.log) to look for the log timestamps.
