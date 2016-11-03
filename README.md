
Обсуждение тут - http://forum.imagecms.net/viewtopic.php?id=4988

### Конструктор форм - xforms для ImageCMS

## Обратите внимание!
Файлы модуля должны находиться в папке /application/modules/xforms

Модуль корректно работает с ImageCMS версий 4.9,4.10 и 4.11

#### UPD: 04/11/16
* Исправлена ошибка в tpl письма + добавлена функция скачивания файлов

#### UPD: 19/10/16 - Версия 2.3
* Добавил новый тип поля, для формы, - "загрузка файла". Можно загружать файлы через ajax и выбирать какие типы файлов разрешено загружать.
* Теперь можно сделать первое значение select/checked/radio выбранным по умолчанию.
* Косметические исправления при редактировании поля в админке.
* checkbox работает как надо

Для обновления модуля с версии 2.0 до 2.3 замените все файлы модуля, а так-же зайдите в админ панель и перейдите по адресу - /admin/components/cp/xforms/update_2_3/

#### UPD: 11/06/16
* Теперь работают типы поля checkbox и исправил ошибки в radio
* Модуль будет по умолчанию отправлять письсма через SMTP если он у вас настроен.

#### UPD: 11/05/16
* При создании поля, его позиция по умолчанию = ID поля, если она не указана. (поле помещается в конец списка)


### Что сделано?
* Отправка почты на несколько email адресов.
* Все формы на AJAX и отправляются без перезагрузки страницы.
* Теперь поля можно включать и выключать.
* Переписан дизайн админ панели для формы, теперь нет глюков.
* Добавлена функция запрета прямого доступа к форме через УРЛ. (не путать с запретом доступа к модулю через УРЛ)
* Добавлена функция прикрепления файлов к форме. (нужно создать поле "загрузка файла" к форме)
* Форму мы можем встроить как виджет, но перейдя по ссылке формы, будет 404 ошибка.
* Добавнена функция "защитный код (каптча)". Если в форме есть ошибки, капча автоматически обноавляется.
* Уведомление об ошибках "на лету", т.е. если вы ввели что то неправильно в поле, вылазит уведомление об ошибке (после нажатия на кнопку отправить)
* Есть такой мифический тип поля, при создании - "разделитель". Нужен например для визуального отделения мелких групп полей. Не стал заморачиваться с fieldset и legend. Возможно в будущем поля будут иметь доп. свойство - группировка.

###Что не работает?
* Нет дефолтных стилей формы, позже будут дописываться.


###Что в планах? (в порядке убывания приоритетов)
* Сохранение сообщенией в админ панель, и там же отмечать (просмотрено, не просмотрено)
* Интегрировать настройки отправки почты через модуль "Управление email-уведомлениями"
* группировка полей в fieldset или что-то подобное.
* Добавить дефолтные стили.
* Добавление новых типов полей (Телефон, email итд. input'ов из HTML5)
* JS валидация в соответствии с выставленными условиями проверки (valid_email|max_length[255]|min_length[1]|numeric итд)
* Добавление поля Time, data и time data. (На основе Js - datetimepicker)