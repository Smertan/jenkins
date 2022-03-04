# ssl-tls
Open ssl configuration files


Self signed certification configuration file = openssl_selfsigned.conf

# Create a Certificate using OpenSSL
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout localhost.key -out localhost.crt -config openssl_selfsigned.conf

# Viewing the certificate
openssl x509 -in localhost.crt -text
