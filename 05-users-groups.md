# Linux User Management  

* Create user

```
sudo useradd username
```

* Set password

```
sudo passwd username
```

* Delete user

```
sudo userdel username
```

* Check userinfo

```
id username 
```

* Check List all users

```
cat /etc/passwd
```

# Linux Group Management 

* Create group

```
sudo groupadd (gropuname )
```

*  Delete group

```
sudo groupdel (groupname)

```

* Modify group name

```
sudo groupmod -n newname oldname

```

*  Add user to group

```
sudo usermod -aG  groupname username

```

* Remove user from group

```
sudo gpasswd -d username groupname

```

* Check group

```
> groups username

> getent group

```

* Modify user ( add to group )

```
sudo usermod -aG groupname username
```

*  Check user groups

```
groups username
```

* Switch User

```
su - username
```

* Check how many groups exist in linux

** Method 1 

```
cat /etc/group | wc -l
```

** Method 2 

```
getent group | wc -l  ( direct give no. how many groups exist ) 
