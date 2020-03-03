# Intercom Reverse Proxy on Heroku

Run a reverse ssl termination proxy using nginx on Heroku so that you can use a custom domain with Intercom in the simpliest possible way. Yes, you still need to setup the SSL but Heroku's ACM makes that easy and you'll need a CNAME/ALIAS record but still, this is much easier than mucking around.

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

## Installation

- Use the [Deploy to Heroku](https://heroku.com/deploy) button above to create a
copy of the app, then configure the CUSTOM_DOMAIN config variable.
- Add a credit card, upgrade to a paid dyno (hobby).
- Enable ACM (Let's Encrypt certificate managed completely by Heroku).
- Add your custom domain to the new Heroku app and add the related CNAME DNS record. I highly recommend [DNSimple](https://dnsimple.com/r/811f4af066782e)
- Wait (for the gerbils).
- Bingo.

## Config Variables

* `CUSTOM_DOMAIN` - should be your domain (no scheme) that you set in the Intercom Help Center Settings. Eg. support.yourdomain.com

![help center domain on intercom](https://i.imgur.com/cZFCSsF.jpg)

## Credits

Updated to heroku-16 stack and recent community build pack for nginx.

Based on [funwhilelost/heroku-reverse-proxy](https://github.com/funwhilelost/heroku-reverse-proxy) who at least had something that wasn't based on cedar.

[![Support via PayPal](https://cdn.rawgit.com/twolfson/paypal-github-button/1.0.0/dist/button.svg)](https://www.paypal.me/kori/)
