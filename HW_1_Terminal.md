## HW_1_Terminal

1) See where I am - `pwd`
2) Create a folder - `mkdir foldername`
3) Go to the folder - `cd foldername`
4) Create 3 folders - `mkdir foldername1 foldername2 foldername3`
5) Go to any folder - `cd foldername1`
6) Create 5 files (3 txt, 2 json) - `touch a.txt b.txt c.txt d.json e.json`
7) Create 3 folders - `mkdir foldername4 foldername5 foldername6`
8) List folder contents - `ls`
9) Open any txt file - `open a.txt`
10) Write there any text - `cat >> a.txt`
qwer
bbg
11) Save and exit - `Enter` --> `Ctrl+C`
12) Exit the folder one level up - `cd ..`
13) Move any 2 files you created to any other folder - `mv a.txt b.txt foldername5/`
14) Copy any 2 files you created to any other folder - `cp a.txt b.txt foldername6/`
15) Find a file by name - `find. -name c.txt`
16) View content in real time (`grep` command) and learn how it works - `tail -f a.txt | grep -w -i "sec"`
17) Output the first few lines from a text file - `head -n3 a.txt`
18) Output the last few lines from a text file - `tail -n3 a.txt`
19) View the contents of a long file (`less` command) learn how it works - `less a.txt`
The more filter command displays the contents of the file on the screen in separate pages, just the size of the entire screen. In order to see the next page, you must press the spacebar. Pressing the ‹Enter› key shifts by one line. The ‹B› key goes back one screen. You can exit the view mode using the ‹Q› key.
20) Display date and time - `date +%F-%T`

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

