# SYSTEMCTL-SERVICE-SETUP
### Service files doc root:
```
/etc/systemd/system/
```
### Usual template:
```
[Unit]
Description=<name>

[Service]
User=<user>
ExecStart=/home/<user>/path/to/script.sh
StandardOutput=append:/home/<user>/path/to/output.log

[Install]
WantedBy=multi-user.target
```
### Reload conf and start service:
```
sudo systemctl daemon-reload
sudo systemctl start <service>
```
Optional system autorun:
```
sudo systemctl enable <service>
```
