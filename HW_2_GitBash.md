1. Make folder dir_1
 `mkdir dir_1`
 2. Go to dir_1 folder
`cd dir_1`
 3. Create folder inner_dir_1
 `mkdir inner_dir_1`
 4. See where you are
`pwd`
 5. Being in the dir_1 folder, create an empty text file tf_1.txt
 `touch tf_.txt`
 6. Being in the dir_1 folder, use the cat command to create a text file tf_2.txt with the following lines:
 `cat >> tf_2.txt`
 the first 1
 second 2
 the third 3
 7. Go to the folder inner_dir_1
`cd inner_dir_1`
 8. Through cat make a text file tf_3.txt with any lines
 `cat >> tf_3.txt`
 9. Through cat add the line “the second 2” to the file tf_3.txt
`cat >> tf_3.txt`
 10. Through cat add the line “the sec 2” to the text file tf_3.txt
`cat >> tf_3.txt`
 11. Through cat add the line “the sec 3” to the text file tf_2.txt
`cat >> tf_2.txt`
 12. Through cat add the line “the SeCoNd 2” to the text file tf_3.txt
`cat >> tf_3.txt`
 13. Through cat add the line “the seConD 2” to the text file tf_2.txt
`cat >> tf_2.txt`
 14. Make a text file tf_4.txt which will contain 15 lines.
`seq 1 15 | cat > tf_4.txt`
 15. Make a text file tF_5.txt which will contain 13 lines.
`seq 1 13 | cat > tF_5.txt`
 16. List all files in a folder.
`ls`
 17. Exit folder inner_dir_1
`cd`
 18. Output the contents of the tf_3.txt file to the terminal.
`cat dir_1/inner_dir_1/tf_3.txt`
 19. Find the path to the file tf_4.txt
`find $PWD -type f -name "tf_4.txt"`
 20. Clear the tf_4.txt file from the contents without deleting the file itself.
`> ft_4.txt`
 21. Find the path to files that have "tf" in their names.
`find $PWD -type f -name "tf*"`
 22. Find the path to files that have "tf" in the name and letters in any case.
`find $PWD -type f -iname "tf*"`
 23. Find lines in files where there is a combination of letters “sec” in the current folder
`find . -type f -name "*" -exec grep "sec" {} +`
 24. Find lines in files where there is a combination of letters “sec” in any case in the current folder
`find . -type f -name "*" -exec grep -i "sec" {} +`
 25. Find lines in files where there is only a combination of letters “sec” in the current folder
`find . -type f -name "*" -exec grep -w "sec" {} +`
 26. Find lines in files where there is only a combination of letters “sec” in any case in the current folder
`find . -type f -name "*" -exec grep -w -i "sec" {} +`
 27. Find lines in files where there is a combination of letters “second” in the current folder
`find . -type f -name "*" -exec grep "second" {} +`
 28. Find lines in files where there is a combination of letters “second” in any case in the current folder
`find . -type f -name "*" -exec grep -i "second" {} +`
 29. Find lines in files where there is a combination of letters “second” in all folders below the level
`find inner_dir_1 -type f -name "*" -exec grep -i "second" {} +`
 30. Find only the path and file name in the lines of which there is a combination of letters “second” in the current folder
`find . $PWD -type f -name "*" -exec grep "second" {} +`
 31. Find all lines in all files where there is no “second” combination
`find -type f -name "*" -exec grep -v "second" {} +`
 32. Find only the name and path to files where there is no “second” combination
`find $PWD -type f -name "*" -exec grep -v "second" {} +`
 33. Print to the terminal the last 4 lines of any text file
`tail -n4 tf_2.txt`
 34. Output to terminal 4 the first lines of any text file.
`head -n4 tf_4.txt`
 35. Command in one line. Create a folder and create a text file with contents.
`mkdir B && touch B/myfile.txt`
 36. Command in one line. Move to any one folder text files that have the word “sec” in their content
`grep -rl "sec" | xargs mv -t B`
 37. Command in one line. Copy to any one folder text files that have the word “sec” in their content
`grep -rl "sec" | xargs cp -t B`
 38. Command in one line. Find all lines with "sec" in all text files, copy and paste these lines into one new created text file.
`grep -iro 'sec' > sssssoo.txt`
 39. Command in one line. Delete text files that have the word “sec” in their content
`grep -l "sec" * | xargs rm`
 40. Just print the line “Good job!!”
`echo "Good Job!"`
