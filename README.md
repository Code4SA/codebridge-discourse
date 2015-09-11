Speak Up Mzansi! Discourse Configuration
========================================

This repo stores the speakupmzansi.org.za Discourse configuration. It is expected to be used
with a [Discourse Docker Image](https://github.com/discourse/discourse/blob/master/docs/INSTALL-cloud.md).

To use it, first setup a Docker-based Discourse instance and clone this repo into a directory somewhere (such as `~/speakup-discourse`).

Edit `speakup.yml` and set these env variables appropriately:

- `DISCOURSE_SMTP_PASSWORD` - password/api key for Mandrill
- `NEW_RELIC_LICENSE_KEY` - new relic license key string
- `MAILCHIMP_API_KEY` - API key for mailchimp integration
- `MAILCHIMP_LIST_ID` - ID of the list to subscribe new users to

Then link this file into `/var/discourse/containers` and rebuild the app.

```bash
sudo ln -s `pwd`/speakup.yml /var/discourse/containers/
cd /var/discourse
sudo ./launcher rebuild speakup
```

Domains
-------

Speak Up Mzansi has a primary domain of speakupmzansi.org.za and also supports
these domains (which will redirect to the primary domain):

* speakup.org.za
* speakupmzansi.co.za
* speakupmzansi.org
