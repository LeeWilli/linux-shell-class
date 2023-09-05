# The basics of Linux Shell

Part 1: Navigate the file system
- Create a directory `foo` via `mkdir foo` command

- `cd` into the `foo` directory

Part 2: Create a file with `touch`
- Create a file using `touch newfile.txt`

Run the command again? What happens?

Part 3: Remove files and directories
- Remove the directory `foo` via the command `rm -rf foo`

Make a file and then delete it: `touch bar.txt` then run `rm bar.txt`

Part 4: List files
- list the contents of `/usr/bin` by running the command `ls -l /usr/bin`

# Practicing Common Shell Piping Operations

Part 1: Count the files and directories in `/usr/bin`
- Pipe the output of `ls -l /usr/bin | wc -l` to count the files and directories in `/usr/bin`

How many did you count?

Part 2: Create a new file with `echo a`
- Run the following command "`echo 'hi'`"

Pipe this to a file by using "`echo 'hi' > hello.txt`"

Now run `ls` to verify it exists

- count the words in the file `cat hello.txt | wc -w`

How many did you count?

# Goal: Learn to work with streams

Part 1: Create a new file and write to it via stdout
- Run the following command in your Bash terminal: `echo "fruit" > meal.txt`

Part 2: Append new data to the file by using stdout
- Run the following command in your Bash terminal: `echo "chocolate" >> meal.txt`

Part 3: Redirect standard input
- Use the tr command to substitute characters by reading standard input: `tr fruit steak < meal.txt`

Part 4: Throwaway stdout to /dev/null
- Send the output of standard out to /dev/null via `cat meal.txt > /dev/null`

