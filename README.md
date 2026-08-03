# InfiniSim (WRT edition)

This fork adds support for the [White Rose Timer](https://wejn.org/2026/08/white-rose-timer-on-pinetime/)
mod ([available here](https://github.com/wejn/InfiniTime)) to InfiniSim.

Original [README](https://github.com/InfiniTimeOrg/InfiniSim/blob/main/README.md).

I do not intend to upstream this.

## Building

Configure:

``` sh
test -d ../InfiniTime/ # should be https://github.com/wejn/InfiniTime
npm install lv_font_conv
git submodule update --init --recursive
cmake -S . -B build -DInfiniTime_DIR=../InfiniTime/ \
  -DENABLE_USERAPPS="Apps::Alarm,Apps::Timer,Apps::Steps,Apps::HeartRate,Apps::WhiteRoseTimer" \
  -DENABLE_WATCHFACES="WatchFace::Digital,WatchFace::Terminal,WatchFace::WhiteRose"
```

Rebuild:

``` sh
cmake --build build -j4
```

## Running

``` sh
./build/infinisim
```
