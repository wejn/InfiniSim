# What's this
Modded sim for the [White Rose InfiniTime mod](https://github.com/wejn/InfiniTime).

# Building

Configure:

``` sh
test -d ../InfiniTime/
npm install lv_font_conv
git submodule update --init --recursive
cmake -S . -B build -DInfiniTime_DIR=../InfiniTime/ -DENABLE_USERAPPS="Apps::Alarm,Apps::Timer,Apps::Steps,Apps::HeartRate,Apps::WhiteRoseTimer"
```

Rebuild:

``` sh
cmake --build build -j4
```

# Running

``` sh
./build/infinisim
```
