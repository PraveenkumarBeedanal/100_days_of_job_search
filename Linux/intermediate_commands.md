### Intermediate commands

1. date
    * prints the current date and time

2. >
    * redirect the commands output to file instead of command line
    * eg; `date > today.txt` -- it overwrites the content of today.txt with current date and time
    * creates **today.txt** if it doesn't exists

3. >>
    * it also redirects the output of command to file, but instead of overwrite it appends to file
    * eg; `whoami > today.txt` -- content of today.txt
    ![alt text](image-1.png)
    * it also creats file if it doesn't exists

4. cat
    * concatenate and prints the file
    * eg; `cat today.txt` -- prints the file content to terminal
    * eg; `cat today.txt whoami.txt > concatenates` -- prints both file content one after another and save to **concatenates** file
    ![alt text](image-2.png)
    * `cat -n today.txt` -- prints along with line number

5. less
    * interactive way of displaying the file on the screen
    * allows forward and backward movement of file
    * `less big_file.txt`

6. echo
    * prints it back the user provided text
    * eg; `echo 'hello'`, `echo 'username=Praveen' > config.txt`

7. wc
    * returns word, line, character, and byte count of input file or text
    * eg; `wc -w today.txt` -- prints no of words in file
    * `wc -l today.txt` -- prints no of lines in file
    * `wc -c today.txt`  -- prints no of bytes in file

8. | -- piping
    * output of one command to another command
    * eg; `ls -l | wc` -- output of list files to word count command
    * prints lines, words and byte counts
    ![alt text](image-3.png)

9. sort
    * sorts the information
    * eg; `sort abcd.txt` -- sort lexiographically
    * eg; `sort -n numbers.txt` -- if we want to sort the number pass -n options, 
    * to reverse add -r, and get unique sort result use -u
    * eg; `sort -nu numbers.txt | wc -l` -- count no of unique numbers in file

10. uniq
    * report or filter out repeated lines in a file
    * necessary to sort the file first before passing it uniq, because it always checks adjacent to remove duplicates
    * eg; `sort duplicates.txt | uniq`
    * `sort duplicates.txt | uniq -d` -- prints only duplicate rows
    * `sort duplicates.txt | uniq -u` -- prints unique rows
    * `sort duplicates.txt | uniq -c` -- prints count of each rows
    * `sort duplicates.txt | uniq -c | sort -n` -- sort the rows count
 
 

