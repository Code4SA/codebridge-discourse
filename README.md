Speak Up Mzansi! Discourse Configuration
========================================

This repo stores the speakupmzansi.org.za Discourse configuration. It is expected to be used
with a [https://github.com/discourse/discourse/blob/master/docs/INSTALL-digital-ocean.md](Discourse Docker Image).

To use it, first setup a Docker-based Discourse instance and clone this repo into a directory somewhere.

Edit speakup.yml and set the `DISCOURSE_SMTP_PASSWORD` and `NEW_RELIC_LICENSE_KEY` variables
appropriately.

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
