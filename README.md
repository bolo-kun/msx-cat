PCB works for games up to 64kb (it's bits, so in bytes it's 8kB). Carts above 64kb aren't natively supported by MSX and need a mapper.

Fixed wrong hole placement, reduced PCB size to make is cheaper to produce.

Chips the original project used are hard to get and pricey but W29EE011 and AM29F010B work flawless for me, other 29F010 chips should work as well (first two letters stand for chip maker)

If you want to put it into a cartridge shell, you need to solder the EEPROM directly to the PCB as it won't fit into the case with a DIP socket.

For chips I mentioned you need to pad the rom file as shown below on linux bash or on windows using GIT-Bash:

```bash
# 16kb:
cat rom16k.bin rom16k.bin rom16k.bin rom16k.bin rom16k.bin rom16k.bin rom16k.bin rom16k.bin > game128.bin

# 32kb: 
cat rom32k.bin rom32k.bin rom32k.bin rom32k.bin > game128.bin

# 64kb:
cat rom64k.bin rom64k.bin > game128.bin
```

<img width="1099" height="826" alt="image" src="https://github.com/user-attachments/assets/cbeb0609-2034-4902-893f-8153153c7e76" />

<img width="1081" height="815" alt="image" src="https://github.com/user-attachments/assets/335a831f-8319-4cee-a952-4c3bb1128801" />
