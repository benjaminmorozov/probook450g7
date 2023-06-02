## HP Probook 450 G7 (Intel i5-10210U) and some data I discovered

### ThrottleStop
Honestly just a personal config list that helped me get some use from this useless junk of a laptop. I am no expert in overclocking - there is DEFINITELY a better way to do all of this but I think it's a pretty amazing attempt nevertheless.
This repo contains two files:
 - ThrottleStopSchool.ini - an efficient config that makes games and other processing run a tad bit faster [the HP throttling is really extreme and basically hinders any performance when not using ThrottleStop]
 - ThrottleStop.ini - an absolute behemoth of a config that turns the cpu in to a beast but ⚠️ **WILL DESTROY YOUR BATTERY IN A YEAR** ⚠️ [when plugged into the wall, the laptop still uses the battery to power its turbo overclock]

 I do NOT promise you any performance gains from using any of these configs. DO NOT contact me for help, I don't and will NOT take any responsibilty for your screwups caused by misuse of any of these configs.

### Discoveries
 - the cpu does a thermal shutdown at 101°C, so I set the throttlestop max to 100°C. It is completely capable of running at these temps long-term - proof: my laptop has been running off these configs for 4years and I'm still counting.
 - the gpu is completely useless, I'm not even joking. It's an MX150 and I've never seen a worse chip to this date ever. It's a DirectX 12_1 chip, so just say goodbye to modern games (FIFA 22+). Some overclocking up to +150MHz is possible but the chip is locked otherwise. I've seen it jump to even higher clocks than possible manually, but I have no idea what it means. It's better to just leave the GPU be, it can do cool stuff on its own, but if it's still not enough, try this, it will work: https://www.alza.sk/pcie-riser-1-to-16-card-6-pin-molex-sata-ver-009-priama-d6446231.htm
 - the igpu is pretty fine, just add some ram and dedicate at least 1GB to the igpu in the BIOS and you won't even notice that it's an igpu.
 - the laptop won't ever support anything below Windows Vista, it's due to the AHCI/IDE legacy settings in BIOS that just don't do anything when you switch between them.