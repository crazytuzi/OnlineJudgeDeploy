# OnlineJudgeDeploy
**gitkraken**	
- https://www.gitkraken.com/download

**vm-tools**
- sudo apt-get install open-vm-tools-desktop -y

**镜像**
- https://mirror.tuna.tsinghua.edu.cn/help/ubuntu/

**python3.6**
- sudo apt-get install software-properties-common
- sudo add-apt-repository ppa:jonathonf/python-3.6
- sudo apt-get update
- sudo apt-get install curl
- curl https://bootstrap.pypa.io/get-pip.py | sudo python3.6

**安装python依赖包**
- sudo pip3 install -r requirements.txt

**卸载通过源码安装的包**
- python setup.py install --record logName
- cat logName | xargs rm -rf

**Mysql**
- sudo apt-get install mysql-server
- sudo service mysql start
- sudo service mysql stop
- 远程访问
	- sudo gedit /etc/mysql/mysql.conf.d/mysqld.cnf
	- 注释bind-address = 127.0.0.1
	- mysql -u root -p
	- grant all on *.* to root@'%' identified by '123456';
	- flush privileges;
	- sudo /etc/init.d/mysql restart

**npm**
- sudo apt-get install npm
- npm install -g cnpm --registry=https://registry.npm.taobao.org
- ln -s /usr/bin/nodejs /usr/bin/node
- npm install n -g
- n stable
- cnpm install -g vue-cli
- cnpm install
- cnpm run dev