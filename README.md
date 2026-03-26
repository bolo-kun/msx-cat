PCB works for games up to 64kb (it's bits, so in bytes it's 8kB). Carts above 64kb aren't natively supported by MSX and need a mapper.

Fixed wrong hole placement, reduced PCB size to make is cheaper to produce compared to the source project. 
Chips the original project used are hard to get nowadays but AM29F010B works flawless for me, other 29F010B should work as well (first two letters stand for AMD so models with different first 2 letters are clones from different factories), W29EE011 should work as well but I haven't tried it yet.

For chips I mentioned you need to pad the rom file as shown below on linux bash or on windows using for example GIT Bash:

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
