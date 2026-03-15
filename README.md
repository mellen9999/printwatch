# printwatch

real-time terminal monitor for Bambu Lab 3D printers. connects via LAN mode MQTT — no cloud required.

![printwatch](https://img.shields.io/badge/python-3.10+-blue)

## what it does

- live progress bar, layer count, ETA
- nozzle/bed temperature gauges
- fan speeds, wifi signal
- alerts on failure, filament issues, clogs
- stuck detection (warns if same layer for 10+ minutes)
- terminal bell + desktop notification on print done/failed
- works over LAN only — no Bambu Cloud needed

## setup

```
pip install -r requirements.txt
```

your printer needs **LAN Mode** enabled (Settings → Network on the touchscreen). grab the **access code** and **serial number** from the printer screen.

## usage

```
printwatch --ip 192.168.1.100 --code 12345678 --id 01P00A000000000
```

or with env vars:

```
export BAMBU_IP=192.168.1.100
export BAMBU_ACCESS_CODE=12345678
export BAMBU_DEVICE_ID=01P00A000000000
printwatch
```

## compatible printers

tested on A1 Mini. should work with any Bambu Lab printer that supports LAN mode MQTT (X1C, X1, P1P, P1S, A1).

## license

MIT
