## Raspberry Pi Configuration Scripts

This is a collection of scripts borrowed from [here](https://github.com/jameswhite/raspi) for my single Raspberry Pi setup. It sets up a reverse proxy so that `http://<your-host-or-ip>/camera` will `proxy_pass` through to the port running motion (8081).

### Setup

```bash
cd ~
git clone https://github.com/stephenyeargin/raspberrypi-setup.git
cd raspberrypi-setup/bin
./fix-wifi-drops
./fix-us-keyboard
./install-motion
./install-nginx-camera
```

### Notes

- If you expose your Raspberry Pi to the internet, make sure you turn off SSH Password login (`PasswordAuthentication no` in /etc/ssh/ssh_config`) and change the default password on the machine (`sudo passwd`).
- Your default website is in `/var/www/`
- Your camera is available to be used as an image (see camera.html)
