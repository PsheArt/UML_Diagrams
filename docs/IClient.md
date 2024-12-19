## Описание интерфейса IClient

Интерфейс предназначен для работы с методами класса [Client](Client.md)

### Реализация интерфейса

- +Add (Client: [Client](Client.md)): String — функция, добавляющая клиента в базу данных. Параметр «[Client](Client.md)» — клиент, которого необходимо добавить в БД;

- +Save (Client:[Client](Client.md)): String — функция, сохраняющая данные о клиенте. Параметр «[Client](Client.md)» — клиент, которого необходимо сохранить в БД;

- +Edit (Client:[Client](Client.md)): String — функция, редактирующая данные о клиенте. Параметр «[Client](Client.md)» — клиент, которого необходимо редактировать в БД;

- +Delete (ID): Int — функция удаляет клиента из БД;

- +FindAll(sortingA:string,sortingB:string, filterA:[Client](Client.md),filterB:[Client](Client.md), count:int, page:int):List<[Client](Client.md)> -  функция, возвращающая всех клиентов, удовлетворяющих заданным параметрам.
Параметры:
+ sorting: string — отвечает, по какому полю будет сортироваться список;
+ sortingА: string — отвечает, по возрастанию или убыванию будут сортироваться элементы;
+ filterA:[Client](Client.md) — отвечает за фильтрацию;
+ filterB:[Client](Client.md) —необходим для количественных атрибутов;
+ count: int — отвечает, сколько элементов необходимо показать;
+ page: int — отвечает, с какой страницы начинать поиск элементов.

- +GetService(IDClient:Int):List< [Service](Service.md) > функция, возвращающая список услуг, которые оказывались/оказываются клиенту.

- +GetRequest(IDClient:Int):List< [Request](Request.md) >  - функция, возвращающая список заказов клиентов.
