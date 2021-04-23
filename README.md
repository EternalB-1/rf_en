<h2># WORKING WITH 433MHz TRANSMITTERS WITH RASPBERRY PI</h2>

Modern barriers, electronic gates, and some electronic locks operate on these frequencies. By reading the values from the receiver when there is a signal from the remote control to open something, you can repeat this signal, thereby opening/closing the target.

<h2>The following types of modules are used for receiving and transmitting:</h2>

![alt text](https://static-sl.insales.ru/images/products/1/1171/141264019/1070.jpg)
![alt text](https://ae01.alicdn.com/kf/HTB1day5aULrK1Rjy1zbq6AenFXa6/QIACHIP-433-Mhz.jpg)

<h2>I connected them according to the scheme:</h2>

![alt text](https://github.com/EternalB-1/rf/blob/master/img/Screenshot_1.png?raw=true)

<h3>After that, you need to install the library and repository:</h3>

git clone https://github.com/EternalB-1/rf_ru

pip3 install rpi-rf

<h3>If you have any problems installing the rpi-rf library, there is a folder with it in the repository. To install it manually, enter:</h3>

cd rf/rpi-rf-0.9.6

sudo python3 setup.py install

<h2>To receive a signal, enter:</h2>

cd rf

python3 recieve.py -g 20

<h2>To send a signal (if you receive a signal at this time, create a new session):</h2>

cd rf

python3 send.py -g 21 -t * -p ** ***

*- protocol

**-pulse

***- device code



All information is taken from the video: https://youtu.be/HCiEaf1HPhE
