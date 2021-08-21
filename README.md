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