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

# Install Yarn on CentOS 7
1. If you don't have Node.js installed on your system, you need to enable the Nodesource repository with the following curl command:
```
curl --silent --location https://rpm.nodesource.com/setup_10.x | sudo bash -
```
2. After that, install the Node.js package using the following command:
```
yum install nodejs
```

3. There is consistent maintenance of the official Yarn repository. It further, provides the most up-to-date version. To enable the Yarn repository and import the repository’s GPG key, run the below commands:
```
curl --silent --location https://dl.yarnpkg.com/rpm/yarn.repo | sudo tee /etc/yum.repos.d/yarn.repo
sudo rpm --import https://dl.yarnpkg.com/rpm/pubkey.gpg
```
4. After the addition of the repository, install Yarn by running the following command:
```
yum install yarn
```
5. Now, run the below command to confirm if yarn is installed successfully:
```
yarn --version
```

# Install pm2 on CentOS 7
```
yum install npm
npm install pm2 -g
pm2 status
```
