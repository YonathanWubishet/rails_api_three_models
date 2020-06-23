# README

Rails Pods API Creation Steps:

1. Run 'rails new pods_api -d mysql --api'

The --api option will create just an api folder structure.

It will not have the views folder and other folders which would have been included in a monolithic rails app.

The -d option will add the mysql2 gem in the Gem file along with all related mysql dependecies.

2. Now, enter the command 'cd pods_api' to switch to the newly created directory.

3. Start your VS Code IDE from that directory by typing 'code .'

4. If we open the database.yml file, we'll see that the default adapter for our databse is now set to mysql2, which is what we want.
Without the --api option in the generation command, our database.yml file, would have pointed to the default database which would have been sqlite3.

5. (*If the mysql server is not installed in the machine, it would be necessary to install mysql server from https://dev.mysql.com/downloads/mysql/
Also we would have to update the password in the database.yml file with the password that we created when installing Mysql server. 
Otherwise we could get a database creation permission error when we run 'rails db:migrate', which looks like this:
Access denied for user 'root'@'localhost' (using password: NO)
Couldn't create 'pods_api_development' database. Please check your configuration.
rails aborted!
Mysql2::Error::ConnectionError: Access denied for user 'root'@'localhost' (using password: NO))

6. After verifying that our password has been set and that all entries in the database.yml file looks correct, we can now run 'rails db:create', to create the database 
(alternatively, we could use PHPmyadmin or MySQL Workbench to manually create the database, but that wouldn't be feasible, when we have the convenience and ease of the rails terminal command.).

7. Finally, run 'rails s' and and go to localhost:3000 on your browser. You should get the Rails welcome screen.