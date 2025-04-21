# NestDAQ-HbdMonitor

## Installation

```
cd NestDAQ-HbdMonitor;

cmake \
-DCMAKE_PREFIX_PATH=<your nestdaq installation path> \
-DCMAKE_INSTALL_PREFIX=<your installation path> \
-B <build dir> -S .;

cd <build dir>;
make install;
```

## How to use

An executable file, HbdMonitor, will be generated.
The process is expected to be connected to TFB through the dqm port.
No mq option exists.
