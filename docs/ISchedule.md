## Описание интерфейса ISchedule

Интерфейс предназначен для работы с методами класса [Schedule](Schedule.md)

### Реализация интерфейса

- +Add (Schedule: [Schedule](Schedule.md)): String — функция, добавляющая расписание сотрудника в базу данных. Параметр «[Schedule](Schedule.md)» — расписание, которое необходимо добавить в БД;

- +Save (Schedule: [Schedule](Schedule.md)): String — функция, сохраняющая расписание. Параметр «[Schedule](Schedule.md)» — расписание, которое необходимо сохранить в БД;

- +Edit (Schedule: [Schedule](Schedule.md)): String — функция, редактирующая расписание. Параметр «[Schedule](Schedule.md)» — расписание, которое необходимо редактировать в БД;

- +Delete (ID): Int — функция удаляет расписание сотрудника из БД;

- +FindAll(sortingA:string,sortingB:string, filterA:[Schedule](Schedule.md),filterB:[Schedule](Schedule.md), count:int, page:int):List<[Schedule](Schedule.md)> - функция, возвращающая расписание сотрудников, удовлетворяющих заданным параметрам.                                          
Параметры:                                                                                                             
+ sorting: string — отвечает, по какому полю будет сортироваться список;
+ sortingА: string — отвечает, по возрастанию или убыванию будут сортироваться элементы;
+ filterA: [Schedule](Schedule.md) — отвечает за фильтрацию;
+ filterB: [Schedule](Schedule.md) — необходим для количественных атрибутов;
+ count: int — отвечает, сколько элементов необходимо показать;

- +GetEmployee(IDSchedule:Int):List< [Employee](Employee.md) > функция, возвращающая работников, которые работают в определенный день.

