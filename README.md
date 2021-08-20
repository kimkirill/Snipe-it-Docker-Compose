# Snipe-it-Docker-Compose
Этот репозиторий для запуска snipe-it в Docker.
Для запуска воспользуйтесь командой
```bash
docker-compose up
```

Вы должны создать файл .env в корневой директории со следующими параметрами:
```bash
# Mysql Parameters
MYSQL_PORT_3306_TCP_ADDR=snipe-mysql
MYSQL_ROOT_PASSWORD=YOUR_ROOT_PW
MYSQL_DATABASE=snipeit
MYSQL_USER=snipeit
MYSQL_PASSWORD=snipeit

# Email Parameters
# - the hostname/IP address of your mailserver
MAIL_PORT_587_TCP_ADDR=smtp.example.com
#the port for the mailserver (probably 587, could be another)
MAIL_PORT_587_TCP_PORT=587
# the default from address, and from name for emails
MAIL_ENV_FROM_ADDR=ex@email.com
MAIL_ENV_FROM_NAME=Your Name
# - pick 'tls' for SMTP-over-SSL, 'tcp' for unencrypted
MAIL_ENV_ENCRYPTION=tls
# SMTP username and password
MAIL_ENV_USERNAME=your_username
MAIL_ENV_PASSWORD=your_email_pw

# Snipe-IT Settings
APP_ENV=production
APP_DEBUG=false
APP_KEY={{INSERT_API_TOKEN}}
APP_URL=http://127.0.0.1:80
APP_TIMEZONE=Europe/London # you should change this to your timezone
APP_LOCALE=en # you should change this for the desired language
```

# API key
