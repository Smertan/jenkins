# OpenSSL default configuration file for creation

The self signed certification configuration file is **openssl_selfsigned.conf**. When creating a new set of keys it can be used using the -config option as shown below. Editing the file as required i.e., altnames IP.1 IP address


# Create a Certificate using OpenSSL

The code below creates a self-signed certificate and outputs them in the desired location.

```
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/nginx-selfsigned.key -out /etc/ssl/certs/nginx-selfsigned.crt -config openssl_selfsigned.conf
```

# Viewing the certificate
```
openssl x509 -in localhost.crt -text
```

# self-signed.conf Nginx location

The file lets Nginx know the location of the certificate and key. It should be placed in the following directory /etc/nginx/snippets/
