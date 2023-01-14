## Multibot releases
Многофункциональный Minecraft-bot

### Начало работы
Скачайте нужную версию из releases (Windows/Linux) и загрузите шаблон конфигурации (config.json)
#### 1. Настройка конфигурации
Основные параметры:
- activation_key - ключ активации бота
- telegram_id - ваш telegram ID (куда будет писать телеграм бот), чтобы узнать его напишите боту любое сообщение [Roninore bot](http://t.me/roninore_bot)
- password - пароль, который будут вводить боты при авторизации (да, у всех один)
- mining_rotate - угол поворота при копании генератора (подобрать для себя, рекумендуемые значения: 0 - прямой генератор, 3.85 - 7 блоковый)  
#### [Все настройки конфигурации](config.md)

 #### 2. Запуск приложения
 Запускать приложение необходимо через командную строку(консоль), при этом файл конфигурации должен быть в той же папке, где и исполняемый файл.  
 Структура команды  
 ```
 [исполняемый файл] [сокр. имя бота] [IP] [Никнейм] [Режим работы] [Дополнительно] [Имя файла конфигурации] [Прокси IP] [Прокси PORT] [Прокси Логин] [Прокси Пароль]
 Примеры:
 
 (Все параметры)
 bot_nextgen-win.exe m server.minecraft.net User12345 miner 0 config_2.json 127.0.0.1 4145 proxyuser123 qwertyqwerty
 
 (Только обязательные параметры)
 bot_nextgen-win.exe d server.minecraft.net 12345User empty
 ```
 !!! Порядок параметров важен, но вы можете не указывать ненужные параметры начиная справа  
 Описание параметров:
 - [исполняемый файл] - Исполняемый файл бота !!Для linux(ubuntu) перед использованием напишите `chmod +x [filename]`
 - [сокр. имя бота] - 1-2 лат. буквы для удобного доступа к боту
 - [IP] - Сервер к которому вы хотите подключиться
 - [Никнейм]
 - [Режим работы] - Программа работы бота(`empty` если не нужно выполнять ничего) (На данный момент есть: [`miner`,`crafter`,`fisher`,`seno`,`seller`]
 - [Дополнительно] - По умолчанию 0, лучше не менять
 - [Имя файла конфигурации] - Если нужно запустить разных ботов с разными конфигурациями, можно скопировать config.js и указать новое имя
 - [Прокси IP] - Дальше настройки прокси если есть хороший прокси сервер и нужно запустить много ботов с одного IP
 - [Прокси PORT]
 - [Прокси Логин] 
 - [Прокси Пароль]


### Команды управления
Все боты именуются коротким именем для удобства ввода команд (1-2 лат. буквы). 
Чтобы отправить команду используйте такой шаблон `!<сокр. имя бота>!<команда> <параметры>`
Пример: `!m!chat Всем привет` (m - сокр. имя бота, chat - команда, Всем привет - параметр)  
#### [Актуальный список команд](/commands.md)


