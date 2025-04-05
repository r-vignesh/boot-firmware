# Boot Firmware

This repository contains the firmwares required during booting up a system. Boot stage is described as any and all code or programs that run on a system before High level OS (like Linux, Zephyr) begins. These firmwares are usually loaded by ROM or initial programmable bootloader and are permitted to redistribute under appropriate licenses accompained with each firmware.
Boot firmwares play criticial role in overall security of the system. Compromise bootloader/firmwares can help bypass all OS level hardening or render them fully or partially ineffective. Hence, it is necessary to obtain such firmwares from trusted sources. This repository intends to collect and host boot firmwares from such legitamate sources, so as to serve as centrl sources for various bootloaders and build systems to lookup.

> NOTE: Firmwares hosted in these repository need not be specific to particular bootloader like U-Boot or particular OS like Linux. 

## Some of the example of boot firmwares
- DDR controller or flash controller firmwares
- Platform Security Firmwares
- Device Management firmware (ARM SCP equivalents)
- Custom early stage bootloaders which are vendors release in binary form only.
- Any such firmware critical for boot

## Repository Structure
```
boot-firmware/
├── vendor-name-a/             # Dedicated top-level folder per vendor
    ├── firmware-type-a/       # Collection of a particular type of firmware of various products of vendor
    ├── firmware-type-b/       # Another set of a particular type of firmware of various products of vendor
    |── License.name1          # File containing all the license for firmwares with name1
    |── License.name2          # File containing all the license for firmwares with name2
    |── License.vendor-name-a  # File containing blanket license for remaining firmwares under given vendor directory
    ...
    |── WHENCE               # Per vendor WHENCE file with firmware file to license mapping
├── vendor-name-b/           # Documentation
    ...
├── vendor-name-c/           # Documentation
...

```

## Contributing
Contributions are welcome! Please follow the [contribution guidelines](CONTRIBUTING.md).

## License
See individual vendor folders for license information.

## Frequently Asked Questions

### Can any sort of binaries be hosted?
One of the reasons for a centralized Boot Firmware repository is to make it easier for various bootloaders and build systems to pick up firmware from a common location instead of needing to look at each vendor's website. The general guideline is not to host firmware that is available in source form.
### Is there a Size Limit on the binaries?
No, but remember these are firmware required during boot sequences, so typical size would be within a few MBs.
### Can Encrypted Binaries be hosted?
Yes, encrypted binaries are often part of secure boot flow. They can be hosted as long as obtained from a trusted source, such as the vendor's official website.
### What about firmwares used at OS stage?
They are to be hosted at linux-firmware [repo](https://gitlab.com/kernel-firmware/linux-firmware)