- There are 50 users.

``SELECT COUNT(*) FROM users;
``

- Five most expensive items: 1) Small Cotton Gloves 2) Small Wooden Computer 3) Awesome Ganite Pants 4) Sleek Wooden Hat 5) Ergonomic Steel Car
  60|Ergonomic Steel Car|Books & Outdoors|Enterprise-wide secondary firmware|9341
  40|Sleek Wooden Hat|Music & Baby|Quality-focused heuristic info-mediaries|9390
  100|Awesome Granite Pants|Toys & Books|Upgradable 24/7 access|9790
  83|Small Wooden Computer|Health|Re-engineered fault-tolerant adapter|9859
  25|Small Cotton Gloves|Automotive, Shoes & Beauty|Multi-layered modular service-desk|9984

``SELECT * FROM items WHERE category = 'Books' ORDER BY price DESC LIMIT(1);
``

- The cheapest book is from the Books only category is "Fantastic Steel Chair"

``SELECT * FROM items WHERE category = 'Books' ORDER BY price DESC LIMIT(1);
  ``

  The cheapest book when opening the search to any category with a Books is "Awesome Granite Pants"

`` SELECT * FROM items WHERE category LIKE "%Books%" ORDER BY price DESC LIMIT(1);
``

- Corrin Little lives at 6439 Zetta Hills, Willmouth, WY. 2nd address at 54369 Wolff Forges, Lake Bryon CA 31587.
  40|Corrine|Little|rubie_kovacek@grimes.net
  43|40|6439 Zetta Hills|Willmouth|WY|15029
  44|40|54369 Wolff Forges|Lake Bryon|CA|31587

``SELECT * from addresses WHERE street LIKE '%ZETTA%';
  SELECT * FROM user where id=40;
  SELECT * FROM addresses where user_id=40;
    ``

- Virinie Mitchell's address has been updated shown
  41|39|12263 Jake Crossing|New York|NY|34705
   42|39|83221 Mafalda Canyon|Bahringerland|WY|24028

``UPDATE addresses SET city = 'New York' WHERE street = '12263 Jake Crossing';
  ``

- It would cost $46477 to buy one of each tool.

``SELECT sum(price) FROM items WHERE category like "%Tools%";
``

- 2125 items were sold.

``SELECT SUM(quantity) FROM orders;
``

- Total amount spent on books $420,566

``SELECT SUM(price*quantity)
  FROM orders
  JOIN items
  ON orders.item_id = items.id
  WHERE category = 'Books';
``

- 51    Naghmeh        Shirazi  ndrs@email.com

``INSERT INTO (first_name, last_name, email)
  values('Naghmeh', 'Shirazi', 'ndrs@email.com');
  ``

  78   51             4     14    2016-03-28 20:43:02

  ``INSERT INTO orders (user_id, item_id, quantity, created_at)
    VALUES (51, 4, 14, 2015-03-28);
    ``

  378   51             4     14    1984

  ``UPDATE orders SET created_at = CURRENT_TIMESTAMP
    WHERE created_at = 1984;
  ``
  SELECT * FROM orders;
  - Most ordered item Incredible Granite Car.
    72|65|Incredible Granite Car

    ``SELECT sum(orders.quantity) AS "sum", orders.item_id, items.title
    FROM orders INNER JOIN items ON orders.item_id = items.id
    GROUP BY orders.item_id ORDER BY sum DESC LIMIT 1;
    ``

  
