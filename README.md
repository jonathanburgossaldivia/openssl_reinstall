# openssl_reinstall
Solve problem on arch linux usr/lib/libcrypto.so.3: version `OPENSSL_3.0.0' not found 

```
cd /usr/src
wget https://www.openssl.org/source/openssl-3.0.7.tar.gz
tar -zxf openssl-3.0.7.tar.gz
cd openssl-3.0.7
./config
make
make install
mv /usr/bin/openssl /root/
ln -s /usr/local/bin/openssl /usr/bin/openssl
ldconfig /usr/local/lib64/
openssl version
```
