# Awesome CH32

An unofficial curated list of WCH's 32-bit MCU related code and resources.

## Official Resources

> **Note**
> Chinese(中文) content are always newer than English version.

- Official Website (Chinese) [南京沁恒微电子股份有限公司](http://www.wch.cn/)
  - **BBS**: [沁恒微电子社区](https://www.wch.cn/bbs) - Official Tech Support Forum, English is also acceptable.
- Official Website (English) [Nanjing Qinheng Microelectronics](http://www.wch-ic.com/)
- **Download Center**, DataSheet, EVT(SDK+Demo Code), Tools, etc.
  - Chinese: [下载资料](https://www.wch.cn/downloads/category/27.html)
  - English: [Downloads](https://www.wch-ic.com/downloads/category/27.html)
  - DS for "DataSheet 数据手册", RM for "Reference Manual 应用手册", EVT for "SDK+Demo Code 开发工具"
  - IC Package and Footprint: [SCHPCB.ZIP](https://www.wch.cn/downloads/SCHPCB_ZIP.html) [PACKAGE.PDF](https://www.wch.cn/downloads/PACKAGE_PDF.html)
- **Github Organization**: [openwch](https://github.com/openwch) - organized by MCU series. Documents, code, demo are included.
  - Arduion Support: [openwch/arduino_core_ch32](https://github.com/openwch/arduino_core_ch32)
  - OpenOCD (Binary): [openwch/openocd_wch](https://github.com/openwch/openocd_wch)
- MCU List: [MCU+](https://www.wch-ic.com/products/categories/47.html?pid=5)
- MCU Selection: [MCU](https://special.wch.cn/zh_cn/mcu/#/)(CN) [MCU](https://special.wch.cn/en/mcu/#/)(EN)
- MounRiver Studio(IDE): <http://www.mounriver.com/>
- Debugger Probe: [WCH-Link](https://www.wch-ic.com/products/WCH-Link.html) [WCH-Link仿真调试器模块](https://www.wch.cn/products/WCH-Link.html)
  - [WCH-LinkUtility.ZIP](https://www.wch.cn/downloads/WCH-LinkUtility_ZIP.html)
- USB ISP Programmer: [WCHISPTool_Setup.exe](https://www.wch.cn/downloads/WCHISPTool_Setup_exe.html)
  - [WCHISPTool_CMD.ZIP](https://www.wch.cn/downloads/WCHISPTool_CMD_ZIP.html) for command line under Linux, macOS and Windows.

## MCU Families

For 32-bit MCU, WCH has two categories: Cortex-M and RISC-V.
Cortex-M product line has not been updated for a long time. (There is a 32-bit unknown instruction set used by CH563/CH561/CH568/CH567).

[Official Intro(Chinese)](https://www.wch.cn/products/productsCenter)

### RISC-V

> **Note**
> WCH's RISC-V has some key differences from the mainstream RISC-V ISA:
>
> - No `mtime` and `mcycle` CSR. No `MachineTimer` interrupt. Use `SYSTICK` core peripheral instead.
> - No `MachineExternal` interrupt. The external interrupts are handled the same as core interrupts as `mcause` code.
> - Core interrupts are different, refer "QingKeV*_Processor_Manual.PDF" for details.

Refer: [ch32-data]

- CH32V General RISC-V
  - [CH32V103] RISC-V4A
  - [CH32V203] RISC-V4B
  - [CH32V208] RISC-V4C, BLE 5.3
  - [CH32V303] RISC-V4F, CAN
  - [CH32V307]/CH32V305 RISC-V4F, USBHS, CAN, DVP, 1000M ETH
  - [CH32V317] RISC-V4F, USBHS,1000M ETH, DVP
  - CH32V0 Low Price
    - [CH32V003] RISC-V2A
    - [CH32V002] RISC-V2C (unreleased) - V003 compatible with bigger SRAM, 12-bit ADC
    - [CH32V004] RISC-V2C (unreleased) - V003 compatible with bigger SRAM, 12-bit ADC
    - [CH32V006]/CH32V005 RISC-V2C (unreleased)
    - ~~[CH32V007]/CH32M007 RISC-V2C (unreleased) - M for Motor Control~~ DS revoked?
- CH32X0 Special IO
  - [CH32X035]/CH32X033 RISC-V4C, USB PD(CH32X035), PIOC
- CH32L Low Power
  - [CH32L103] RISC-V4C, USB PD, Low Power
- BLE MCU
  - [CH573]/CH571 RISC-V3A, BLE 4.2
  - [CH583]/CH582/CH581 RISC-V4A, BLE 5.3
  - [CH585]/CH584 RISC-V3C, BLE 5.4, USBHS(CH585), NFC
  - [CH592]/CH591 RISC-V4C, BLE 5.4
  - [CH32V208] (also appears in CH32V series)
- Special Interface
  - [CH569]/CH565 RISC-V3A, USBSS, SerDes, HSPI, BUS8, 1000M ETH
  - [CH641] RISC-V2A, USB PD, Wireless Charging
  - [CH643] RISC-V4C, RGB LED Driver, USB PD, PIOC
  - [CH645] RISC-V4C (unreleased), USBHS, USB Hub, USB PD, 100M ETH
  - [CH564] RISC-V4J, USBHS, USB PD, 100M ETH, XBUS, SLV

In the list above CH57x, CH58x, CH59x and CH56x are legacy peripheral ones, which means they have an old style of peripherals.

### Cortex-M

- Cortex-M3
  - CH32F1: [CH32F103]
  - CH32F2:
    - [CH32F203]/[CH32F203C8]
    - [CH32F207]/CH32F205
    - [CH32F208] - BLE
- Cortex-M0 - BLE MCU
  - [CH578/7]
  - [CH579]

[ch32-data]: https://github.com/ch32-rs/ch32-data
[CH32F103]: https://www.wch.cn/products/CH32F103.html
[CH32F203C8]: https://www.wch.cn/products/CH32F203C8.html
[CH32F203]: https://www.wch.cn/products/CH32F203.html
[CH32F207]: https://www.wch.cn/products/CH32F207.html
[CH32F208]: https://www.wch.cn/products/CH32F208.html
[CH32V002]: https://www.wch-ic.com/downloads/CH32V002DS0_PDF.html
[CH32V003]: https://www.wch.cn/products/CH32V003.html
[CH32V004]: https://www.wch-ic.com/downloads/CH32V004DS0_PDF.html
[CH32V006]: https://www.wch.cn/downloads/CH32V006DS0_PDF.html
[CH32V007]: https://www.wch.cn/downloads/CH32V00XRM_PDF.html
[CH32V103]: https://www.wch.cn/products/CH32V103.html
[CH32V203]: https://www.wch.cn/products/CH32V203.html
[CH32V208]: https://www.wch.cn/products/CH32V208.html
[CH32V303]: https://www.wch.cn/products/CH32V303.html
[CH32V307]: https://www.wch.cn/products/CH32V307.html
[CH32V317]: https://www.wch.cn/products/CH32V317.html
[CH32X035]: https://www.wch.cn/products/CH32X035.html
[CH32L103]: https://www.wch.cn/products/CH32L103.html
[CH573]: https://www.wch.cn/products/CH573.html
[CH578/7]: https://www.wch.cn/products/CH578_7.html
[CH579]: https://www.wch.cn/products/CH579.html
[CH583]: https://www.wch.cn/products/CH583.html
[CH585]: https://www.wch.cn/products/CH585.html
[CH592]: https://www.wch.cn/products/CH592.html
[CH641]: https://www.wch.cn/products/CH641.html
[CH643]: https://www.wch.cn/products/CH643.html
[CH645]: https://www.wch.cn/products/CH645.html
[CH564]: https://www.wch.cn/downloads/CH564DS0_PDF.html
[CH569]: https://www.wch.cn/products/CH569.html
