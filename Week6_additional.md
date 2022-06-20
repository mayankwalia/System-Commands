### condition-examples.sh
```bash
#!/bin/bash
for i in {1..9}
do
	echo $i
	if [ $i -le 3 ] || [ $i -ge 7 ]
	then
		echo $i is out of range 
	fi
	if [ $i -gt 3 ] && [ $i -lt 7 ]
	then
		echo $i is in the range
	fi
done
```


### 

```bash
#!/bin/bash

if [ $# -lt 2 ]
then
	echo use with two natural naumbers as arguments
	exit 1
fi

re='^[0-9]+$'
if ! [[ $1 =~ $re ]]
then
	echo $1 is not a natural number
	exit 1
fi

if ! [[ $2 =~ $re ]]
then
	echo $2 is not a natural number
	exit 1
fi

let a=$1*$2
echo product a is $a
(( a++ ))
echo product a incremented is $a

let b=$1**$2
echo power is $b

c=$[ $1 + $2 +10]
echo sun+10 is $c

d=$(expr $1 + $2 + 20)
echo sum+20 is $d

f=$(( $1 * $2 * 2 ))
echo product times 2 is $f
```

### 

```bash
#!/bin/bash
set -x
a=256
b=4
c=3

ans=$( expr $a + $b )
echo $ans

ans=$( expr $a - $b )
echo $ans

ans=$( expr $a \* $b )
echo $ans

ans=$( expr $a / $b )
echo $ans

ans=$( expr $a % $b )
echo $ans

ans=$( expr $a \> $b )
echo $ans

ans=$( expr $a \>= $b )
echo $ans

ans=$( expr $a \< $b )
echo $ans

ans=$( expr $a \<= $b )
echo $ans

ans=$( expr $a = $b )
echo $ans

ans=$( expr $a != $b )
echo $ans

ans=$( expr $a \| $b )
echo $ans

ans=$( expr $a \& $b )
echo $ans

str="octavio version as in Jan 2022 is 6.4.0"
reg="[oO]ctav[aeiou]*"
ans=$( expr "$str" : $reg )
echo $ans

ans=$( expr substr "$str" 1 6 )
echo $ans

ans=$( expr index "$str" "vw" )
echo $ans

ans=$( expr length "$str" )
echo $ans
```

###
```bash
#!/bin/bash
a=2.5
b=3.2
c=4
d=$(bc -l << EOF
scale=5
($a+$b)^$c
EOF
)
echo $d
```


```bash

#!/bin/bash
set -x
echo path is set as $PATH
i=0
IFS=:
for n in $PATH
do
	echo $i $n
	(( i++ ))
done

```
