Лаба 1
1.Выберите из таблицы orders все заказы
SELECT * FROM orders;
![415884576-23460e5a-748e-4c98-af98-3b637623958c](https://github.com/user-attachments/assets/f3c0cc0b-c957-4b93-a2a9-8bfa88fdf510)
2.Выберите из таблицы orders все заказы кроме новых. У новых заказов status равен "new". Использовать in
SELECT * FROM orders WHERE STATUS IN ('cancelled','in_progress','delivery');

![415884825-37ed988f-4a88-4c2b-bc07-a68dc8c8b53f](https://github.com/user-attachments/assets/a59ef17e-96c3-47af-ad28-39047de989ca)


3.Выберите из таблицы orders все новые и отмененные заказы. У отмененных заказов status равен "cancelled". У новых заказов status равен "new".
SELECT *FROM orders WHERE STATUS IN ('new', 'cancelled');
 ![415884896-9bc193b2-02e3-4e4e-aaef-d6ea182e538e](https://github.com/user-attachments/assets/a4a038c7-9fed-40f5-b32b-ac653b7a3a4b)

4.Выберите из таблицы orders все заказы содержащие более 3 товаров (products_count). Вывести нужно только номер (id) и сумму (sum) заказа.
SELECT id, SUM FROM orders WHERE products_count >3;
![415885262-2f208a4d-1ca9-4cfb-8e36-058f3dc827e7](https://github.com/user-attachments/assets/9519238c-32a1-47d6-a7e9-a003f3c8a91e)
