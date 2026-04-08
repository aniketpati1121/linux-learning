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

## 3 


