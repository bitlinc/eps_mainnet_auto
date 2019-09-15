[Unit]
Description=Electrum Personal Server Mainnet
After=bitcoind_mainnet.service

[Service]
ExecStart=/usr/bin/python3 /home/bitcoin/.local/bin/electrum-personal-server /home/bitcoin/eps_mainnet/electrum-personal-server/config.ini
User=bitcoin
Group=bitcoin
Type=simple
KillMode=process
TimeoutSec=60
Restart=always
RestartSec=60

[Install]
WantedBy=multi-user.target
