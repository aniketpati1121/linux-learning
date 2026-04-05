# Linux User Management   

# 👤 What is a User?

👉 A **user** is an identity in Linux system.

## 📌 Purpose:
- Login into system  
- Run commands/programs  
- Own files & processes  

## 🧠 Example:
- `aniket` → your account  
- `root` → admin user (full control)  

## 📌 Marathi:
👉 User म्हणजे system मध्ये login करणारी ओळख (identity)  
तो files create करतो, commands run करतो  


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
--- 

# Linux Group Management  

# 👥 What is a Group?

👉 A **group** is a collection of users  

## 📌 Purpose:
- Manage permissions easily  
- Share access to files/resources  

## 🧠 Example:
- `devops` group → multiple users inside  
- All users can access same files  

## 📌 Marathi:
👉 Group म्हणजे users चा set  
permissions manage करायला easy होतं 


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
