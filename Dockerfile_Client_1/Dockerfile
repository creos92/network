FROM osrf/ros:indigo-desktop-full

RUN \
 svn checkout https://github.com/creos92/network.git/trunk/Client &&\
 apt-get update &&\
 apt-get install build-essential checkinstall -y &&\
 apt-get install libssl-dev liblzo2-dev libpam0g-dev wget -y &&\
 wget https://swupdate.openvpn.org/community/releases/openvpn-2.4.4.tar.gz &&\
 sudo tar zxvf openvpn-2.4.4.tar.gz &&\
 cd openvpn-2.4.4 && ./configure && make && checkinstall -y
 
CMD cd Client && chmod +rx start_c_1.sh && sync && ./start_c_1.sh
