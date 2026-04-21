// Multiplication table using for loop
for i in {1..10}
do
  result=$((num * i))
  echo "$num x $i = $result"
done

// Print 1 to 5 no. using while loop
i=1
while [ $i -le 5 ]
do
  echo $i
  i=$((i + 1))
done

// until loop
i=1
until [ $i -gt 5 ]
do
  echo $i
  i=$((i + 1))
done

// Sum of n numbers
sum=0
i=1

while [ $i -le $n ]
do
  sum=$((sum + i))
  i=$((i + 1))
done

// factorial
fact=1
i=1

while [ $i -le $n ]
do
  fact=$((fact * i))
  i=$((i + 1))
done

// prime or not
flag=0

for ((i=2; i<=n/2; i++))
do
  if [ $((n % i)) -eq 0 ]
  then
    flag=1
    break
  fi
done
