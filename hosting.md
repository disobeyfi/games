# Hosting

## Formats

For hosting-as-a-service, the following formats are supported:

* Docker image / Dockerfile
  * with all the necessary instructions for building and installation
  * docker-compose.yml helps a ton
  * If you use docker compose, remember "restart: unless-stopped"
* Ansible playbook / shell script with reasonable documentation which installs the challenge on a server where we have root access to.
  * The supported platforms are current releases of Ubuntu, Centos Stream, Rocky Linux, and Debian.
* Virtual machine image
  * **If you’re planning this, please contact us for more details!**
  * The image needs to be in RAW format usually ending with the .img extension.
    * This means that e.g. VMware images do not work as-is.
    * Many image formats can be converted to the RAW format with a tool such as qemu-img.
    * Also, the image needs to be set up to obtain its IP address via DHCP and it might be useful for us to have some means of logging in.

## Hosting your own

If you want, you can host the challenge (or parts of it) yourself. At your own risk of course. You are also responsible for all the related communication with for example your hosting provider.

## Domain names

* To avoid extra work when hunting for errors, we support custom domain names only within the **dissi.fi** domain.
  * Entirely made up domains using split-horizon DNS do not tend to work anymore due to DNS over HTTPS.
* As an exception, you may use your own public DNS domain if you host the challenge yourself on the internet.
