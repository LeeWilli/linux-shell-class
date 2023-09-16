Please create hw2 directory in your root and use bash files to finish the following exercises through one or more bash scripts.

1. To assign variables in bash, use the syntax foo=bar, and print the value of foo on your terminal window.

2. Write a bash shell that can take the first argument that is a directory name. Then create the directory and cd into it.

3. Run the follwing commands and see the results:
```bash
  false || echo "Oops, fail"
  
  true || echo "Will not be printed"
  
  true && echo "Things went well"
  
  false && echo "Will not be printed"
  
  true ; echo "This will always run"
  
  false ; echo "This will always run"
```
  
4. One of the most common repetitive tasks that every programmer faces is finding files or directories. Using `find` to do the following tasks:
- Find all directories named src
- Find all python files that have a folder named test in their path
- Find all files modified in the last day
- Find all zip files with size in range 500k to 10M

5. Write bash functions marco and polo that do the following. Whenever you execute marco the current working directory should be saved in some manner, then when you execute polo, no matter what directory you are in, polo should cd you back to the directory where you executed marco. For ease of debugging you can write the code in a file marco.sh and (re)load the definitions to your shell by executing source marco.sh.


