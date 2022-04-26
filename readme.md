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
* Все основные видео кодеки
* Все пакеты visual c++
* Браузер Google Chrome чистый
* Архиватор 7-zip
* AdwCleaner - простая программа для чистки аналог CCleaner
* Dot Net пакеты все версий для поддержки старых программ

### GamingPrograms.bat
Устанавливает лаунчеры игр и другое
* Steam - самый популярный интернет магазин игр
* EpicGame Launcher - интернет магазин с халявой
* 