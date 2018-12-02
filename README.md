# dobby18bot
telegram bot for dobby's learning
```
[Unit]
Description=Bot Daemon for Dobby
After=dobby-bot.service

[Service]
User=pi
Group=www-data
WorkingDirectory=/home/pi/dobby-bit
ExecStart=/home/pi/ocv/venv/bin/python dobby-bot.py
ExecReload=/bin/kill -s HUP $MAINPID
ExecStop=/bin/kill -s TERM $MAINPID

[Install]
WantedBy=multi-user.target
```