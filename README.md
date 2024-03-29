Проектирование Базы данных интернет магазина ***(SQL)***
=================

Интернет магазин будет специализироваться на продаже любых видов товаров: телефоны, машины, одежда

Какие данные необходимо хранить
-----------------------

* Описание сайта
	* Meta данные (title, description, keywords)
	* Название страницы
	* URL страницы ***пример: http://site.ru/about/  — храним только about***
		* Уникальный путь в рамках текущего шага ***пример: в родителе уникально; в ребёнке не уникально***

	* Контент страницы
	* Активная страница или не активная (опубликованная или скрытая)

* Категории товаров ***(неограниченное кол-во вложений)***
	* Название
	* URL
	* Описание
	* Статус опубликова или нет

* Карточка товара
	* Meta данные (title, description, keywords)
	* Название товара
	* Описание
	* Категория товара ***товар может принадлежать к нескольким категориям***
	* Характеристики товаров
		* Бренд
		* Хранение разных типов
			* Цвет
			* Размер
			* Вес
			* Габариты (для доставки)
			* Прочее
	* URL карточки товара
		* URL абсолютно уникальный! 
	* Фотографии к товару
		* Одна либо несколько
		* Главное изображение или второстепенное (что бы можно было изменять порядок вывода)
		* alt&title изображения
		* Название фотографии
	* Комментария к товару ***(только зарегистрированные пользователи могут оставлять комменты)***
	* Кол-во товаров на складе 
	* Цена
	* Дата и время создание товара

* Пользователи
	* Данные пользователя
		* ФИО
		* Тел **(уникальный)**
		* Email **(уникальный)**
		* Кол-во заказов
			* Номер накладной заказа **(уникальный)**
			* Что клиент заказал
			* Стоимость
			* Дата + Время
			* Какой источник привёл к совершению покупке ***пример: органический поиск, реклама (определяем по utm-меткам)***
			* Статус заказа 
				* Новый
				* Обработан
				* Ожидает доставки
				* Доставляется
				* Доставлен
				* Отменён
				* Перенесён
			* Статус оплаты
				* Оплачен 
				* Не оплачен

* Реклама
	* Виды рекламы
		* Контекстная реклама
			* Название рекламной компании
			* Площадка 
			* Вид рек. носителя
			* Группа рек. 
			* Дата начала рек
			* Дата конца рек
		* Социальные сети
			* .....

* Поиск на сайте
	* По Артикулам товаров
	* По описанию и назваию (полнотекстовый) ***Приоритет: Артикул, Название, Описание***

* Аналитика продаж
	* По пользователям
	* По группам товаров
	* По товару
	* За отрезок времени



> **Что необходимо участь:**
> > URL адреса
> > > В ходе публикаций содержимого на сайте, через N время может потребоваться оптимизировать название URL адреса текущего содержимого. ***пример: tovar-1 решите переименовать в ЧПУ iphone-6s-32gb-grey*** Если мы не будем хранить старый URL, то при переходе пользователя через поиск по старому URL адресу у него будет выходить ошибка! — 404 страница не найдена! Во избежание данного факапа необходимо учесть момент хранения и изменения URL адресов

> > Цены
> > > Цены к товару могут изменяться, необходимо учесть данный момент что бы не было исторического факапа по продажам или анализу изменения цен

> > Поиск по сайту
> > > Полнотекстовый поиск, очень опасный метод. Так как при присвоение полнотекстового индекса, все данные будут храниться в оперативке;



Задание
========
1. Спроектировать базу данных
2. Описать принцип взаимодействия таблиц и хранения данных
3. Поля в таблицах прокомментируйте (что за что и для чего)
4. Заполнить тестовыми данными:
	* Добавить несколько страниц сайта
		* Главная страница, О компании, Контакты... 
		* Эллектроника / Смартфоны / Apple / 
			* iphone 6, iphone 7 + Характеристики
		* Гаджеты / Самокаты
		* Гаджеты / Велосипеды
	* Оформить несколько заказов с разными статусами



