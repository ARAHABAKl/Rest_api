# Rest_api

## Требования

Предполагается, что у вас установлена ОС Windows, но вы также можете запустить этот проект на других ОС.

**Windows**

- `OSPanel` установлен
- `PhpStorm` установлен
- Установлено любое потребительское приложение rest, напримерPostman, или любой плагин REST client в любом браузере (например, "Расширенный клиент REST" в Chrome).

## Настройка

Скопируйте проект.

```bash
git clone --recurse-submodules https://github.com/ARAHABAKl/Rest_api.git .
```


Создайте новую базу данных MySQL.

```SQL
CREATE DATABASE phpapidb;
```

Запустить SQL-скрипт для создания таблицы.

```SQL
CREATE TABLE IF NOT EXISTS `Employee` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(256) NOT NULL,
  `email` varchar(50),
  `age` int(11) NOT NULL,
  `designation` varchar(255) NOT NULL,
  `created` datetime NOT NULL,
  PRIMARY KEY (`id`)
)ENGINE=InnoDB  DEFAULT CHARSET=utf8 AUTO_INCREMENT=19
```
Заполните данные в `Employee` таблицу.

```SQL
INSERT INTO `Employee` (`id`, `name`, `email`, `age`, `designation`, `created`) VALUES 
(1, 'John Doe', 'johndoe@gmail.com', 32, 'Data Scientist', '2012-06-01 02:12:30'),
(2, 'David Costa', 'sam.mraz1996@yahoo.com', 29, 'Apparel Patternmaker', '2013-03-03 01:20:10'),
(3, 'Todd Martell', 'liliane_hirt@gmail.com', 36, 'Accountant', '2014-09-20 03:10:25'),
(4, 'Adela Marion', 'michael2004@yahoo.com', 42, 'Shipping Manager', '2015-04-11 04:11:12'),
(5, 'Matthew Popp', 'krystel_wol7@gmail.com', 48, 'Chief Sustainability Officer', '2016-01-04 05:20:30'),
(6, 'Alan Wallin', 'neva_gutman10@hotmail.com', 37, 'Chemical Technician', '2017-01-10 06:40:10'),
(7, 'Joyce Hinze', 'davonte.maye@yahoo.com', 44, 'Transportation Planner', '2017-05-02 02:20:30'),
(8, 'Donna Andrews', 'joesph.quitz@yahoo.com', 49, 'Wind Energy Engineer', '2018-01-04 05:15:35'),
(9, 'Andrew Best', 'jeramie_roh@hotmail.com', 51, 'Geneticist', '2019-01-02 02:20:30'),
(10, 'Joel Ogle', 'summer_shanah@hotmail.com', 45, 'Space Sciences Teacher', '2020-02-01 06:22:50');
```
### Запуск

Запустите `Postman` протестируйте приложение по следующему URL.

```url
http://php-rest-api/api/
```
  
## Применение

### Получить информацию о всех

* `GET - http://php-rest-api/api/read.php`


![image](https://github.com/ARAHABAKl/Rest_api/assets/53332177/2babe726-a3b2-43af-9ecf-5d66884532ae)

___
### Получить информацию о пользователе

* `GET - http://php-rest-api/api/single_read.php/?id=2`


![image](https://github.com/ARAHABAKl/Rest_api/assets/53332177/2babe726-a3b2-43af-9ecf-5d66884532ae)

___
### Добавить пользователя

**Метод**
* `POST - http://php-rest-api/api/create.php`


![image](https://github.com/ARAHABAKl/Rest_api/assets/53332177/7d3dd71f-5341-49da-b6d7-19440d777945)

___
### Обновить пользователя

**Метод**
* `POST - http://php-rest-api/api/update.php`


![update](https://github.com/ARAHABAKl/Rest_api/assets/53332177/5e29b66b-8c0e-44e6-b18b-bfc24f1a3e7d)

___
### Удалить пользователя

**Метод**

* `DELETE - http://php-rest-api/api/delete.php`


![image](https://github.com/ARAHABAKl/Rest_api/assets/53332177/51a3ff1f-e0ff-4392-b080-8cda5110d4a4)
