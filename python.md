# python
###### check python

- ls /usr/local/lib | grep python
- which python3
- whereis python3
- type python3

###### install python old version
- sudo apt install build-essential
- mkdir -p ~/test/python-source
- wget -P ~/test/python-source [Python3.7](http://www.python.org/ftp/python/3.7.5/Python-3.7.5.tgz)
- cd ~/test/python-source
- tar xvzf Python-3.7.5.tgz
- cd Python-3.7.5
- ./configure --enable-optimizations
- sudo make altinstall

<!-- to make it global -->
- type -a python3.7
- sudo update-alternatives --install /usr/bin/python3 python3 /usr/local/bin/python3.7 1
- sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.9 2
- sudo update-alternatives --config python3
