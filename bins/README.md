
# Example of flashing command


## OTA
```
esptool.py --chip esp8266 --port COM5 --baud 460800 --before default_reset --after soft_reset write_flash -z --flash_mode dio --flash_freq 80m --flash_size 4MB 0xd000 .\build\ota_data_initial.bin 0x0 .\build\bootloader\bootloader.bin 0x10000 .\build\blackmagic.bin 0x8000 .\build\partitions_two_ota.bin
```
## noOTA
```
esptool.py --chip esp8266 --port COM5 --baud 460800 --before default_reset --after soft_reset write_flash -z --flash_mode dio --flash_freq 80m --flash_size 4MB 0x0 .\build\bootloader\bootloader.bin 0x10000 .\build\blackmagic.bin 0x8000 .\build\partitions_singleapp.bin
```

