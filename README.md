# jtag-remote-server

This tool can help you debug chips remotely. It requires libftdi to communicate with FTDI chips and exposes various protocol for remote debugging.

An example scenario where this tool might be useful:

```
┌────────┐ JTAG ┌────────┐ USB ┌──────────┐ TCP ┌──────────┐
│  FPGA  ├──────┤  FTDI  ├─────┤  HOST 1  ├─────┤  HOST 2  │
└────────┘      └────────┘     └──────────┘     └──────────┘
```

You can run this tool on `HOST 1` and debug the chip on `HOST 2` remotely.

Supported protocols:

- Xilinx virtual cable: for Vivado
- Remote bitbang: for OpenOCD
- JTAG vpi: for OpenOCD

Some example OpenOCD configs are provided under `examples` directory.