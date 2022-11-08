# openssl_reinstall
Solve problem on Arch Linux usr/lib/libcrypto.so.3: version `OPENSSL_3.0.0' not found 

Start with su command, run this commands with root privileges

fix **usr/lib/libcrypto.so.3: version `OPENSSL_3.0.0' not found** issue on Arch Linux and derived distributions

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

In case of presenting the same error run **ldconfig /usr/local/lib64/** with root privileges
