# testptp

## Build
```bash
gcc testptp.c -o testptp
```

## Usage

Here we use Intel I210 for example.

Set SDP0 channel 0 as PPS output with 1Hz
```bash
sudo ./testptp -d /dev/ptp0 -L0,2 -i 0
sudo ./testptp -d /dev/ptp0 -p 1000000000
```

Set SDP1 channel 1 as PPS input
```bash
sudo ./testptp -d /dev/ptp0 -L1,1 -i 1
```

Listen PPS input event for channel 1
```bash
sudo ./testptp -d /dev/ptp0 -e 100 -i 1
```
