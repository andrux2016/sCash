# SagaCoin

sCash is a PoW + PoS-based cryptocurrency.

sCash uses libsecp256k1,
			  libgmp,
			  Boost1.55,
			  OR Boost1.57,  
			  Openssl1.01m,
			  Berkeley DB 4.8,
			  QT5 to compile


Block Spacing: 30 Seconds
Stake Minimum Age: 24 Hours

Port: 62551
RPC Port: 62551


BUILD LINUX (see the [Wiki](https://github.com/andrux2016/sCash/wiki/Unix-Build) for dependencies)
-----------
1) git clone https://github.com/andrux2016/sCash

2) cd sCash/src

3) mkdir obj/crypto

4) chmod +x leveldb/build_detect_platform

5) cd leveldb && make libleveldb.a libmemenv.a

6) cd ..

7) sudo make -f makefile.unix USE_UPNP=    # Headless SagaCoin

8) strip scashcoind

9) sudo cp scashcoind /usr/local/bin





BUILD WINDOWS
-------------

1) Download Qt.zip from https://github.com/andrux2016/sCash/releases/tag/v1.0 and unpack to C:/

2) Download sCash source from https://github.com/andrux2016/sCash/archive/master.zip 

2.1) Unpack to C:/sCash

3) Install Perl for windows from the homepage http://www.activestate.com/activeperl/downloads

4) Download Python 2.7 https://www.python.org/downloads/windows/

4.1) While installing python make sure to add python.exe to the path.

5) Run msys.bat located in C:\MinGW49-32\msys\1.0

6) cd /C/SagaCoin/src/leveldb

7) Type "TARGET_OS=NATIVE_WINDOWS make libleveldb.a libmemenv.a" and hit enter to build leveldb

8) Exit msys shell

9) Open windows command prompt

10) cd C:/dev

11) Type "49-32-qt5.bat" and hit enter to run

12) cd ../sCash

13) Type "qmake USE_UPNP=0" and hit enter to run

