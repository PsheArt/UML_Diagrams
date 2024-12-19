## Описание интерфейса IRequest

Интерфейс предназначен для работы с методами класса [Request](Request.md)

### Реализация интерфейса

- +Add (Request: [Request](Request.md)): String — функция, добавляющая заказ в базу данных. Параметр «[Request](Request.md)» — заказ, который необходимо добавить в БД;

- +Save (Request: [Request](Request.md)): String — функция, сохраняющая данные о заказе. Параметр «[Request](Request.md)» — заказ, который необходимо сохранить в БД;

- +Edit (Request: [Request](Request.md)): String — функция, редактирующая данные о заказе. Параметр «[Request](Request.md)» — заказ, который необходимо редактировать в БД;

- +Delete (ID): Int — функция удаляет заказ из БД;

- +FindAll(sortingA:string,sortingB:string, filterA:[Request](Request.md),filterB:[Request](Request.md), count:int, page:int):List<[Request](Request.md)> - функция, возвращающая все заказы, удовлетворяющих заданным параметрам.
Параметры:
+ sorting: string — отвечает, по какому полю будет сортироваться список;
+ sortingА: string — отвечает, по возрастанию или убыванию будут сортироваться элементы;
+ filterA:[Request](Request.md) — отвечает за фильтрацию;
+ filterB:[Request](Request.md) — необходим для количественных атрибутов;
+ count: int — отвечает, сколько элементов необходимо показать;
+ page: int — отвечает, с какой страницы начинать поиск элементов.

- +GetEmployee(IDRequest:Int):List<[Employee](Employee.md) > - функция, возвращающая список сотрудников ,которые занимаются данным заказом

- +GetService(IDRequest:Int):List<[Service](Service.md)> - функция, возвращающая список услуг, которые есть в заказе. 
