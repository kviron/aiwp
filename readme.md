# Автоматизированная установка программ для windows 10

Первое что нужно сделать, для того что бы можно было воспользоваться автоматической установкой это:

* Откройте командную строку (power shell) от имени администратора
* Выполните две команды по очередно

`Set-ExecutionPolicy AllSigned ` или `Set-ExecutionPolicy Bypass -Scope Process`

Подвердите выполнение команды вписав `Y` а после одной из выполненых команд выполните следующую команду
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Все вы готовы к автоматической установке программ. Для того что бы запустить установку программ. Кликните правой кнопокй мыши на файлы установки и запустите их  `от имени администратора` это <b>важно</b>!

## Описание файлов
Описание всех файлов и устанавливающих программ

### Common.bat
Устанавливает все самые важные пакеты для windows такие как:
* [Klite Codec Pack - Все основные видео кодеки](https://codecguide.com/)
* [Microsoft Visual C++ Все версии](https://docs.microsoft.com/ru-ru/cpp/windows/latest-supported-vc-redist?view=msvc-170)
* [Google Chrome чистый](https://www.google.com/intl/ru_ru/chrome/)
* [Архиватор 7-zip](https://www.7-zip.org/)
* [AdwCleaner](https://ru.malwarebytes.com/adwcleaner/)
* [Dot Net пакеты всеx версий](https://dotnet.microsoft.com/en-us/)

### GamingPrograms.bat
Устанавливает лаунчеры игр и другое
* Discord
* Steam
* EpicGame Launcher 
* PicoTorrent - легковестный бесплатный торрент клиент

### NvidiaDrivers.bat
* Актуальный игровой видеодрайвер
* [Geforce Expirience](https://www.nvidia.com/ru-ru/geforce/geforce-experience/)