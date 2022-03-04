# ssl-tls
Open ssl configuration files


Self signed certification configuration file = openssl.conf

# Create a Certificate using OpenSSL
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout localhost.key -out localhost.crt -config ssl_host.conf

# Viewing the certificate
openssl x509 -in localhost.crt -text
