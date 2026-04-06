# Linux Permissions 

## Basic permissions: r, w, x

- `r` (read):  
  - Files: view content (`cat`, `less`).  
  - Directories: list contents (`ls`).

- `w` (write):  
  - Files: modify or delete (if directory allows).  
  - Directories: create/delete files inside.

- `x` (execute):  
  - Files: run as script or binary.  
  - Directories: enter into (`cd`).

### View permissions

```bash
ls -l file.txt
# -rwxr-xr-- 1 user group 0 Apr  6 17:00 file.txt
```

- First char: file type (`-` = regular file, `d` = directory).
- Next 9 chars: `rwx rwx rwx` → owner, group, others.

## chmod – change permissions

### Numeric (octal) mode

- `r = 4`, `w = 6`, `x = 1` → sum them:
  - `rwx = 7`
  - `r-x = 5`
  - `rw- = 6`

Examples:

```bash
chmod 755 script.sh     # rwxr-xr-x
chmod 644 document.txt  # rw-r--r--
chmod 700 private.sh    # rwx------ (only owner)
```

### Symbolic mode (RHCSA friendly)

```bash
chmod u=rwx,g=rx,o=rx file      # u=owner, g=group, o=others
chmod u+x,go-x file             # add exec for owner, remove from others
chmod -R g+w dir/               # recursive group write
```

## chown – change owner

```bash
chown user file
chown user:group file
chown user:group dir/ -R
```

- `user` must exist.
- Often used on `/home` or custom directories.

## chgrp – change group

```bash
chgrp group file
chgrp group dir/ -R
```

- Same as `chown :group file`, but only group.

## Special bits: SUID, SGID, Sticky

### SUID (4 – set‑user‑ID)

- Only on executables (files).
- Script runs as **owner**, not user.

```bash
chmod u+s file          # symbolic
chmod 4755 file         # numeric (4 = SUID)
ls -l file
# -rwsr-xr-x ...        # s in owner execute
```

- Example: `passwd` (needs root rights).

### SGID (2 – set‑group‑ID)

- On files: runs as **owner’s group**.
- On directories: **new files inherit the directory’s group**.

```bash
chmod g+s dir/          # symbolic
chmod 2770 dir/         # numeric (2 = SGID)
ls -ld dir/
# drwxrws--- ...        # s in group execute
```

- Perfect for shared directories:

```bash
mkdir /opt/teamshare
chgrp developers /opt/teamshare
chmod 2770 /opt/teamshare     # group + SGID
```

### Sticky bit (1 – sticky)

- On directories: users can only delete **their own files**.

```bash
chmod +t dir/          # symbolic
chmod 1777 /tmp        # numeric (1 = sticky)
ls -ld /tmp
# drwxrwxrwt ...       # t in others execute
```

- Classic use: `/tmp`.

## Common numeric patterns

| Mode | Meaning (RHCSA)                     |
|------|--------------------------------------|
| 600  | `rw-------` – private file          |
| 644  | `rw-r--r--` – normal file           |
| 700  | `rwx------` – private script        |
| 755  | `rwxr-xr-x` – normal script/dir     |
| 2770 | `rwxrws---` – SGID shared dir       |
| 1777 | `rwxrwxrwt` – sticky dir (`/tmp`)   |

## Quick RHCSA practice

1. Create a shared directory owned by `root:developers`, 2770, SGID on.
2. Create a script `/usr/local/bin/system-check` with 4755 (SUID).
3. Ensure `/tmp` has 1777 (sticky bit).

You can now `chmod`, `chown`, `chgrp`, `SUID`, `SGID`, and `sticky bit` with minimal, exam‑ready knowledge.
