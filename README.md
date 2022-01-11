# mysql++OnPower
Download mysql++ Source Code Release Tarball from 
https://tangentsoft.com/mysqlpp/releases/mysql++-3.3.0.tar.gz

# Build mysql++
tar xzf mysql++-3.3.0.tar.gz

cd /home/soft/mysql++-3.3.0

CC=gcc \
CXX=g++ \
CFLAGS="-O3 -mcpu=native -mtune=native" \
CXXFLAGS="-O3 -mcpu=native -mtune=native" \
./configure --prefix=/opt/mysql++ \
  --with-mysql=/opt/mysql/bin \
  --with-mysql-lib=/opt/mysql/lib --with-mysql-include=/opt/mysql/include  2>&1 | tee config.log    
  
make -j8 && make install 
