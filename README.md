# Intercom Reverse Proxy on Heroku

Run a reverse ssl termination proxy using nginx on Heroku so that you can use a custom domain with Intercom in the simpliest possible way.

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

## Installation

- Use the [Deploy to Heroku](https://heroku.com/deploy) button above to create a
copy of the app, then configure the UPSTREAM_SERVER and CUSTOM_DOMAIN config variables.

- Add a credit card, upgrade to a paid dyno (hobby).
- Enable ACM (Let's Encrypt certificate managed completely by Heroku).
- Add your custom domain to the new Heroku app and add the related CNAME DNS record.
- Wait (for the gerbils).
- Bingo.

## Config Variables

* `UPSTREAM_SERVER` - should be https://custom.intercom.help:443
* `CUSTOM_DOMAIN` - should be your domain (no scheme). Eg. support.yourdomain.com

## Credits

Updated to heroku-16 stack and recent community build pack for nginx.

Based on [octoberswimmer/heroku-reverse-proxy](https://github.com/octoberswimmer/heroku-reverse-proxy),
originally forked from [api-proxy-3scale-heroku](https://github.com/Taytay/api-proxy-3scale-heroku).
