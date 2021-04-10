![CI](https://github.com/x86chi/twitter-github-contribution-graph/workflows/CI/badge.svg)
![cron](https://github.com/x86chi/twitter-github-contribution-graph/workflows/cron/badge.svg)

A client uploading Github contribution graph to Twitter profile banner.

[PREVIEW](https://twitter.com/x86chi)

## Usage

Please generate Twitter app key and token at [Twitter Developer Dashboard](https://developer.twitter.com/en/apps)

### Authorize Twitter app

You can authorize Twitter app to your Twitter account with [Twitter CLI](https://github.com/sferik/t#configuration)

Below command will direct you to a URL where you can authorize to Twitter bot.

```
t authorize
```

### Step 1. Fork this repository

> Forked repository page -> Secrets -> New Secret

Create `CONSUMER_KEY`, `CONSUMER_SECRET`, `ACCESS_TOKEN_KEY`, `ACCESS_TOKEN_SECRET`.

Done. The banner is updating once a day.

### Step 2. Create [`.env`](https://github.com/motdotla/dotenv) file in root directory

write the information upper.

```
CONSUMER_KEY=
# etc...
```

Add your Github username.

```
USERNAME=
```

### Parse only this year

This project support parsing only this year history. It can enable in Github Action.

Please add the `CURRENT_YEAR: true` environment variable in `.github/workflows/cron.yml` if you want this feature.

## License

MIT
