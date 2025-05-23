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

Лаба 2
1.Выберите из таблицы orders 3 самых дешевых заказа за всё время. Данные нужно отсортировать в порядке убывания цены. Отмененные заказы не учитывайте.

SELECT * FROM orders WHERE STATUS != 'отменен' ORDER BY sum ASC LIMIT 3;

![415886747-6de610d5-391d-46e1-b894-db1ed9330e77](https://github.com/user-attachments/assets/f4b0cd59-d6af-4417-bff8-ad573a5e03b8)

2.Выберите из таблицы orders 2 самых дорогих заказов за всё время. Данные нужно отсортировать в порядке убывания цены. Отмененные заказы не учитывайте.

SELECT * FROM orders WHERE STATUS != 'отменен' ORDER BY sum DESC LIMIT 2;

![415886816-3f8fe9e3-d4f4-4b08-b5ed-0d374fe9bebf](https://github.com/user-attachments/assets/864184cf-bccb-4551-84ca-0d9ae57dbdfe)


3.Добавьте в таблицу orders данные о новом заказе стоимостью 8000 рублей. В заказе 4 товара (products).

INSERT INTO orders (id, products, sum) VALUES (6, 4, 8000);

![418255956-11d54dfc-f39b-4381-8b39-08db0a22c9a2](https://github.com/user-attachments/assets/56f82329-d463-4914-9282-b873f6f8d880)

![418255968-7472531a-e42f-458c-9899-9699d2e65cea](https://github.com/user-attachments/assets/37ff1a0a-8ada-494c-a358-7a15f3932364)



4.Добавьте в таблицу products новый товар — «VR-очки», стоимостью 70000 рублей в количестве (count) 2 штук.

INSERT INTO products (id, name, price, count) VALUES (7, 'VR-очки', 70000, 2);
![418256147-dabf7dc4-b441-4a55-8bea-48950d5cd7dc](https://github.com/user-attachments/assets/8c1145ce-2cbd-43d3-9b43-ccbb4685d06f)

![418255956-11d54dfc-f39b-4381-8b39-08db0a22c9a2 (1)](https://github.com/user-attachments/assets/600e0c09-672e-4c80-ac20-9fec60f384f7)

5.В таблицу products внесли данные с ошибкой, вместо "PS5" в наименовании написали IMAC. Исправьте ошибку.

UPDATE products SET name = 'PS5' WHERE name = 'IMAC';

![418256518-45f95fbc-ed0f-4fd9-bc35-5b8a190ecc46](https://github.com/user-attachments/assets/bf1b6d3b-8619-4cb2-bb48-5b302590949f)

![418256567-1288a625-6daf-4162-8be0-1e61b328eea4](https://github.com/user-attachments/assets/69fd980a-3354-45c3-87c3-ed14389eff3d)
