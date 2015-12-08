#Homework 2

######Esther Teplitsky
######12/4/2015
######GA Data Science 19

Using chipotle.tsv in the data subdirectory:
Look at the head and the tail, and think for a minute about how the data is structured. What do you think each column means? What do you think each row means? Tell me! (If you're unsure, look at more of the file contents.)

`head chipotle.tsv`
`tail chipotle.tsv`

Each column is an attribute of an item that was ordered at Chipotle, which each row represents an individual item that was ordered.

How many orders do there appear to be?

`Sort chipotle.tsv`

There appear to be 999 orders, as the first order_id is 1 and the last is 999.

How many lines are in the file?

Wc – l chipotle.tsv

4623 lines

Which burrito is more popular, steak or chicken?

grep -i "chicken burrito" | wc -l
grep -i "steak burrito" | wc –l

553 chicken burritos > 368 steak burritos

Chicken burritos are more popular than steak burritos

I really should account for the number of burritos that were ordered, but in any case, there are more orders of chicken burritos even though I have not verified that more chicken burritos were purchased overall.

Do chicken burritos more often have black beans or pinto beans?

grep -i "chicken burrito" chipotle.tsv | grep -i "pinto beans" | wc -l
grep -i "chicken burrito" chipotle.tsv | grep -i "black beans" | wc -l

105 pinto beans < 282 black beans

Chicken burritos more often have black beans.


Make a list of all of the CSV or TSV files in the DAT7 repo (using a single command). Think about how wildcard characters can help you with this task.

I’m assuming this is supposed to be the GA DS 19 repository.
grep -r ".[tc]sv" . 
grep -r ".[tc]sv" . | wc -l

The first command printed out all of the files. The second command counted the files, 194 in total.

Count the number of occurrences of the word 'dictionary' (regardless of case) across all files in the DAT7 repo.

grep -ri "dictionary" . | wc –l

There are 5 occurrences of the word ‘dictionary’

Optional: Use the the command line to discover something "interesting" about the Chipotle data. The advanced commands below may be helpful to you!


