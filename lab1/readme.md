# My lab #2
https://lab2-ny1h.onrender.com

Для запуску у себе на пк 

Потрібно клонувати проект в свою робочу директорію:
```
https://github.com/NastyaSira/lab2.git
```
Створити віртуальне середовище за допомогою venv:
```
python3 -m venv venv
```
Активувати віртуальне середовище:
```
source ./venv/bin/activate
```
Встановити flask та решту за допомогою команди:
```
pip install flask
```
```
pip install -r requirements.txt
```
Тут є .flaskenv файл, тому потрібно поставити python-dotenv:
```
pip install python-dotenv
```
Далі можна збілдити image такою командою:
```
docker build --build-arg PORT=<your port> . -t <image_name>:latest
```
Якщо image упішно збілдився, то його можна запустити і перевірити:
```
docker run -it --rm --network=host -e PORT=<your port> <image_name>:latest
```
Збілдити контейнер: 
```
docker-compose build
```
Запустити контейнер:
```
docker-compose up
```