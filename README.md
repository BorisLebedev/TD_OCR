**Что делает**

Переименовывает pdf документы (маршрутные карты)

**Как работать**

1. Скопировать сканированные маршрутные карты в папку scan (есть образец для тестирования)
2. Запустить скрипт
3. Переименованные документы будут скопированы в папку documents

**Ограничения**

Тип документа: Маршрутная карта

Форма документа: Форма 2

Положение документа: развернут на 270 градусов

**Как работает скрипт**

1. Подготавливает изображение титульного листа документа

2. Вырезает области где должен находиться текст реквизитов документа (наименование, децимальные номера конструкторской и технологической документации)

3. Извлекает децимальные номера поиском через регулярные выражения

4. Ищет наименование документа в БД по децимальному номеру и меняет название если находит

5. Копирует в папку documents документ с новым наименованием и удаляет документ из папки scan или оставляет документ в папке scan, если документ не распознан
