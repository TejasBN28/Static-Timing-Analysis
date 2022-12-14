# Static-Timing-Analysis
VSD Udemy Course Static Timing Analysis
## Installing OpenTimer
To install the opentimer, 
  - Install CMAKE as explained in the following website https://linuxhint.com/install-cmake-on-ubuntu/.
  - Type the following commands in the terminal
```
cd Desktop
git clone https://github.com/OpenTimer/OpenTimer.git
cd OpenTimer
mkdir build
cd build
cmake ../
make 
```

## Invoking OpenTimer
Opentimer can be invoked by typing the following command 
```
cd Desktop
cd OpenTimer
./bin/ot-shell
```
<p align="center">
  <img src="/images/sta1.png">
</p><br>

The commands available in `OpenTimer can be viewed by typing the command `help` in after invoking OpenTimer.
<p align="center">
  <img src="/images/sta2.png">
</p><br>

## Specifying Constraints in OpenTimer
Consider a random example of timing constaint file (which is usually named as `.timing`) for the design shown in below figure.
<p align="center">
  <img src="/images/sta3.png">
</p><br>

```
clock clk 1000 50
at clk 0 500 0 500
at in 50 50 100 100
slew clk 70 50 70 50
slew in 150 100 150 100
load out 40
rat out 160 160 180 180
```

Here, `clock clk 1000 50` signifies that `clk` is the primary input of the desin and it is a clock input. Here `clock` is a keyword. Always in openTimer, we assume that Clock starts fromlow and then goes high. Here, clk has a period of 1000ps/1ns and a 50% duty cycle.

<p align="center">
  <img src="/images/sta4.png">
</p><br>

Consider `at clk 0 500 0 500`. This signifies the arrival time of the clock. 
<p align="center">
  <img src="/images/sta5.png">
</p><br>



