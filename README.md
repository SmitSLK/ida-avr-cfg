# ida-avr-cfg
IDA Pro ATmega168/P/PB ATmega328/P/PB configs

# 1. Converting Hex code to dump:
```bash
#avr-objdump -s -m atmega8 -D flash.hex > flash.dump
avr-objdump -s -m avr -D flash.hex > flash.dump
```
# 2. Converting Hex code to elf
```bash
avr-objcopy -I ihex flash.hex -O elf32-avr flash.elf
```
# 3. Converting Hex code to bin
```bash
avr-objcopy -I ihex flash.hex -O binary flash.bin
```
# 4. Converting Hex/bin code to assembler
```bash
avr-objdump -l -t -D -S flash.bin > flash.bin.dis
avr-objdump -m avr -D flash.hex > flash.hex.dis
```
