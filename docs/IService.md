## Описание интерфейса IService

Интерфейс предназначен для работы с методами класса [Service](Service.md)

###Реализация интерфейса

- +Add (Service: [Service](Service.md)): String — функция, добавляющая услугу в базу данных. Параметр «[Service](Service.md)» — услуга, которую необходимо добавить в БД;

- +Save (Service: [Service](Service.md)): String — функция, сохраняющая данные о услуге. Параметр «[Service](Service.md)» — услуга, которую необходимо сохранить в БД;

- +Edit (Service: [Service](Service.md)): String — функция, редактирующая данные о услуге. Параметр «[Service](Service.md)» — услуга, которую необходимо редактировать в БД;

- +Delete (ID:int): Int — функция удаляет услугу из БД;

- +FindAll(sortingA:string,sortingB:string, filterA:[Service](Service.md),filterB:[Service](Service.md), count:int, page:int):List< [Service](Service.md) > -  функция, возвращающая список услуг, удовлетворяющих заданным параметрам.
Параметры: 

+ sorting: string — отвечает, по какому полю будет сортироваться список;
+ sortingА: string — отвечает, по возрастанию или убыванию будут сортироваться элементы;
+ filterA: [Service](Service.md) — отвечает за фильтрацию;
+ filterB: [Service](Service.md) —необходим для количественных атрибутов;
+ count: int — отвечает, сколько элементов необходимо показать;

- +GetClient(IDService:Int):List< [Client](Client.md) > - функция возвращает список клиентов, у которых была данная услуга
