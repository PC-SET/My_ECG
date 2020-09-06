	Программа My ECG на Android

Программа предназначена для работы на смартфоне Android 7 и выше 
с экспериментальным медицинским прибором по детектировании ЭКГ и ФПГ человека. 

По Bluetooth происходит сопряжение со смартфоном, 
далее создаётся подключение в самой программе (сокет), 
после чего начинается стадия обмена команд.

Прибор работает в двухканальном режиме (ЭКГ и ФПГ) 
или в одноканальном (только ФПГ или ЭКГ). 

После отправки команды на смартфоне 
(нажатие на старт после настройки конфигураций), 
прибор начинает съем и отправкуp данных по беспроводному 
каналу Bluetooth на смартфон.

Данные, которые отправляются по беспроводному каналу, 
являются однобайтовыми (unsigned char). 

Диапазон чисел от 0 до 255. Если включён режим мультиканала, 
1 байт, пришедший по UART является значением ФПГ, 2 байт, значение ЭКГ, 
дальше чередуется аналогично. 

Для калибровки и защиты от ложных данных в короткий промежуток времени 
отправляется выравнивающие 2 байта (FFFF). 

	Задача

Задача смартфона в мультиканале принимать данные, отрисовывать их 
в реальном времени (в два графика) и обрабатывать их по заданному алгоритму.  
После чего необходима возможность записи данных в файл для более детальной 
обработки и исследования уже на другом устройстве или компьютере.

	Состояние на 09.2020

Программа находится в alpha версии. Более подробное описание будет опубликовано 
чуть позднее, когда пройдёт начальный этам разработки.

	Создатели 

Проект принадлежит лаборанту Саратовского Государственного Университета 
имени Чернышевского факультета Нано и Био Медицинских технологий кафедры 
Динамического Моделирования и Биомедецинской Инженерии Буднику Д.Ю.
