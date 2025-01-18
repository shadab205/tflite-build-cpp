# TensorFlow Lite C++ for Raspberry Pi and x86 Platforms

Precompiled **TensorFlow Lite 2.18.0** binaries for **Raspberry Pi 3, 4 (64-bit)** and **x86 (64-bit)** systems.

## Supported Features

- NEON optimization (Raspberry Pi)
- XNNPACK delegate (Raspberry Pi, x86)

### Supported Platforms

#### Raspberry Pi
- **Boards:**
  - Raspberry Pi 3 Model A+
  - Raspberry Pi 3 Model B+
  - Raspberry Pi 4 Model B
  - Raspberry Pi 5 (Not tested)
- **OS:**
  - Raspberry Pi OS Bookworm 64-bit
- **Tested On:**
  - Raspberry Pi 3 Model B+
  - Raspberry Pi 4 Model B (8 GB)

#### x86
- **Note:**
  - No support for `avxnnint8`. This flag is disabled as it causes build failure of the library.
- **Tested On:**
  - x86 64-bit machine running Ubuntu 22.04.

## Installation

Download and install the appropriate `.deb` package for your platform:

### Raspberry Pi (64-bit)
```bash
wget https://github.com/tflite-build/releases/latest/download/tensorflowlite-elinux_aarch64.deb
sudo apt install -y ./tensorflowlite-elinux_aarch64.deb
```

### x86 (64-bit)
```bash
wget https://github.com/tflite-build/releases/latest/download/tensorflowlite-amd64.deb
sudo apt install -y ./tensorflowlite-amd64.deb
```

### Uninstallation

To uninstall TensorFlow Lite, run:
```bash
sudo apt purge --autoremove -y tensorflowlite
```

### Debian Package Contents

The debian package contains the following:

| Library                     | Description                                                              |
|:----------------------------|:-------------------------------------------------------------------------|
| libtensorflowlite.so        | C++ API to access TensorFlow Lite interpreter and perform an inference   |
| Header Files                | Includes headers for TensorFlow Lite, enabling development with C++ APIs |

### Reference
1. [TensorFlow Lite repository](https://github.com/tensorflow/tensorflow/tree/master/tensorflow/lite)
2. [Bazel](https://bazel.build/docs)