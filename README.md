## Тестовое задание

![](https://img.hhcdn.ru/employer-logo/1916367.png)


### Задание: 

Выберите одно из следующих приложений для тестирования:
- Калькулятор страхования ипотеки: (https://mortgage.finuslugi.ru/)
- Калькулятор страхования ОСАГО: (https://osago.finuslugi.ru/)
Произведите тестирование выбранного инструмента, используя метод черного ящика.
Составьте подробный отчет о проведенном тестировании.
Примечание: Фактические платежи через тестируемые приложения производить не следует!

Предоставление результатов:
После завершения тестирования, составьте отчет и загрузите его в облачное хранилище (например, Google Drive, Яндекс.Диск, Dropbox, OneDrive и т.д.). 
Убедитесь, что доступ к файлу открыт для просмотра, и предоставьте нам ссылку на ваш отчет.

# ВЫПОЛНЕНИЕ:

## ТЕСТ-ПЛАН:

Составитель: Александр Ощепков
Версия: 1.0

##### Оглавление:
1. Введение
2. Объект тестирования: тестируется функционал, GUI, UX, онлайн-калькулятора ОСАГО по адресу https://osago.finuslugi.ru/
3. Объем тестирования: метод тестирования - исследовательское тестирование, в котором мы проверим функционал приложения, наличие ошибок в графическом отображении, орфографические и прочие ошибки. Тестирование проводится методом "Черного ящика"
4. Тест-документация: в ходе тестирования будут подготовлен тест-план, тест-кейсы и баг-репорты в случае обнаружения дефеектов.
5. Критерии начала тестирования: тестирование начинается сразу после подготовки тест-плана.
6. Критерии окончания тестирования: тестирование будет окончено
7. Среда: тестирование проводится на системе: Процессор	Intel(R) Core(TM) i7-4700MQ CPU @ 2.40GHz   2.40 GHz Оперативная память	16,0 ГБ Тип системы	64-разрядная операционная система, процессор x64. (тестирование проводилось с турецкого IP)

###### Обнаруженные ошибки:
1. Нельзя залогиниться при расчете ОСАГО в калькуляторе ОСАГО
   Шаги: 1) зайти на страницу https://osago.finuslugi.ru/ 2) нажать на "Войти" в верхнем правом углу страницы 3) ввести регистрационные данные 4) в открывшемся ЛК нажать на выпадающий список "Новый продукт" и выбрать "Страхование"
   ОР: откроется страница со страховыми продуктами, при этом пользователь остается залогиненным
   ФР: открылась страница со страховыми продуктами, но авторизация в системе слетает
   Приоритет: High
   Серьезность: Critical
   
2. Нет ни одного предложения от страховых компаний при расчете ОСАГО
   Шаги: 1) зайти на страницу https://osago.finuslugi.ru/ 2) ввести номер автомобиля и нажать на кноку "Рассчитать" 3) заполнить все данные владельца авто и автомобиля в открывшемся окне 4) после уточнения данных выбрать желаемую дату начала страхования
   ОР: система предложит варианты от страховых компаний с ценами
   ФР: нет предложений ни от одной компании
   Приоритет: High
   Серьезность: Blocker

   ![](https://drive.google.com/file/d/1HLIHGasi3vyhD9_DUfmwlxFkBcfNXjO-/view?usp=sharing)



   # Вывод:
   Найденные ошибки имеют серьезность Critical и Blocker, что напрямую связано с невозможностью реализовать бизнес-логику приложения и несоответствию общепринятым стандартам реализации данного рода функционала.
   Релиз требует срочной доработки.
