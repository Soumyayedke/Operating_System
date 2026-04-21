#!/bin/bash
# This is a simple Hello World script
echo "Hello, World!"

#!/bin/bash
echo "Enter your name:"
read name
echo "Hello, $name!"

#!/bin/bash
echo "Enter two numbers:"
read a b
echo "You entered: $a and $b"

#!/bin/bash
# Taking input
read -p "Enter your name: " name
read -p "Enter your age: " age
# Printing output
echo "Your name is: $name"
echo "Your age is: $age"

#!/bin/bash
# Taking input
read -p "Enter first number: " num1
read -p "Enter second number: " num2
# Comparing numbers
if [ $num1 -gt $num2 ]
then
    echo "$num1 is greater than $num2"
else
    echo "$num2 is greater than or equal to $num1"
fi

#!/bin/bash
# Taking input
read -p "Enter first number: " a
read -p "Enter second number: " b
read -p "Enter third number: " c
# Nested if-else to find largest
if [ $a -gt $b ]
then
    if [ $a -gt $c ]
    then
        echo "$a is the largest number"
    else
        echo "$c is the largest number"
    fi
else
    if [ $b -gt $c ]
    then
        echo "$b is the largest number"
    else
        echo "$c is the largest number"
    fi
fi

#!/bin/bash
read -p "Enter country name: " country
echo "Country name is: $country"

#!/bin/bash
# Take input
read -p "Enter your age: " age
# Check and print
if [ $age -gt 0 ]
then
    echo "Your age is: $age"
else
    echo "Invalid age entered"
fi

#!/bin/bash
read -p "Enter first number: " a
read -p "Enter second number: " b
sum=$((a + b))
echo "Addition = $sum"

#!/bin/bash
read -p "Enter first number: " a
read -p "Enter second number: " b
sub=$((a - b))
echo "Subtraction = $sub"

#!/bin/bash
read -p "Enter first number: " a
read -p "Enter second number: " b
mul=$((a * b))
echo "Multiplication = $mul"

#!/bin/bash
read -p "Enter first number: " a
read -p "Enter second number: " b
if [ $b -eq 0 ]
then
    echo "Division by zero not allowed"
else
    div=$((a / b))
    echo "Division = $div"
fi

#!/bin/bash
# Read number from user
read -p "Enter a number: " num
# Check even or odd
if [ $((num % 2)) -eq 0 ]
then
    echo "$num is even"
else
    echo "$num is odd"
fi

#!/bin/bash
# Read year from user
read -p "Enter a year: " year
# Check leap year
if [ $((year % 400)) -eq 0 ]
then
    echo "$year is a leap year"
elif [ $((year % 100)) -eq 0 ]
then
    echo "$year is not a leap year"
elif [ $((year % 4)) -eq 0 ]
then
    echo "$year is a leap year"
else
    echo "$year is not a leap year"
fi

#!/bin/bash
# Read marks from user
read -p "Enter your marks: " marks
# Check grade
if [ $marks -ge 75 ]
then
    echo "Distinction"
elif [ $marks -ge 65 ]
then
    echo "First Division"
elif [ $marks -ge 55 ]
then
    echo "Second Division"
else
    echo "Third Division"
fi
