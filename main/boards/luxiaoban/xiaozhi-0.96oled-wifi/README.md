# luxiaoban-xiaozhi-0.96oled-wifi

ESP32-S3 鹿小班小智板，网络：Wi-Fi。

## 硬件

- 显示：SSD1306 128x32（默认），可选 SSD1306/SH1106 128x64；I2C SDA41/SCL42
- 音频：PDM 麦克风 CLK GPIO2 / DIN GPIO3；扬声器 BCLK15 / LRCK16 / DOUT7；输入输出均 16 kHz
- 按键：BOOT GPIO0；音量键见 config.h
- 电源：充电 GPIO38、电池 ADC2 channel 6、电源锁存 GPIO21

## 构建

```sh
python scripts/build.py luxiaoban/xiaozhi-0.96oled-wifi --name luxiaoban-xiaozhi-0.96oled-wifi
```

OLED 的 128x64 变体可用 config.json 中对应唯一 build name。TFT 显示风格使用项目全局 `DISPLAY_STYLE`，不新增 wechatui 身份变体。

## 实机验证

需验证上电锁存、充放电检测与电量、休眠/关机、显示方向和背光、PDM 录音、16 kHz 播放、按键、配网/重连；ML307 型号还需验证网络切换、UART 通信与两种网络传输。

