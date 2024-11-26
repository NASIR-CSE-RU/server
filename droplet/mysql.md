## 1. Log in to MySQL as root
If you're logged in as a non-root user, you’ll need to log in as root to create the database and assign permissions:

```bash
sudo mysql -u root -p
```
You’ll be prompted to enter the root password.

## 2. Create the New Database
Once you're logged into MySQL, create the new database:

```sql
CREATE DATABASE new_database_name;
```
Replace new_database_name with your desired database name.

## 3. Grant All Privileges to root
Now, assign all privileges to the root user for the new database:

```sql
GRANT ALL PRIVILEGES ON new_database_name.* TO 'root'@'localhost';
```
This command grants full access to the root user for the newly created database.


## 4. Flush Privileges
After granting permissions, run the following command to apply the changes:

```sql
FLUSH PRIVILEGES;
```
## 5. Exit MySQL
Exit the MySQL prompt:

```sql
EXIT;
```