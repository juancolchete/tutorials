# Wordpress on Docker
```bash
ip -json route get 8.8.8.8 | jq -r '.[].prefsrc'
```
```bash
docker run --name wpDB -p 3306:3306 -e MYSQL_ROOT_PASSWORD=123456!@change --network wp -d mysql:latest
```
```bash
docker run --name wpLocal -p 8080:80 --network wp -d wordpress
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
