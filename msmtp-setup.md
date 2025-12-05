# MSMTP-SETUP
## Install:
```
sudo apt install -y msmtp mailutils
```
In the UI choose 'yes'.

## .msmtprc setup:
```
nano .msmtprc
```
### Paste the following:
```
# --- DEFAULT SETTINGS ---
defaults
auth           on
tls            on
tls_starttls   off
tls_trust_file /etc/ssl/certs/ca-certificates.crt
logfile        ~/.msmtp.log

# --- USER EMAIL ACCOUNT ---
account <username>
host <smtp-server>
port <smtp-port>
from <info@email.com>
user <info@email.com>
password <email-account-app-password>

# --- DEFAULT ACCOUNT ---
account default : <username>
```
NB: Might work without it, but if needed, then fix perms with:
```
chmod 600 ~/.msmtprc
```

## Usage:
```
EMAIL="info@email.com"
echo -e "Subject: <subject>\n\n<body>" | msmtp "$EMAIL"
```
