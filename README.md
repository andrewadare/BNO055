# BNO055
### Driver library for Bosch Sensortec BNO055 absolute orientation sensor

This is a fork of the ARM mbed library from https://developer.mbed.org/users/StressedDave/code/BNO055/.

Modifications:
* Sensor calibration data is stored in a struct (`cal`) instead of a single register byte (which is available as `cal.raw`).
* `get_calib()` applies masks to the status byte to extract the status of the magnetometer, accelerometer, gyro, and overall system. They are saved as integer fields (ranging 0-3) in the `cal` struct.
* Some formatting and doc changes
