## Схема Базы Данных
![Диаграмма](Diagrams/BD.png) 

**Описание таблицы Client**

+ Название таблицы:	Client
+ Краткое описание:	В таблице хранятся данные о клиентах
+ Первичные ключи:	id
+ Таблицы, связанные соединением:
    *   «один-ко-многим»:	Request;
    *   «многие-ко-многим»:	-
    *   «один-к-одному»:	-
+ Значение полей: 
    *   Id:	Ключевое поле
    *   FIO:	ФИО клиента
    *   Phone:	Телефон клиент
    *   Email:	Электронная почта клиента 

**Описание таблицы Request**

+ Название таблицы:	Request 
+ Краткое описание:	В таблице хранятся данные о заказах
+ Первичные ключи:	Id
+ Таблицы, связанные соединением:
    *   «один-ко-многим»:	-
    *   «многие-ко-многим»:	Service (через таблицу Service_Request), Employee (через таблицу Request_Employee);
    *   «один-к-одному»:	
+ Содержит внешние ключи таблиц: - 	
+ Значение полей:	
    *   id:	Ключевое поле
	*   Price:	Стоимость заказа
	*   IdClient:	Клиент, которым был сделан заказ
	*   Session_Time:	Время сеанса
	*   Data_Finish:	Дата начала
	*   Data_Start:	Дата окончания
	*   status:	Статус заказа

**Описание таблицы Employee**

+ Название таблицы:	Employee
+ Краткое описание:	В таблице хранятся данные работников
+ Первичные ключи: id
+ Таблицы, связанные соединением: 
    *   «один-ко-многим»:	Request_Employee
    *   «многие-ко-многим»:	Service (через таблицу Request_Employee);
    *   «один-к-одному»:	
+ Содержит внешние ключи таблиц:	
+ Значение полей:	
    *   id:	Ключевое поле
	*   FIO_Employee:	Полное имя сотрудника
	*   ExperienceAge:	Опыт работы
	*   Post:	Пост
	*   Phone:	Номер телефона
	*   Birthday: 	Дата рождения сотрудника 

**Описание таблицы Service**

+ Название таблицы:	Service
+ Краткое описание:	В таблице хранится информация об услугах
+ Первичные ключи:	id
+ Таблицы, связанные соединением: 
    *   «один-ко-многим»:	Request_Service;
    *   «многие-ко-многим»:	Request (через таблицу Request_Service)
    *   «один-к-одному»:	-
+ Значение полей:	
    *   id:	Ключевое поле
	*   NameService:	Название услуги
	*   Price:	Стоимость услуги
	*   Time:	Примерное время услуги
	*   IDType:	Тип услуги

**Описание таблицы Employee_Service**

+ Название таблицы:	Employee_Service
+ Краткое описание:	В таблице хранится информация об сотрудниках и какую услугу он делает
+ Первичные ключи:	-
+ Таблицы, связанные соединением: 
    *   «один-ко-многим»:	Employee, Service;
    *   «многие-ко-многим»:	-
    *   «один-к-одному»:	-
+ Содержит внешние ключи таблиц:	Service (IDService), Employee (IDEmployee)
+ Значение полей:	
    *   IDEmployee:	Сотрудник
	*   IDService:	Услуга

**Описание таблицы Schedule**

+ Название таблицы:	Schedule
+ Краткое описание:	В таблице хранится информация о сменах работника
+ Первичные ключи:	Id
+ Таблицы, связанные соединением: 
    *   «один-ко-многим»:	-
    *   «многие-ко-многим»:	-
    *   «один-к-одному»:	Employee
+ Содержит внешние ключи таблиц:	-
+ Значение полей:	
    *   Id:	Ключевое поле
	*   IdService: 	Услуга
	*   Datefinish:	Конец смены
	*   Datestart:	Начало смены
	*   Workerid:	Работник

**Описание таблицы Type**

+ Название таблицы:	Type
+ Краткое описание:	В таблице хранится информация о типах услугах
+ Первичные ключи:	IdType
+ Таблицы, связанные соединением :
    *   «один-ко-многим»:	Service
    *    «многие-ко-многим»:	-
    *   «один-к-одному»:	-
+ Содержит внешние ключи таблиц:	
+ Значение полей:	
    *   IDType:	Ключевое поле
	*   Description:	Описание услуги
	*   Name:	Название услуги

**Описание таблицы Request_Employee**

+ Название таблицы:	Request_Employee
+ Краткое описание:	В таблице хранится информация о заказе и сотруднике, который выполняет данных заказ
+ Первичные ключи:	IDRequest
+ Таблицы, связанные соединением :
    *   «один-ко-многим»:	-
    *   «многие-ко-многим»:	-
    *   «один-к-одному»:	-
+ Содержит внешние ключи таблиц:	Employee (IDEmployee), Schedule(IDSchedule)
+ Значение полей:	
    *   IDRequest:	Заказ
	*   IDEmployee:	Сотрудник
	*   IDSchedule:	Расписание


**Описание таблицы Service_Request**

+ Название таблицы:	Service_Request
+ Краткое описание:	В таблице хранится информация о услугах, которые имеются в заказе
+ Первичные ключи:	-
+ Таблицы, связанные соединением: 
    *   «один-ко-многим»:	Service, Request
    *   «многие-ко-многим»:	-
    *   «один-к-одному»:	
+ Содержит внешние ключи таблиц:	Service (IDServcie), Request (IDRequest)
+ Значение полей:	
    *   Data_Start:	Дата начала заказа 
	*   IDService:	Услуга
	*   DataFinish:	Приблизительная дата окончания заказа
	*   IDRequest:	Заказ

