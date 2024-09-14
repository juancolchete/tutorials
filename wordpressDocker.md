# Wordpress on Docker
```bash
docker run --name wpDB -p 3306:3306 -e MYSQL_ROOT_PASSWORD=123456!@Change -d mysql:latest
```
```bash
mysql -u root -h 127.0.0.1 -p
```
```bash
CREATE USER 'wordpress'@'%' IDENTIFIED BY '123456!@Change';
```
```bash
GRANT ALL PRIVILEGES ON *.* TO 'sammy'@'localhost' WITH GRANT OPTION;
```
```bash
docker run --name wpLocal -p 8080:80 -d wordpress
```
```bash
FLUSH PRIVILEGES;
```
```bash
pacman -S jq
```
or
```bash
sudo apt install jq
```
```bash
ip -json route get 8.8.8.8 | jq -r '.[].prefsrc'
```
