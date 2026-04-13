# Process Management 

## 1 ps ( Process list ) 
```
ps (check running ps)
ps aux (check in details)
ps aux | grep sleep  ( used for check process id )
ps -o pid,ni,comm -p 1234 ( direct check PID,Nice value, command )
```

## 2 top
```
top (live monitor)
```

## 3 kill (Stop process)
```
kill PID
kill -9 PID
```

## 4 background process 
```
sleep 500 & (start this process for 500 second)
nice -n 10 sleep 1000 & ( create a job with direct nice value )
```

## 5 jobs (list jobs)
```
jobs (check all running stop terminate job)
```

## 6 foreground
```
fg %1 (job ko terminal pe running karna )
```

## 7 Background (resume)
```
bg %1 (job ko termina; ke background me run karna)
```

## 8 Suspend process 
```
ctrl + z
```

## 9 Kill vs Suspend
```
Ctrl + C → process terminate ❌
Ctrl + Z → process pause ⏸️
```

## 10 nice ( add time priority )
```
nice -n 10 sleep 300 &
```
## 11 renice (change running process priority)
```
renice 5 -p PID
```
>> -20 → highest priority
>>  19 → lowest priority




