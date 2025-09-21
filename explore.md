Question 1: How big is the dataset?
The csv file is 4896884 bytes , which is apporximately 4.8 megabytes. (wc -c clean_dialogue.csv)

Question 2: What is the structure of the data?
The headers are title, write, dialog and pony (csvtool head 1 clean_dialog.csv)
To get each value, I can do csvtool col 1-2 (or any range I need) clean_dialog.csv

Question 3: How many episodes does it over?
198 episodes (csvtool col 1 clean_dialog.csv | uniq | wc -l
198)

Question 4: Unexpected aspect of the dataset
When you try to count the number of unique ponies using the 4th column, the same pony may be counted uniquely (even though they're the same). This could be due to characters or spaces being different, which only makes them visually similar.