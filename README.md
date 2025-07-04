# simracing-hwdb
Collection of hwdb entries for various simracing equipment.

### What devices are there?
- Various pedals, which can be mistakenly detected as accelerometers.
- Wheelbases/Handbrakes with one/two axis without a buttons, which is not enough for standard tools to detect a joystick.

# Installation
```
sudo make install
sudo systemd-hwdb update
```

# Removal 
```
sudo make remove
sudo systemd-hwdb update
```

# Contributions
Contributions are welcome! .hwdb entries created as small files like so:
```
# Device description
id-input:modalias:input:*vVIDpPID*
 ID_INPUT_JOYSTICK=1
```
VID and PID should be in uppercase. `ID_INPUT_JOYSTICK=1` is a must for our purposes. `ID_INPUT_ACCELEROMETER=0` is needed only if device has 3 axis (X, Y, Z)
