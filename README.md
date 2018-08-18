# log-sensor-express
Logs sensor data (DHT11) in Firebase database and visualize in browser (via Firebase Hosting).  
Main reference (e-Book): Full Stack Web Development with Raspberry Pi 3 (Packt).  
My site: https://cv.antonello.com.br  

This implementation don´t need Express or Sqlite3 because all data are directly saved in Firebase (run: node firebase-process to being saving data) and the view can be done by browser in Firebase Hosting. No history data area saved.

## Reading DHT11 sensor
git clone git://git.drogon.net/wiringPi  
cd wiringPi/  
./build  
gpio -v
wget http://www.airspayce.com/mikem/bcm2835/bcm2835-1.52.tar.gz  
tar -xvzf bcm2835-1.52.tar.gz  
cd bcm2835-1.52  
./configure  
make  
sudo make check  
sudo make install
npm install --save node-dht-sensor

## Instaling Chart.js
npm install chart.js --save

## Instaling Firebase
npm install -g firebase-tools  
firebase --version  
firebase login  
firebase init  
firebase serve # to serve and test locally (localhost:5000)
firebase deploy # to deply app in the firebase hosting  

## Running the recorder 
On firebase folder run 'node firebase-process' (where firebase-process is a subfolder in firebase folder)  
This will recorder data in firebase every 4 seconds, but no history are implemented.
