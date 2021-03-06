# Add Data to a Table with SQL Insert

## 1.  Add Static Data

### Query
```sql
insert into Products (create_date, product_id, title, description, price, technology) values ('2018-06-06', 'b1debc99-9c0b-4ef8-bb6d-6bb9ac380bb1', 'sql fundamentals course', 'This course is designed to take someone that has no experience with relational databases and teach them how to at least create, read, update, and delete.', '100.00', 'sql');
```
### Output
| create_date              | product_id                           | title                                              | description                                                                                                                                               | price   | technology                                         |
| ------------------------ | ------------------------------------ | -------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- | -------------------------------------------------- |
| 2018-06-06T00:00:00.000Z | b1debc99-9c0b-4ef8-bb6d-6bb9ac380bb1 | sql fundamentals course                            | This course is designed to take someone that has no experience with relational databases and teach them how to at least create, read, update, and delete. | $100.00 | sql                                                |

---

## 2. Add Dynamic Data

### Query
```sql
insert into Products (create_date, product_id, title, description, price) values (now(), uuid_generate_v4(), 'react course', 'This course you will learn all about React.', '250.00');
```

or Shorthand:

```sql
insert into Products values (now(), uuid_generate_v4(), 'react course', 'This course you will learn all about React.', '250.00', 'react');
```

### Output
Something similar to:

| create_date              | product_id                           | title                                              | description                                 | price   | technology                                         |
| ------------------------ | ------------------------------------ | -------------------------------------------------- | ------------------------------------------- | ------- | -------------------------------------------------- |
| 2019-04-12T00:00:00.000Z | 49a24487-478e-4007-b204-3f924b087923 | react course                                       | This course you will learn all about React. | $250.00 | react                                              |

---