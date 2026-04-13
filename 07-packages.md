# 📦 Linux Package Management (RHCSA Notes)

---

# 🧠 What is Package Management?

👉 Package = software (nginx, httpd, git)
👉 Package Manager = tool to install/update/remove software

👉 In RHEL-based systems:

* `dnf` (new, used in RHCSA)
* `yum` (old)

---

# 🔹 1. Install Package

```bash
sudo dnf install httpd
```

👉 Installs Apache web server + dependencies

---

# 🔹 2. Remove Package

```bash
sudo dnf remove httpd
```

👉 Uninstalls package

---

# 🔹 3. Update Packages

```bash
sudo dnf update
```

👉 Updates all packages

```bash
sudo dnf update httpd
```

👉 Updates specific package

---

# 🔹 4. Search Package

```bash
dnf search nginx
```

👉 Search available packages

---

# 🔹 5. Package Info

```bash
dnf info nginx
```

👉 Shows:

* version
* size
* repo

---

# 🔹 6. List Installed Packages

```bash
dnf list installed
```

---

# 🔹 7. Check if Installed

```bash
dnf list installed | grep nginx
```

---

# 🔥 8. Repositories (Very Important)

👉 Repo = source from where packages are downloaded

---

## 🔍 Check Repo List

```bash
dnf repolist
```

---

## 📂 Repo Files Location

```bash
/etc/yum.repos.d/
```

---

## 🧾 Sample Repo File

```ini
[AppStream]
name=AppStream Repo
baseurl=http://example.com/repo
enabled=1
gpgcheck=1
```

---

# ⚠️ Important Exam Points

* RHCSA uses `dnf`
* Internet may NOT be available → local repo needed
* Must know:

  * enable/disable repo
  * install package from repo

---

# 🔄 yum vs dnf

| Feature  | yum | dnf |
| -------- | --- | --- |
| Old tool | ✔   | ❌   |
| New tool | ❌   | ✔   |
| RHCSA    | ❌   | ✔   |

---

# 💻 macOS vs RHEL

| System | Package Manager |
| ------ | --------------- |
| macOS  | brew            |
| RHEL   | dnf             |

---

# 🧪 Practice Commands

```bash
dnf search nginx
sudo dnf install nginx
dnf info nginx
dnf list installed | grep nginx
sudo dnf remove nginx
```

---

# 🧠 Key Concepts

* Package = software
* Repo = software store
* dnf = install/update/remove tool

---

# 🇲🇷 Marathi Recap

* package = software
* repo = store
* dnf = install/update/remove

---

# 🎯 Final Goal

✔ Install package
✔ Remove package
✔ Update system
✔ Work with repos

---
