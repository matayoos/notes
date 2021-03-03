## Wednesday, March 3, 2021, 5:23:11PM -03 <1614802991>

### Add new user

https://www.digitalocean.com/community/tutorials/how-to-create-a-new-user-and-grant-permissions-in-mysql

## Tuesday, March 2, 2021, 11:09:55AM -03 <1614694195>

### Add a foreign key to an existing table

- ALTER TABLE invoice ADD grocery_store_id INT NOT NULL;
- ALTER TABLE invoice ADD CONTRAIT fk_grocery_store FOREIGN KEY
  (grocery_store_id) REFERECES grocery_store(id);

## Tuesday, March 2, 2021, 8:59:35AM -03 <1614686375>

### Delete row MySQL

- DELETE FROM **table_name** WHERE [condition];

### Drop column

- ALTER TABLE **table_name** DROP COLUMN column_name;

### Add column

- ALTER TABLE table ADD [COLUMN] column_name column_definition [FIRST|AFTER existing_column];

## Monday, March 1, 2021, 4:31:54PM -03 <1614627114>

### Error 1698
- sudo mysql -u root
- ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'test'; 
  - Note: here test is a new password for the root user. 
- sudo service mysql restart
