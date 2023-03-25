# Main Branch
This is CA2 from Secure Application Programming
As requested on part4:

Part 4										20%
Check out your master or main branch of the repository created in part 3.
Modify the  README.md file to include the following instructions in a code block you can use the following cheatsheet to assist you.
 https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
•	provide a command that will create a docker network.
•	Provide a command that will run a mysql:latest docker image with the name of db with a root password=my-secret-password.
•	Provide a command that will run the docker image phpmyadmin/phpmyadmin on the network previously created mapping a port of your choice to port 80 of the container
Reference 
https://hub.docker.com/_/mysql  
https://hub.docker.com/_/phpmyadmin 



Here you can find the steps:


# Create a docker network
docker network create mynetwork

# Run a MySQL docker image with the name of db and root password=my-secret-password
docker run -d --name db --network mynetwork -e MYSQL_ROOT_PASSWORD=my-secret-password mysql:latest

# Run the phpMyAdmin docker image on the mynetwork network, mapping a port of your choice to port 80 of the container
docker run -d --name phpmyadmin --network mynetwork -p <host_port>:80 -e PMA_HOST=db phpmyadmin/phpmyadmin









Built With

Markup (HTML)
Styles (CSS)

Visit Repo
https://github.com/Igor-dos-santos/CA2_SecureApp 

Author
👤 Igor Dos Santos

GitHub: @Igor-dos-santos
LinkedIn: @igor-dos-santos