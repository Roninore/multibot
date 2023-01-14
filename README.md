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
#####[Все настройки конфигурации](config.md)

 #### 2. Запуск приложения
 Запускать приложение необходимо через командную строку(консоль), при этом файл конфигурации должен быть в той же папке, где и исполняемый файл.  
 Структура команды  
 ```
 [исполняемый файл] [сокр. имя бота] [IP] [Никнейм] [Режим работы] [Дополнительно] [Имя файла конфигурации] [Прокси IP] [Прокси PORT] [Прокси Логин] [Прокси Пароль]
 Пример:
 bot_nextgen-win.exe m server.minecraft.net User12345 miner 0 config_2.json 127.0.0.1 4145 proxyuser123 qwertyqwerty
 ```
 !!Порядок параметров важен, но вы можете не указывать ненужные параметры начиная справа
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
##### [Актуальный список команд](/commands.md)
- start-view/close-view - Включить/отключить viewer - просмотр от лица бота в браузере (порт `3030`)
- start-inv/close-inv - Включить/отключить просмотр инвентаря в браузере (порт `3000`)
- open-block(x,y,z) - Открыть блок смещенный от бота на x,y,z блоков
- close-block - Закрыть блок/любое другое открытое окно
- print-window - Написать в консоль содержимое открытого окна
- print-inv - Написать в консоль содержимое инвентаря
- transfer(type,source,destination,count) - Переложить предмет type из слота source в слот destination в количестве count
- clicker(slot,mode,btn) - Нажать на слот slot кнопкой btn(0,1) в режиме (0,1)
- craft(id, count) - Создать предмет(id) в количестве count
- steal-inv - Выложить все предметы из инвентаря в открытый сундук
- steal-chest - Собрать предметы из открытого сундука
- set-goal(x,y,z) - Дойти до x,y,z !!!!координаты смотреть через `F3 - Target block`, а не координаты персонажа, они смещены по X и Z, возможны ошибки
- chat(message) - Написать в чат сообщение !!! Из-за того что "!" используется для разделения комманд его нельзя использоват в сообщениях, но вы можете использовать "#", которая будет заменена на "!" при отправке сообщения
- quickbar(N) - Установить активный слот (0-8)
- active - Активировать предмет в руке (в основном для меню)
- joinsb - Зайти на скайблок
- rotate(x,y) - Повернуть бота x - влево/вправо, y-вверх/вниз
- control(control,state) - Установить действие бота ('forward', 'back', 'left', 'right', 'jump', 'sprint', 'sneak') в состояние (0,1)
- print-item(slot) - Вывести в консоль информацию о предмете в слоте
- exp - Вывести в консоль уровень бота
- miningstats - Вывести в телеграм информацию о добытых блоках с момента запуска
- restart - Перезагрузка бота
- mine/stop-mine - Начать/Перестать копать
- craft-proc - Запустить процесс крафта
- И др. (позже появятся тут)


