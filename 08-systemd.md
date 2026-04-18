## Service Control

```
systemctl start (service name)     # start service
systemctl stop  (service name)   # stop service
systemctl restart (service name )   # restart service
systemctl reload (service name )    # reload config
```

## Enable / Disable (Boot)

```
systemctl enable (service name)    # start at boot

systemctl disable (service name)   # stop at boot

systemctl is-enabled (service name) # check

systemctl enable --now (service name) # start a boot with run service )

systemctl mask (service name)  #  * Completely disables service * Even root cannot start it

systemctl unmask (service name)  # * Removes block * Now service can start again

```

## Status & Check

```
systemctl status (service name)
systemctl is-active (service name)
```

## List Services

```
systemctl list-units --type=service
systemctl list-units --type=service --state=running
systemctl --failed
```

## Daemon Reload

```
systemctl daemon-reload
```

## Targets (Runlevels)

```
systemctl get-default
systemctl set-default multi-user.target
systemctl isolate multi-user.target
```

## Power Management 

```
systemctl reboot
systemctl poweroff
systemctl halt
```

## View Service File
```
systemctl cat ( service name )
```

## Logs

```
journalctl -u (service name)
journalctl -xe

```

### Improtant Service to known 

```
sshd → SSH login
httpd → web server
nginx → web server
firewalld → firewall
```
