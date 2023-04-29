# Install node on Centos 7

1. On your server, use wget and paste the link that you copied in order to download the archive file:
```
wget https://nodejs.org/dist/v14.19.3/node-v14.19.3.tar.gz
```

2. Extract the archive and move into the new directory by typing
```
tar xzvf node-v* && cd node-v*
```

3. There are a few packages that we need to download from the CentOS repositories in order to compile the code. Use yum to get these now:
```
yum install gcc gcc-c++
```

4. Now, we can configure and compile the software:
```
./configure
make
```

5. The compilation will take quite awhile. When it is finished, you can install the software onto your system by typing:
```
make install
```

6. To check that the installation was successful, you can ask Node to display its version number:
```
node --version
```
