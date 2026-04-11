# Linux Text Processing  


## Create text file using command 

```
echo -e "Ram\nShyam\nPratik\nDev" > aniket.txt
```

>> See output

```
cat aniket.txt
```


## 1 grep command 

```
grep "Ram" aniket.txt
grep -i "Dev" aniket.txt (-i used for case sensitive )
```
>> this input avilable in text file then they show



## 2 cut command 

```
echo "aniket,11,devops,22 > info.csv
```

```
check output using this command :
> cut -d "," -f1 info.csv
> cut -d "," -f2 info.csv
```


## 3  awk command 

```
awk '{print $1}' data.txt

( print first column )
```

```
awk 'END {print NR }' data.txt

( print size of .txt file)
```


## 4 sed command  ( used for replace word any version language many usage )

```
sed 's/apple/mango/' data.txt
( In this apple will be replace by mango )

sed 's/apple/mango/g' data.txt
( In this in last 'g' used then in this all apple will be replace by mango )
```


## 5 Sort command ( basically they used for alphabectical order ) 

```
sort data.txt ( In this normal sorting they a-z alphabtes )

sort -r data.txt ( In this they sort reverse z-a alphabtes )
```

## 6 uniq command 

 >> This command basically give in output only original value remove duplicates

```
sort data.txt | uniq ( In this command only show uniq value but rule is value are adjacent means ex . ved ved , dev dev like this )

uniq data.txt (show only original values)
 
sort data.txt | uniq -c ( In this they calculate duplicates value of data )

sort data.txt | uniq -d ( This command show duplicates value )

sort data.txt | uniq -u ( This command show uniq value )

```

## 7 Redirection 

```
echo "Linux" > file.txt ( This command create a file and add text 

echo "devops" > file.txt ( I this you add new content and remove indirectly old content )

echo "DevOps" >> file.txt ( I this using ">>" app new content with exsiting content )
```

## 8 Pipe (|) 

>> Pipe command basically find to two or more output in command
>> { | } This command basically connect next command

>> ex :

```
cat data.txt | grep "banana" > 1.file show  data.txt 2. find banana in .txt file

sort data.txt | uniq  > arrange to words of data.txt & remove duplicates using in uniq
```






