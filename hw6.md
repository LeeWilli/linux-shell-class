Please create hw6 directory in your root and use bash files to finish the following exercises through one or more bash scripts. 
It's good to write each bash file for each problem and name it with the index of problems, like 1.sh, 2.sh, etc. 

You need to write a correspondent test script for each problem with Bats（Bash Automated Testing System）(e.g., 1_test.bats). You can run it to verify the correctness of your answer through the following command
```bash
$bats 1_test.bats
```
For the usage of Bats, you can read the [text](https://github.com/LeeWilli/linux-shell-class/blob/main/Bats.md).

The problems are the following:

1. Write a Bash script that takes a directory as input and recursively finds all duplicate files within that directory.
The script should display the duplicate files and their corresponding paths.

2. Write a Bash script that accepts a directory as input and recursively finds all files with a specific file extension (e.g., .txt).
The script should create a tar archive of those files in the same directory.

3. Write a Bash script that monitors a given directory for any changes (new files, modified files, or deleted files) and
logs the changes to a specified log file. The script should run indefinitely until manually stopped.
