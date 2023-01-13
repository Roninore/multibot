## Multibot releases
Многофункциональный Minecraft-bot

### Начало работы
Скачайте нужную версию из releases (Windows/Linux) и загрузите шаблон конфигурации (config.json)
Конфигурацию необходимо настроить.
Основные параметры:
- activation_key - ключ активации бота
- telegram_id - ваш telegram ID (куда будет писать телеграм бот), чтобы узнать его напишите боту любое сообщение [Roninore bot](http://t.me/roninore_bot)
- max_reconnections - сколько раз ботам стоит переподключаться за один запуск приложения (в случае перезагрузки сервера, кика или ошибки в программе)
- delay_tick - задержка действий бота (регулирует скорость некоторых действий, лучше не менять)
- password - пароль, который будут вводить боты при авторизации (да, у всех один)
- showChat - отображать ли чат в консоли
- mining_rotate - угол поворота при копании генератора (подобрать для себя, рекумендуемые значения: 0 - прямой генератор, 3.85 - 7 блоковый)
- allowed_blocks - массив разрешенных для добычи блоков


### Команды управления
Все боты именуются коротким именем для удобства ввода команд (1-2 лат. буквы). 
Чтобы отправить команду используйте такой шаблон !<сокр. имя бота>!<команда> <параметры>
Пример: !m!chat Всем привет (m - сокр. имя бота, chat - команда, Всем привет - параметр)
- start-view/close-view - Включить/отключить viewer - просмотр от лица бота в браузере (порт 3030)
- start-inv/close-inv - Включить/отключить просмотр инвенторя в браузере (порт 3000)
- open-block-cursor - Открыть блок на который смотрит бот
- open-block - Открыть блок который находится на -1 координату по Z
- close-block - Закрыть блок/любое другое открытое окно
- print-window - Написать в консоль содержимое открытого окна
- print-inv - Написать в консоль содержимое инвентаря
- transfer(type,source,destination,count) - Переложить предмет type из слота source в слот destination в количестве count
- clicker(slot,mode,btn) - Нажать на слот slot кнопкой btn(0,1) в режиме (0,1)
- craft(id, count) - Создать предмет(id) в количестве count
- steal-inv - Выложить все предметы из инвенторя в открытый сундук
- steal-chest - Собрать предметы из открытого сундука
- set-goal(x,y,z) - Дойти до x,y,z !!!!координаты смотреть через F3 - Target block, а не координаты персонажа, они смещены по X и Z, возможны ошибки
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


