# Wordpress on Docker
```bash
docker run --name wpDB -p 3306:3306 -e MYSQL_ROOT_PASSWORD=123456!@Change -d mysql:latest
```
```bash
sudo pacman -S mysql
```
or
```bash
sudo apt install mysql
```
```bash
mysql -u root -h 127.0.0.1 -p
```
```bash
CREATE DATABASE wordpress;
```
```bash
CREATE USER 'wordpress'@'%' IDENTIFIED BY '123456!@Change';
```
```bash
GRANT ALL PRIVILEGES ON *.* TO 'wordpress'@'%' WITH GRANT OPTION;
```
```bash
FLUSH PRIVILEGES;
```
```bash
exit
```
```bash
docker run --name wpLocal -p 8080:80 -d wordpress
```
```bash
sudo pacman -S jq
```
or
```bash
sudo apt install jq
```
```bash
ip -json route get 8.8.8.8 | jq -r '.[].prefsrc'
```
