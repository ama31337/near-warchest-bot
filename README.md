## Description [EN]

near-warchest-bot is a script for [NEAR](https://near.org/) validators that manage your validator seat and maintain its number to one. It keeps logs, determines the reason for kicked out from the validator list, pings the pool.

## Installation

### Installation of Dependency

```sudo apt update```

```sudo apt install python3 git curl jq```

You should also have installed [near-cli](https://github.com/near/near-cli), and [logged](https://github.com/nearprotocol/stakewars/blob/master/challenges/challenge001.md#1connect-near-cli-to-your-betanet-wallet) in to your account 

### Installation of near-warchest-bot

```git clone https://github.com/savelev1/near-warchest-bot.git /home/$USER/near-warchest-bot```

near-warchest-bot will install in the directory */home/$USER/near-warchest-bot*. You can change it at your discretion.

Open the directory where the script is installed and create an config.json file from the config.example.json:

```cd /home/near/near-warchest-bot && cp config.example.json config.json```

Edit config.json

### Setting the start of near-warchest-bot at 30 minutes intervals

Put in crontab and use absolute path for $USER

```*/30 * * * * /usr/bin/python3 /home/$USER/near-warchest-bot/near-warchest-bot.py >> /home/$USER/near-warchest-bot/warchest.log 2>&1```

**✅Installation completed**

You can run the script manually to make sure that everything works:

```python3 /home/$USER/near-warchest-bot/near-warchest-bot.py```

The logs are in the near-warchest-bot.log file in the same directory.

### Update near-warchest-bot

Go to the script directory and pull out the updates:

```cd /home/$USER/near-warchest-bot && git pull```
