## check file in readble language 

```
ls -lh
```

##  gzip ( compressing the file )

```
gzip (file name)
```

## gunzip ( decompressing the file )

```
gunzip (file name)
```

## compress file 

```
tar -cvf directory.tar directory/

( tar used for combine multiple files ) 
```

##  decompress file 

```
tar -xvf directory.tar.gz

( In this they decompress the folder -x used for extract ) 
```

## single line command compress & decompress the folder

```
tar -czvf  directory.tar.gz directory/

( In the single command combine directory and all sub folder & compress folde )

tar -xzvf  directory.tar.gz directory/

( In the sinlge line command extract the folder & sub files )

tar -tzvf  directory.tar.gz directory/

( check tar compress what is content folder used for this )

```


# zip 

```
zip data.zip a.txt b.txt   -> all files zip

zip -r file.zip folder/   -> zip any folder
```

# unzip 

```
unzip file.zip   -> decompress the file

unzip file.zip -d /path/ -> decompress on specific location

```



 
