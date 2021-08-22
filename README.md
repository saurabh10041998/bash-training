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