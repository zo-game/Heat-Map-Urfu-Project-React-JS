Проект от URFU, в котором предстояло создать функциональное добавление меток на карту Свердловсвой области, с учетом проведенных в школах опросах о качестве образования. Большая часть функциональности при пуле будет недоступна, из-за привязки к бэкэнду.

Техническое задание
 Проект “Создание тепловой карты региона РФ для визуализации данных об уровне удовлетворенности граждан”

Описание функциональности
Карта

Карта по Свердловской области. При приближении метки будут разделяться(дробиться) по способу: муниципалитеты Свердловской области -> города -> районы в городе -> отдельные учебные заведения. Все это в виде тепловой карты.
Система должна считать средний балл по 10 бальной шкале для каждого объекта и на основании него окрашивать школу и округ:

от 1 до 2 – ярко красный;

от 3 до 4 – бледно красный;

от 5 до 6 – желтый;

от 7 до 8 – бледно зеленый;

от 9 до 10 – ярко зеленый.

необходимо выводить серую подсветку для округов и школ, по которым нет данных или данных меньше минимального количества, которую дать возможность менять через систему администрирования.

		
Роли пользователей

Участники опросов
Авторизация по почте или через гугл аккаунт
Доступна страница с опросами

Роли участников опросов(ученик, сотрудник школы, родитель) будет выбираться при регистрации.
Личный кабинет


Стейкхолдеры
У админа будет возможность добавлять стейкхолдеров через админку он может добавить почту стейкхолдера, дальше этому стейкхолдеру нужно будет зарегистрироваться через эту почту и у него сразу будет роль стейкхолдера. 

Функционал стейкхолдера: добавление опросов, добавление данных по проведенному опросу, просмотр карты, добавление пользователей и стейкхолдеров, просмотр личного кабинета 


Описание страниц

Страницы участника опроса:
Регистрация/авторизация: поле ввода почты и пароля или вход через гугл аккаунт , чекбокс выбора роли пользователя(так как родитель ученика школы может преподавать в этой же школе) , до авторизации и регистрации пользователь видит пустой хедер сайта с логотипом.
После регистрации пользователю становится доступны два раздела в хедере сайта : страница опросов - “опросы” и страница личного кабинета. 
Страница опроса: вопросы идут по порядку, на каждый вопрос ползунок с вариантами от 1 до 10  (уровень удовлетворенности 1 - ужасно, 10 - отлично)
Перед каждым опросом необходимо выбрать соответствующую область, город и школу из предложенных. В зависимости от роли пользователя ему будут предлагаться разные вопросы.
Страница с опросами: плитка разных по темам опросов , например опрос о бытовом состоянии школы , удовлетворенности преподаваемых дисциплин и тд. пользователю не будут доступны темы опросов, в которых он некомпетентен ( школьнику не будет доступен опрос о степени удовлетворенности оплаты труда и тд), один опрос для одной роли.
Личный кабинет: информация о пользователе - возраст,роль

        


Страницы стейкхолдера:
Новому стейкхолдеру на почту приходит письмо с ссылкой ,при переходе по ней его перебрасывает на страницу регистрации с двумя полями: логин (почта , на которую пришло письмо с приглашением) заполнен автоматически и паролем, который придумывает новый стейкхолдер.
Хедер: для стейкхолдера будет доступно больше разделов в хедере , чем для обычного пользователя. Будут доступны следующие разделы: “Карта” , “ Опросы”, “Стейкхолдеры”, “Учебные заведения”,”Результаты опроса” и личный кабинет.
Карта: слева до 1\3 экрана находятся фильтры: оценка по роли ( среднее арифметическое за все опросы по одной роли) , общая оценка (среднее арифметической за опросы по всем ролям) , а остальные 2\3 занимает интерактивная карта Свердловской области. В максимальном отдалении карта будет закрашиваться по районам соответствующими цветами к средней оценке по всем школам, при приближении будут появляться отдельные маркеры со средней оценкой школ города , также будет показан соответствующий цвет в маркере, при повторном приближении города будут выделены районы этого города и маркерами отмечена каждая отдельная школа. Приближение на данный момент будет реализовано по кнопками.
Опросы: будет показана плитка всех созданных опросов конкретного стейкхолдера и кнопка добавления нового опроса , при открытии карточки опроса можно будет посмотреть все вопросы в этом опросе и поделиться им по Qr-коду.
После нажатия на кнопку “создать опрос” открывается страница с полем, в которое стейкхолдер вводит тему опроса, checkbox с ролью для которой будет проходить опрос, добавление вопроса через кнопку (добавляется поле ввода вопроса, можно добавлять хоть сколько вопросов). В конце кнопка создать опрос, после этого создание опроса завершается и он становится доступным для опрашиваемых.
Стейкхолдеры: список добавленных стейкхолдеров , состоящий из ФИО , кнопки “редактировать” и “удалить”. При нажатии на кнопку “редактировать” можно отобрать или добавить право “добавление новых стейкхолдеров” у конкретного стейкхолдера, а “удалить” полностью убирает у данного пользователя все возможности стейкхолдера. Вверху справа будет находиться кнопка “Добавить стейкхолдера” , при нажатии на нее появится модальное окно в центре экрана с затемнением , в нем  поле ввода почты для приглашения пользователя ,пункт с выбором права “разрешить приглашение других стейкхолдеров”, кнопкой “готово” и “отменить”.
Учебные заведения:  возможность добавления нового учебного заведения с его адресом - поля: область, город, номер школы.
Результаты опросов: таблица с двумя столбцами, в первом будет логин, во втором результаты опроса ( среднее арифметическое ).
Фильтры справа занимают ⅓ экрана, фильтры: по области/городу/школе, по роли.
Возможность добавления данных вручную: кнопка “добавить данные”  при нажатии  открывается страница с выбором области, города, школы, роли опрашиваемых, темы опроса и поле с вводом средней оценки каждого пользователя.
Личный кабинет: Поля с вводом ФИО, почта, к которой привязан личный кабинет, возможность смены пароля.
