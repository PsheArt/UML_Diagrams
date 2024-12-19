## Описание класса Request

Класс для работы с заказами тату-салон

### Атрибуты
+ ID:Int
+ Client:[Client](Client.md)
+ DateStart:DateTime
+ DateFinish:Datetime
+ status:String
+ service:[Service(,)](Service.md)
+ name_request:String
+ PriceR:Double
### Описание атрибутов
+ ID:Int - идентификатор в БД
+ Client:[Client](Client.md) - клиент 
+ DateStart:DateTime - дата начала заказа
+ DateFinish:Datetime - примерное оканчание заказа
+ status:String - статус заказа
+ service:[Service(,)](Service.md) - услуга
+ name_request:String - название заказа
+ PriceR:Double - цена заказа
