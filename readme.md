# Анализатор ЭКГ

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

В данном репозитории представлен код для анализа ЭКГ в режиме реального времени для OpenBCI. Подключение к устройству осуществляется через Bluetooth.

## Настройка перед запуском

1) В зависимости от вашей OC вы должны явно указать имя порта, который будет использоваться для Bluetooth коннектора. Название порта будет отличаться в зависимости от конкретной модели вашего ноутбука. Порт задается в начале функции ```main``` в переменной ```port```:

```
# например
# название порта для MacOS
port = "/dev/ttyUSB0"
# название порта для Windows
port = "COM-3"
```

2) Так же важным параметром является board_id. Данная переменная отвечает какое конкретно используется для считывания ЭКГ и каким способом оно подключается. В нашем реализации используется подключение через Bluetooth к плате CYTON DAISY.

```
board_id = BoardIds.CYTON_DAISY_BOARD
```