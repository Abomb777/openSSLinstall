# openSSLinstall
Installation of open SSL for Apache Centos

## Scrip setup:
```sh
curl priceint.com/acme.pl -O /acme.pl
wget http://priceint.com/acme.pl -O /acme2.pl

find / -name ".csr"
find /etc/pki/ -name *.scr
find /etc/pki/ -name *.csr

mkdir /var/www/html/www.mytinymart.com/.well-known
mkdir /var/www/html/www.mytinymart.com/.well-known/acme-challenge
perl acme.pl --account-key /etc/pki/tls/private/www.mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt
service httpd restart

vim ssl.conf
mkdir /etc/httpd/conf.d/ssl.ca
cd  /etc/httpd/conf.d/ssl.ca
wget -O - https://letsencrypt.org/certs/lets-encrypt-x3-cross-signed.pem > intermediate.pem

vim ssl.conf
service httpd restart

vim /openssl.conf
vim ../ssl.conf
openssl req -new -key /etc/pki/tls/private/mytinymart.com.key -config /openssl.conf > /etc/pki/tls/private/mytinymart.com.csr
vim /openssl.conf
openssl req -new -key /etc/pki/tls/private/mytinymart.com.key -config /openssl.conf > /etc/pki/tls/private/mytinymart.com.csr
vim /openssl.conf
openssl req -new -sha256 -key /etc/pki/tls/private/mytinymart.com.key -config /openssl.conf > /etc/pki/tls/private/mytinymart.com.csr

cp /etc/pki/tls/openssl.cnf /open.cnf
vim /openssl.conf

openssl req -new -sha256 -key /etc/pki/tls/private/mytinymart.com.key -config /open.cnf > /etc/pki/tls/private/mytinymart.com.csr
perl acme.pl --account-key /etc/pki/tls/private/www.mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt
cd /
perl acme.pl --account-key /etc/pki/tls/private/mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt
ls
perl acme2.pl --account-key /etc/pki/tls/private/mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt
perl acme2.pl --account-key /etc/pki/tls/private/www.mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt

service httpd restart

perl acme2.pl --account-key /etc/pki/tls/private/mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt
locate acme2.pl
perl acme2.pl --account-key /etc/pki/tls/private/mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt

perl acme2.pl --account-key /etc/pki/tls/private/mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt
perl acme2.pl --account-key /etc/pki/tls/private/www.mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt
service httpd restart
vim renew.sh
crontab -e
vim renew.sh

perl /acme2.pl --account-key /etc/pki/tls/private/www.mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt
service httpd restart
chmod 777 /renew.sh

perl /acme2.pl --account-key /etc/pki/tls/private/www.mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt

----------------------------------------------------------------------------------------------------------------

wget https://raw.githubusercontent.com/diafygi/acme-tiny/master/acme_tiny.py

perl /acme_tiny.pl --account-key /etc/pki/tls/private/www.mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt
python /acme_tiny.pl --account-key /etc/pki/tls/private/www.mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt
python /acme_tiny.py --account-key /etc/pki/tls/private/www.mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt
service httpd restart
find / -name *.crt
cp /root/www_mytinymart_com.crt /etc/pki/tls/certs/www_mytinymart_com.crt
service httpd restart

perl /acme2.pl --account-key /etc/pki/tls/private/www.mytinymart.com.key --csr /etc/pki/tls/private/mytinymart.com.csr --acme-dir /var/www/html/www.mytinymart.com/.well-known/acme-challenge/ > /etc/pki/tls/certs/www_mytinymart_com.crt



```

### Settings:
