1. print HELLO on cmd
```
    echo "HELLO" 
```
```
    awk 'BEGIN { print "HELLO" }'     OR    awk 'END { print "HELLO" }'
```

2. print odd number from 1 to 100
```
    seq 1 2 100
```
3. Write a Bash script which accepts  name as input and displays the greeting "Welcome (name)"
```
    read first_name
    echo "Welcome $first_name
```