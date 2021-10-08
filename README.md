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
- Finally go to your `Settings` tab and then under `Config Vars` click on `Reveal Config Vars` and then in the place of `key` type in `LIDRAUGHTS_BOT_TOKEN` and in the place of `value` add your Lichess Bot Token.

You're now connected to lidraughts and awaiting challenges! Your bot is up and ready!

# Copying
For Copying the heroku codes see [here](https://github.com/SriMethan/Lidraughts-Bot-Heroku/blob/main/Copying.txt)

## Acknowledgements
This code exsit because of [Attackingordefending's bot client](https://github.com/Attackingordefending/lidraughts-bot) 
