# How to start

In Raspi, start I2C modules 

```
insmod /home/i2c-bme280.ko
echo "bme280 0x76" > /sys/bus/i2c/devices/i2c-1/new_device
```

Start webserver

```
python /home/server.py
```

Read from server

```
wget 127.0.0.1:80
cat index.html
```

Start ambient light 

```
python /home/ambient-light.py -c
```

See temperature output on console

```
watch -n 0.2 cat /sys/devices/platform/soc/20804000.i2c/i2c-1/1-0076/temperature
```