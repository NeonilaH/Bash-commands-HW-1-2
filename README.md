[name.txt](https://github.com/NeonilaH/Terminal-Bash-commands/blob/main/name.txt), [phone.txt](https://github.com/NeonilaH/Terminal-Bash-commands/blob/main/phone.txt), [thefirst.txt](https://github.com/NeonilaH/Terminal-Bash-commands/blob/main/thefirst.txt) are the very first files created and pushed to the repository during the class.</br>
[HW_1_Terminal](#1.1) - The first homework was completed with MAC Terminal.</br>
[HW_2_GitBash](#1.2) - The second homework was completed with Windows Git Bash.

***

## **HW_1_Terminal**<a name="1.1"><a>

1) See where you are. - `pwd`
2) Create a folder. - `mkdir foldername`
3) Go to the folder. - `cd foldername`
4) Create 3 folders. - `mkdir foldername1 foldername2 foldername3`
5) Go to any folder. - `cd foldername1`
6) Create 5 files (3 txt, 2 json). - `touch a.txt b.txt c.txt d.json e.json`
7) Create 3 folders. - `mkdir foldername4 foldername5 foldername6`
8) List folder contents. - `ls`
9) Open any txt file. - `open a.txt`
10) Write there any text. - `cat >> a.txt`
qwer
bbg
11) Save and exit. - `Enter` --> `Ctrl+C`
12) Exit the folder one level up. - `cd ..`
13) Move any 2 files you created to any other folder. - `mv a.txt b.txt foldername5/`
14) Copy any 2 files you created to any other folder. - `cp a.txt b.txt foldername6/`
15) Find a file by name. - `find. -name c.txt`
16) View content in real time (`grep` command) and learn how it works. - `tail -f a.txt | grep -w -i "sec"`
17) Print the first few lines from a text file. - `head -n3 a.txt`
18) Print the last few lines from a text file. - `tail -n3 a.txt`
19) View the contents of a long file (`less` command) learn how it works. - `less a.txt`
The more filter command displays the contents of the file on the screen in separate pages, just the size of the entire screen. In order to see the next page, you must press the spacebar. Pressing the ‹Enter› key shifts by one line. The ‹B› key goes back one screen. You can exit the view mode using the ‹Q› key.
20) Display date and time. - `date +%F-%T`

### Exercise *

1) Send http request to server 

`curl http://162.55.220.72:5005/terminal-hw-request`
```
 % Total % Received % Xferd Average Speed ​​Time Time Time Current
                                 Dload Upload Total Spent Left Speed
100 283 100 283 0 0 1687 0 --:--:-- --:--:-- --:--:-- 1704{
 "Intro": "Hello!! This is your first response from server",
 "Tasks": {
 "Task_1": "Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number)",
 "result": [
 "Your_String",
  "Your_number"
  ]
 }
}
```

`curl "http://162.55.220.72:5005/get_method?name=Neonila&age=34"`
```
% Total % Received % Xferd Average Speed ​​Time Time Time Current
                                 Dload Upload Total Spent Left Speed
100 25 100 25 0 0 160 0 --:--:-- --:--:-- --:--:-- 162[
 "Neonila"
 "34"
]
```

2) Write a script that will automatically execute steps 3, 4, 5, 6, 7, 8, 13

`nano bash_script.sh`

```sh
#!/bin/bash
mkdir d1 d2 d3
cd d1
touch a.txt b.txt c.txt d.json e.json
mkdir d4 d5 d6
ls
mv a.txt b.txt d6/
```

`bash bash_script.sh`

***

## **HW_2_GitBash**<a name="1.2"><a>

1. Make folder dir_1. -
`mkdir dir_1`
 2. Go to dir_1 folder. -
`cd dir_1`
 3. Create folder inner_dir_1. -
 `mkdir inner_dir_1`
 4. See where you are. -
`pwd`
 5. Being in the dir_1 folder, create an empty text file tf_1.txt. -
 `touch tf_.txt`
 6. Being in the dir_1 folder, use the cat command to create a text file tf_2.txt with the following lines: the first 1
 second 2
 the third 3. <br/>
 `cat >> tf_2.txt`

 7. Go to the folder inner_dir_1. -
`cd inner_dir_1`
 8. Using cat command make a text file tf_3.txt with any lines. -
 `cat >> tf_3.txt`
 9. Using cat command add the line “the second 2” to the file tf_3.txt. -
`cat >> tf_3.txt`
 10. Using cat command add the line “the sec 2” to the text file tf_3.txt. -
`cat >> tf_3.txt`
 11. Using cat command add the line “the sec 3” to the text file tf_2.txt. -
`cat >> tf_2.txt`
 12. Using cat command add the line “the SeCoNd 2” to the text file tf_3.txt. -
`cat >> tf_3.txt`
 13. Using cat command add the line “the seConD 2” to the text file tf_2.txt. -
`cat >> tf_2.txt`
 14. Make a text file tf_4.txt which will contain 15 lines. -
`seq 1 15 | cat > tf_4.txt`
 15. Make a text file tF_5.txt which will contain 13 lines. -
`seq 1 13 | cat > tF_5.txt`
 16. List all files in a folder. -
`ls`
 17. Exit folder inner_dir_1. -
`cd`
 18. Print the contents of the tf_3.txt file in the terminal. -
`cat dir_1/inner_dir_1/tf_3.txt`
 19. Find the path to the file tf_4.txt. -
`find $PWD -type f -name "tf_4.txt"`
 20. Clear the tf_4.txt file from the contents without deleting the file itself. -
`> ft_4.txt`
 21. Find the path to files that have "tf" in their names. -
`find $PWD -type f -name "tf*"`
 22. Find the path to files that have "tf" in the name and letters in any case. <br/>
`find $PWD -type f -iname "tf*"`
 23. Find lines in files where there is a combination of letters “sec” in the current folder. <br/>
`find . -type f -name "*" -exec grep "sec" {} +`
 24. Find lines in files where there is a combination of letters “sec” in any case in the current folder. <br/>
`find . -type f -name "*" -exec grep -i "sec" {} +`
 25. Find lines in files where there is only a combination of letters “sec” in the current folder. <br/>
`find . -type f -name "*" -exec grep -w "sec" {} +`
 26. Find lines in files where there is only a combination of letters “sec” in any case in the current folder. <br/>
`find . -type f -name "*" -exec grep -w -i "sec" {} +`
 27. Find lines in files where there is a combination of letters “second” in the current folder. <br/>
`find . -type f -name "*" -exec grep "second" {} +`
 28. Find lines in files where there is a combination of letters “second” in any case in the current folder. <br/>
`find . -type f -name "*" -exec grep -i "second" {} +`
 29. Find lines in files where there is a combination of letters “second” in all folders below the level. <br/>
`find inner_dir_1 -type f -name "*" -exec grep -i "second" {} +`
 30. Find only the path and file name in the lines of which there is a combination of letters “second” in the current folder. <br/>
`find . $PWD -type f -name "*" -exec grep "second" {} +`
 31. Find all lines in all files where there is no “second” combination. <br/>
`find -type f -name "*" -exec grep -v "second" {} +`
 32. Find only the name and path to files where there is no “second” combination. <br/>
`find $PWD -type f -name "*" -exec grep -v "second" {} +`
 33. Print to the terminal the last 4 lines of any text file. -
`tail -n4 tf_2.txt`
 34. Print in the terminal 4 the first lines of any text file. -
`head -n4 tf_4.txt`
 35. Command in one line. Create a folder and create a text file with contents. <br/>
`mkdir B && touch B/myfile.txt`
 36. Command in one line. Move to any one folder text files that have the word “sec” in their content. <br/>
`grep -rl "sec" | xargs mv -t B`
 37. Command in one line. Copy to any one folder text files that have the word “sec” in their content. <br/>
`grep -rl "sec" | xargs cp -t B`
 38. Command in one line. Find all lines with "sec" in all text files, copy and paste these lines into one new created text file. <br/>
`grep -iro 'sec' > sssssoo.txt`
 39. Command in one line. Delete text files that have the word “sec” in their content. <br/>
`grep -l "sec" * | xargs rm`
 40. Just print the line “Good job!!”. -
  `echo "Good Job!"`
