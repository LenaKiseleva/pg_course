Подготовка окружения
```bash
docker run --name habr-pg-17.0 -p 5432:5432 -e POSTGRES_USER=root -e POSTGRES_PASSWORD=root -e POSTGRES_DB=root -d postgres:17.0
```

```bash
apt update && apt install pgcli wget -y
```

```bash
pgcli -U root -d root
> create role postgres; 
```

```bash
wget https://storage.googleapis.com/thaibus/thai_small.tar.gz && tar -xf thai_small.tar.gz && psql < thai.sql
```

Подсчитываем тикеты
```sql
thai> select count(*) from book.tickets;
+---------+
| count   |
|---------|
| 5185505 |
+---------+
SELECT 1
Time: 0.089s
thai>
```
