Please create hw5 directory in your root and use bash files to finish the following exercises through one or more bash scripts. It's good to write each bash file for each problem and name it with the index of problem, like 1.sh, 2.sh, etc. 

You need to write a correspondent test script for each problem with Bats（Bash Automated Testing System）(e.g., 1_test.bats). You can run it to verify the correctness of your answer through the following command
```bash
$bats 1_test.bats
```
For the usage of Bats, you can read the [text](https://github.com/LeeWilli/linux-shell-class/blob/main/Bats.md).

The problems are the following:

1. Given a text file containing a program's source code, extract all function names and their corresponding parameters using regular expressions. The function names should be preceded by the keyword "function" and should be followed by an opening parenthesis "(".

Example Input (input.txt):
```
function add(a, b) {
    return a + b;
}

function multiply(x, y, z) {
    return x * y * z;
}

function subtract(a, b) {
    return a - b;
}
```
Expected Output:
```
add(a, b)
multiply(x, y, z)
subtract(a, b)
```

2. Given a text file containing a list of sentences, reverse the order of words in each sentence using sed.

Example Input (input.txt):
```
This is the first sentence.
Here is another sentence.
One more sentence for testing.
```
Expected Output:
```
sentence first the is This.
sentence another is Here.
testing. for sentence more One
```

3. Given a text file containing a list of employee records (name, department, salary), calculate the average salary for each department and print the department names and their average salaries using awk. The file has the following format: <name>,<department>,<salary>

Example Input (input.txt):
```
John,IT,5000
Jane,HR,6000
Smith,IT,4500
Emily,Marketing,7000
David,HR,5500
Lisa,Marketing,8000
```
Expected Output:
```
IT,4750
HR,5750
Marketing,7500
```

4. Find online data HTML data that can be read from /home/wangli/newclassroom/code/linux-shell-class/tables.html in our server. Find the min and max of one column in a single command, and the sum of the difference between the two columns in another.
