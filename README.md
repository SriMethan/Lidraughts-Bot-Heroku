# lidraughts-bot

The code template to make a Lidraughts Bot and deploy it to heroku server easily.
This is the code of [@libot](https://lidraughts.org/@/libot) and similar heroku run bots in [lidraughts.org](https://lidraughts.org)

Engine communication code taken from https://github.com/AttackingOrDefending/lidraughts-bot by [AttackingOrDefending](https://github.com/AttackingOrDefending)

### Draughts Engine

- [Scan 3.1(dev)](https://github.com/rhalbersma/scan)

### Heroku Buildpack

- [`heroku/python`](https://elements.heroku.com/buildpacks/heroku/heroku-buildpack-python)

### Heroku Stack

- [`heroku-20`](https://devcenter.heroku.com/articles/heroku-20-stack) (allowing a maximum hash size of 512 mb)

### How to Use

- [Fork](https://github.com/SriMethan/Lidraughts-Bot-Heroku/fork) this repository.
- Edit only your token in the `config.yml` file over [here](/config.yml#L1).
- Create a [new heroku app](https://dashboard.heroku.com/new-app).
- Go to the `Deploy` tab and click `Connect to GitHub`.
- Click on `search` and then select your fork of this repository.
- Then `Enable Automatic Deploys` and then select the `main` branch (which is already done by default usually) and Click `Deploy`.
- Once it has been deployed, go to `Resources` tab on heroku and enable `worker (bash startbot.sh)` dynos. (Do note that if you don't see any dynos in the `Resources` tab, then you must wait for about 5 minutes and then refresh your heroku page.)
- Finally go to your `Settings` tab and then under `Config Vars` click on `Reveal Config Vars` and then in the place of `key` type in `LIDRAUGHTS_BOT_TOKEN` and in the place of `value` add your Lidraughts bot token

 

You're now connected to lidraughts and awaiting challenges! Your bot is up and ready!
### Important Ways to handle the bot 
When you dont monitor the bot turn of the dynos or the bot will crash and when you closing the computer but the bot is on turn off dynos then the bot would not loose the conection to heroku... If there is this error 2021-10-08T06:50:53.054476+00:00 heroku[worker.1]: Process running mem=688M(133.6%)
2021-10-08T06:50:53.055929+00:00 heroku[worker.1]: Error R14 (Memory quota exceeded)
Then you have to restart the dynos if there is same errors after dynos then you have to redelte the repo and fork it again
The bot will play 1 game at a time if two games tehn bot have chances to crash so be carefull . 

# Copying
For Copying the heroku codes see [here](https://github.com/SriMethan/Lidraughts-Bot-Heroku/blob/main/Copying.txt)

## Acknowledgements
This code exsit because of [Attackingordefending's bot client](https://github.com/Attackingordefending/lidraughts-bot) 
