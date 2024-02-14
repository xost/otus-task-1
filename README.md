## Система регистрации на мероприятия

### Пользовательские сценарии

+  *Вход в систему ранее зарегистрированного пользователя:*
    + ***неавторизованный клиент*** заходит на сайт, нажимает кнопку "войти" и попадает на страничку ввода логина/пароля
    + клиент вводит свои логин и пароль и нажимает кнопку "войти"
    + если пара логин/пароль верная, то открывается главная страница с активной кнопкой "личный кабинет"
    + если пара логин/пароль неверная, то пользователю выводится информация о ошибке и предлагается повторить попытку либо пройти регистрацию

+ регистрация нового клиента:
    + ***неавторизованный клиент*** заходит на сайт, нажимает кнопку "регистрация" и попадает на страничку регистрации
    + клиент вводит запрашиваемую информацию, придумывает себе логин, пароль и нажимает зарегистрироваться
    + после регистрации клиент попадает на главную страницу как авторизованный клиент и видит лету мероприятий

+ подача заявки на мероприятие
    + ***авторизованный клиент*** заходит на сайт и видит ленту предстоящих мероприятий
    + клиент выбирает интересующее его мероприятие и видит страницу с деталями мероприятия (название мероприятия, описание мероприятия, время проведения, место приведения)
    + клиент нажимает на кнопку "подать заявку на участие" и попадает на страничку "оформления заявки"
    + клиент заполняет требуемые поля (ФИО, дату рождения, телефон, e-mail) и нажимает на кнопку "оплатить участие в мероприятии"
    + клиент переводится на страничку оплаты, вводит требуемые данные и нажимает "оплатить", после успешной оплаты в личном кабинете клиенте, в зарегистрированных мероприятиях появляется запись о участии в данном мероприятие, на указанный e-mail отправляется приглашение на мероприятие и клиент переправляется на страничку, на которой сообщается о том, что он оплатил мероприятие

+ редактирование личной информации в личном кабинете
    + ***авторизованный*** клиент заходит на сайт и нажимает кнопку "личный кабинет"
    + клиент попадает на страничку "личного кабинета" и видит разделы: личная информация, предстоящие мероприятия, прошедшие мероприятия
    + клиент выбирает раздел "личная информация", открывается страничка личной информацией и кнопкой "редактировать"
    + клиент нажимает кнопку "редактировать" и переводится на страничку с возможностью вводить/редактировать личную информацию
    + клиент вводит или редактирует необходимую информацию, нажимает кнопку "сохранить"
    + клиент возвращается на страничку с личной информацией (обновлённой) и кнопкой "редактировать"

### Схема взаимодействия микросервисов

![Схема взаимодействия микросервисов](/interactions.jpg "схема взаимодействия")

### Описание микросервисов

#### Сервис "Мероприятия" (event)

##### Название: "*Мероприятие*"
+ Запросы:
    + детали мероприятия
        + GET /api/v1/event/detail/?event_id=
    + максимальное количество участников
        + GET /api/v1/event/capacity/?event_id=
+ Команды
    + добавить мероприятие
    + изменить мероприятие
+ События:
    +
+ Зависимости:
    +
+ Вопросы:
    +


