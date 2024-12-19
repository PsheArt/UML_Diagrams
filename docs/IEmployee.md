## Описание интерфейса IEmployee

Интерфейс предназначен для работы с методами класса [Employee](Employee.md)

### Реализация интерфейса

- +Add (Employee: [Employee](Employee.md)): String — функция, добавляющая сотрудника в базу данных. Параметр «[Employee](Employee.md)» — сторудник, которого необходимо добавить в БД;

- +Save (Employee: [Employee](Employee.md)): String — функция, сохраняющая данные о сотруднике. Параметр «[Employee](Employee.md)» — сотрудник, которого необходимо сохранить в БД;

- +Edit (Employee: [Employee](Employee.md)): String — функция, редактирующая данные о сотруднике. Параметр «[Employee](Employee.md)» — сотрудник, которого необходимо редактировать в БД;

- +Delete (ID): Int — функция удаляет сотрудника из БД;

- +FindAll(sortingA:string,sortingB:string, filterA:[Employee](Employee.md),filterB:[Employee](Employee.md), count:int, page:int):List< [Employee](Employee.md) >— функция, возвращающая всех сотрудников, удовлетворяющих заданным параметрам. 
Параметры:
+ sorting: string — отвечает, по какому полю будет сортироваться список;
+ sortingА: string — отвечает, по возрастанию или убыванию будут сортироваться элементы;
+ filterA: [Employee](Employee.md) — отвечает за фильтрацию;
+ filterB: [Employee](Employee.md) —необходим для количественных атрибутов;
+ count: int — отвечает, сколько элементов необходимо показать;
+ page: int — отвечает, с какой страницы начинать поиск элементов.

- +GetService(IDEmployee:Int):List< [Service](Service.md) > - функция, возвращающая список работников, оказывающих услугу.

- +GetRequest(IDEmployee:Int):List< [Request](Request.md) > - функция, возвращающая список заказов, оказывающие работниками.

- +GetSchedule(IDEmployee:Int):List< [Schedule](Schedule.md) > функция, возвращающая расписание работника.
