docker run --name db -e MYSQL_ROOT_PASSWORD=123456 -e MYSQL_DATABASE=worldapi -e MYSQL_USER=devspark -e MYSQL_PASSWORD=dev123 -d mysql:5.6

docker run --name appwebserver -p 80:80 --link db:mysql -d dockerfinalproject_appwebserver:latest