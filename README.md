#Wifi RC project
A simple board to make RC projects from. Has three simple motor controllers, 6 prewired LED connections, SPI and Serial outputs & more.

Can run off USB (no motor) or 7.4 or 11.1V batteries (depending on what your motors need). Set your power source using the VS jumper. The 5V outputs are intended to dirve Servo's, but the wiring isn't exactly ideal. A new version may set aside 3 pins for dedicated Servo outputs.

The module has been produced and tested, but not yet mounted in a model. See pictures of the reflowed and soldered board [here](http://jcprojects.tumblr.com/post/149121660034/my-second-dev-board-based-on-the-particleio-p1) and a short video from testing [here](http://jcprojects.tumblr.com/post/154342641139/so-much-blink-all-pins-mapped-out-and-tested-i).

![Alt text](/Pinout_Dumper001.png?raw=true "Pinout")

##BOM
The [bill of materials](/Dumper001/Dumper001.csv) can be found as a .csv file in this repository. The core part is the P1 module (USI WM-N-BM-14) that you can pick up in a [10-pack from the Particle store](https://store.particle.io/products/p1), pre-flashed with the Particle firmware ([P1 datasheet/docs](https://docs.particle.io/datasheets/p1-datasheet/)).

I have used AMS1117 for both 3.3 and 5V regulation and that seems to work well without any signs of overheating. The L9110 motor drivers are weak, but will do the trick for small motors.

##Errata* The pin marked D6 is UART2_CTS,(pin 30) accessable as WKP.* The pin marked as SS is DAC (pin 24). A2 is the actual SS pin for SPI1.
Both of these pins work for digital IO, but use the constant WKP to access the D6 pin and DAC to access the pin marked SS.

##License
[CERN OHL V1.2](http://www.ohwr.org/licenses/cern-ohl/v1.2)

![image](/Dumper3D_001.png)