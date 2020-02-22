```
# 进入目录
cd /tmp
# 开启串口（非常重要！万一刷坏了这可是救命的）
nvram set flag_last_success=1
nvram set boot_wait=on
nvram set uart_en=1
nvram commit
# 正式刷写
mtd write kernel1.bin kernel1
mtd write rootfs0.bin rootfs0
# 重启
reboot
```