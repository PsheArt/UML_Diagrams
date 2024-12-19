## Описание интерфейса ITypeService

Интерфейс предназначен для работы с методами класса [TypeService](TypeService.md)

### Реализация интерфейса

- +Add (TypeService: [TypeService](TypeService.md)): String — функция, добавляющая тип услуги в базу данных. Параметр «[TypeService](TypeService.md)» — тип услуги, которого необходимо добавить в БД;

- +Save (TypeService: [TypeService](TypeService.md)): String — функция, сохраняющая данные о типе услуги. Параметр «[TypeService](TypeService.md)» — тип услуги, которого необходимо сохранить в БД;

- +Edit (TypeService: [TypeService](TypeService.md)): String — функция, редактирующая данные о типе услуги. Параметр «[TypeService](TypeService.md)» — тип услуги, которого необходимо редактировать в БД;

- +Delete (ID): Int — функция удаляет сотрудника из БД;

+FindAll(sortingA:string,sortingB:string, filterA:[TypeService](TypeService.md),filterB:[TypeService](TypeService.md), count:int, page:int):List< [TypeService](TypeService.md) > - функция, возвращающая список типы услуг, удовлетворяющих заданным параметрам.
Параметры:
+ sorting: string — отвечает, по какому полю будет сортироваться список;
+ sortingА: string — отвечает, по возрастанию или убыванию будут сортироваться элементы;
+ filterA: [TypeService](TypeService.md) — отвечает за фильтрацию;
+ filterB: [TypeService](TypeService.md) —необходим для количественных атрибутов;
+ count: int — отвечает, сколько элементов необходимо показать;
