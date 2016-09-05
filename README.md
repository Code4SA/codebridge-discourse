CodeBridge Discourse Configuration
========================================

This repo stores the CodeBridge Discourse configuration. It is expected to be used
with a [Discourse Docker Image](https://github.com/discourse/discourse/blob/master/docs/INSTALL-cloud.md).

To use it, first setup a Docker-based Discourse instance and clone this repo into a directory somewhere (such as `~/codebridge-discourse`).

Edit `speakup.yml` and set these env variables appropriately:

- `DISCOURSE_SMTP_PASSWORD` - password/api key for Mandrill
- `NEW_RELIC_LICENSE_KEY` - new relic license key string

Then link this file into `/var/discourse/containers` and rebuild the app.

```bash
sudo ln -s `pwd`/codebridge.yml /var/discourse/containers/
cd /var/discourse
sudo ./launcher rebuild codebridge
```
