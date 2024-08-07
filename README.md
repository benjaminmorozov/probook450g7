## HP Probook 450 G7 (Intel i5-10210U, MX150)
A dump of files and information regarding HP Probook 450 G7 in the i5-10210U/MX150/noFingerprintReader configuration.
### ThrottleStop
A personal config list that helped me get some use from this laptop. I am no expert in overclocking - there is DEFINITELY a better way to do all of this but I think it's a pretty amazing attempt nevertheless.
This repo contains two files:
 - ThrottleStopSchool.ini - an efficient config that makes games and other processing run a tad bit faster [the HP throttling is really extreme and basically hinders any performance when not using ThrottleStop]
 - ThrottleStop.ini - an absolute behemoth of a config that turns the cpu in to a beast but ⚠️ **WILL DESTROY YOUR BATTERY IN A YEAR** ⚠️ [when plugged into the wall, the laptop still uses the battery to power its turbo overclock]

 I do NOT promise you any performance gains from using any of these configs. DO NOT contact me for help, I don't and will NOT take any responsibilty for your screwups caused by misuse of any of these configs.

### Repasting
Repasting has proven to be really helpful at minimizing throttling issues over the years. I can confirm ARCTIC MX-4 is fully compatible with this laptop.

### Linux compatibility
Fully compatible, including fn keys, sidecar (both wifi and bluetooth), camera+microphone and dgpu.
Tested on: Ubuntu Server 24.04 LTS, Ubuntu 23.04

### Hackintosh compatibility
Incompatible dgpu, webcam, SD reader, microphone and sidecar.
Tested on: macOS Sonoma

### Discoveries
 - the cpu does a thermal shutdown at 103°C, so I set the throttlestop max to 100°C. It is completely capable of running at these temps long-term - proof: my laptop has been running off these configs for 4years and I'm still counting.
 - the gpu is an MX150. It's a DirectX 12_1 chip, so it doesn't have full DX12 support (ex. FIFA 22+). Some overclocking up to +150MHz is possible but the chip is locked otherwise. I've seen it jump to higher clocks than possible manually though. It's better to just leave the GPU be. I did research plugging an external GPU into the internal m2 slot but it is apparently unsupported. (https://www.alza.sk/pcie-riser-1-to-16-card-6-pin-molex-sata-ver-009-priama-d6446231.htm)
 - the igpu is pretty fine, just add some ram and dedicate at least 1GB VRAM to it in the BIOS.
 - the laptop won't ever support anything below Windows Vista, it's due to the AHCI/IDE legacy settings in BIOS that just don't do anything when you switch between them.