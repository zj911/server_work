1.rtsp:
tar -xzvf EasyDarwin-linux-8.1.0-1901141151.tar.gz
cd EasyDarwin-linux-8.1.0-1901141151
sudo ./easydarwin

2.rtmp:
tar -zxvf pcre-8.41.tar.gz
tar -zxvf openssl-1.0.2l.tar.gz
unzip nginx-rtmp-module-master.zip
tar -zxvf nginx-1.12.1.tar.gz
tar -zxvf zlib-1.2.11.tar.gz

cd nginx;

./configure --prefix=/usr/local/nginx --with-debug --with-pcre=../pcre-8.41 --with-zlib=../zlib-1.2.11 --with-openssl=../openssl-1.0.2l --add-module=../nginx-rtmp-module-master
cp nginx.conf.rtmp /usr/local/nginx/conf/

error info:
objs/Makefile文件，将第三行的-Werror去掉就可以
