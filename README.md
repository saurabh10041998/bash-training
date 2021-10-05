#                           Bash Training 
[![Gitter](https://badges.gitter.im/BookOmatic/community.svg)](https://gitter.im/BookOmatic/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
[![GPL Licence](https://badges.frapsoft.com/os/gpl/gpl.svg?v=103)](https://opensource.org/licenses/GPL-3.0/)
[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)

1. print HELLO on cmd
```bash
    echo "HELLO" 
```
```bash
    awk 'BEGIN { print "HELLO" }'     OR    awk 'END { print "HELLO" }'
```

2. print odd number from 1 to 100
```bash
    seq 1 2 100
```
3. Write a Bash script which accepts  name as input and displays the greeting "Welcome (name)"
```bash
    read first_name
    echo "Welcome $first_name"
```
4. Use a for loop to display the natural numbers from 1 to 50.
```bash
    for i in {1..50}
    do
        echo $i
    done
```
5. Given two integers,  X and Y, find their sum, difference, product, and quotient.
```bash
    read X
    read Y
    echo $(($X + $Y))
    echo $(($X - $Y))
    echo $(($X * $Y))
    echo $(($X / $Y))
```
6. Given two integers,  X and Y, identify whether X < Y or X > Y or X = Y .
```bash
    read X
    read Y

    if [ $X -eq $Y ]
    then
        echo "X is equal to Y"
    elif [ $X -gt $Y ]
    then 
        echo "X is greater than Y"
    else
        echo "X is less than Y"
    fi
```
7. Read in one character from STDIN. If the character is 'Y' or 'y' display "YES". If the character is 'N' or 'n' display "NO".
```bash
    read ch
    if [ $ch  = 'y' -o $ch = 'Y' ]
    then 
        echo "YES"
    else 
        echo "NO"
    fi
```
8. Given three integers (X, Y, and Z) representing the three sides of a triangle, identify whether the triangle is scalene, isosceles, or equilateral.
```bash
    read X
    read Y
    read Z
    if [ $X -eq $Y ] && [ $Y -eq $Z ]
    then
        echo "EQUILATERAL"
    elif [ $X -ne $Y ] &&  [ $Y -ne $Z ] && [ $X -ne $Z ]
    then
        echo "SCALENE"
    else
        echo "ISOSCELES"
    fi
```
9. A mathematical expression containing +,-,*,^, / and parenthesis will be provided. Read in the expression, then evaluate it. Display the result rounded to  3 decimal places
```bash
    read element
    echo $element | bc -l | xargs printf "%.3f\n"
``` 
10. Given N integers, compute their average, rounded to three decimal places.
```bash
    #! /bin/bash
    read N
    i=1
    x=0
    sum=0
    while [ $i -le $N ]
    do
        read x
        sum=$(( $sum + $x ))
        i=$(( $i + 1 ))
    done
    echo "$sum/$N" | bc -l | xargs printf "%.3f\n"
```

11. Given  N lines of input, print the  3rd character from each line as a new line of output. It is guaranteed that each of the N  lines of input will have a  3rd character.
```bash
    #! /bin/bash
    while read line
    do
        echo $line | cut -c 3
    done
```

12. Display the 2nd  and 7th  character from each line of text.
```bash
    #! /bin/bash
    while read line
    do
        echo $line | cut -c 2,7
    done
```

13. Display a range of characters starting at the  2nd position of a string and ending at the  7th position (both positions included).
```bash
    #! /bin/bash
    while read line
    do
        echo $line | cut -c 2-7
    done
```

14. Display the first four characters from each line of text.
```bash
    #! /bin/bash
    while read line
    do 
        echo $line | cut -c -4
    done
```

15. Given a tab delimited file with several columns (tsv format) print the first three fields.
```bash
    #! /bin/bash
    while read line
    do
        echo -e "$line" | cut -f -3
    done
```
16. Print the characters from thirteenth position to the end.
```bash
    #! /bin/bash
    while read line
    do 
            echo $line | cut -c 13-
    done
```
17. Given a sentence, identify and display its fourth word. Assume that the space (' ') is the only delimiter between words.
```bash
    #! /bin/bash
    while read line
    do
        echo $line | cut -d' ' -f4
    done
```
18. Given a sentence, identify and display its first three words. Assume that the space (' ') is the only delimiter between words.
```bash
    #! /bin/bash
    while read line
    do
        echo $line | cut -d' ' -f1-3
    done     
```
19. Given a tab delimited file with several columns (tsv format) print the fields from second fields to last field.
```bash
    # /bin/bash
    while read line
    do
        echo -e "$line" | cut -f2-
    done
```
20. In this challenge, we practice using the head command to display the first  n lines of a text file.
Display the first  20 lines of an input file
```bash
   cat file |  head -20
```
21. Display the first 20 characters in input file.
```bash
    cat | head -c 20
```
22. Display the lines (from line number 12 to 22, both inclusive) of a given text file.
```bash
    cat | head -n 22 | tail -n +12
```
23. Display last 20 lines of the input file
```bash
    cat | tail -n 20
```
24. Display last 20 characters of the input file
```bash
    cat | tail -c 20
```
25. Replace the all occurances of '()' to '[]' in the file
```bash
    cat | tr "()" "[]"
```
26. In a given fragment of text, delete all the lowercase characters a - z.
```bash
    cat | tr -d '[:lower:]'
```
27. In a given fragment of text, replace all sequences of multiple spaces with just one space.
```bash
    cat | tr -s  " "
```
28. Given a text file, order the lines in lexicographical order.
```bash
    cat | sort -u
```
29. Given a text file, order the lines in reverse lexicographical order (i.e. Z-A instead of A-Z).
```bash
    cat | sort -ru
```
30. You are given a text file where each line contains a number. The numbers may be either an integer or have decimal places. There will be no extra characters other than the number or the newline at the end of each line. Sort the lines in ascending order - so that the first line holds the numerically smallest number, and the last line holds the numerically largest number.
```bash
    cat | sort -n
```