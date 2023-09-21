Please create hw3 directory in your root and use bash files to finish the following exercises through one or more bash scripts. It's good to write each bash file for each problem and name it with the problem of index, like 1.sh, 2.sh, etc.

1. Say you have a command that fails rarely. In order to debug it you need to capture its output but it can be time-consuming to get a failure run. Write a bash script that runs the following script until it fails and captures its standard output and error streams to files and prints everything at the end. Bonus points if you can also report how many runs it took for the script to fail.
```bash
#!/usr/bin/env bash

 n=$(( RANDOM % 100 ))

 if [[ n -eq 42 ]]; then
    echo "Something went wrong"
    >&2 echo "The error was using magic numbers"
    exit 1
 fi

 echo "Everything went according to plan"
```
2. As we covered in the lecture find’s -exec can be very powerful for performing operations over the files we are searching for. However, what if we want to do something with all the files, like creating a zip file? As you have seen so far commands will take input from both arguments and STDIN. When piping commands, we are connecting STDOUT to STDIN, but some commands like tar take inputs from arguments. To bridge this disconnect there’s the xargs command which will execute a command using STDIN as arguments. For example ls | xargs rm will delete the files in the current directory.

    Your task is to write a command that recursively finds all HTML files in the folder and makes a zip with them. Note that your command should work even if the files have spaces (hint: check -d flag for xargs).

3. Write a command or script to recursively find the most recently modified file in a directory. More generally, can you list all files by recency?

4. Run `vimtutor` from your shell and complete vimtutor.

5. Here is a broken fizz buzz implementation:
```python
def fizz_buzz(limit):
    for i in range(limit):
        if i % 3 == 0:
            print('fizz')
        if i % 5 == 0:
            print('fizz')
        if i % 3 and i % 5:
            print(i)

def main():
    fizz_buzz(10)
```
You need to copy the implementation to your Vim console and fix the following issues through Vim:
- Main is never called
- Starts at 0 instead of 1
- Prints “fizz” and “buzz” on separate lines for multiples of 15
- Prints “fizz” for multiples of 5
- Uses a hard-coded argument of 10 instead of taking a command-line argument

After fixing the issues, try running it and ensure your correctness by the following concept of fizz buzz.


> What is fizz buzz?

> Fizz buzz is a group word game for children to teach them about division.[1] Players take turns to count incrementally, replacing any number divisible by three with the word "fizz", and any number divisible by five with the word "buzz", and any number divisible by both 3 and 5 with the word "fizzbuzz". 

> The player designated to go first says the number "1". Then a typical round of fizz buzz would start as follows:

> 1, 2, Fizz, 4, Buzz, Fizz, 7, 8, Fizz, Buzz, 11, Fizz, 13, 14, Fizz Buzz, 16, 17, Fizz, 19, Buzz, Fizz, 22, 23, Fizz, Buzz, 26, Fizz, 28, 29, Fizz Buzz, 31, 32, Fizz, 34, Buzz, Fizz, ...

