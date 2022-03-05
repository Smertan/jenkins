# ssl-tls
Open ssl configuration files


Self signed certification configuration file = openssl_selfsigned.conf

# Create a Certificate using OpenSSL

The code below creates a self signed certificate and outputs them in the desired location.

---
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/nginx-selfsigned.key -out /etc/ssl/certs/nginx-selfsigned.crt -config openssl_selfsigned.conf
---

# Viewing the certificate
openssl x509 -in localhost.crt -text

# self-signed.conf location

The file lets Nginx know of the location of the certificate and key. It should be placed in the following directory /etc/nginx/snippets/
