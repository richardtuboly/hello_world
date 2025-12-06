# Hello World – beadandó projekt

Egyszerű Python + Flask alkalmazás DevOps alapok bemutatására:

- kód
- trunk-based Git használat
- buildelés
- Dockerizálás
- CI pipeline + Docker registry

## 1. Alkalmazás

Az app HTTP-n érhető el, alapértelmezés szerint:

- URL: http://localhost:8080/
- Válasz: egyszerű szöveg – "Hello World!"

## 2. Környezet és buildelés

### Előfeltételek

- Python 3.12
- pip

### Build és futtatás lokálisan

### virtuális környezet létrehozása

python -m venv venv
source venv/bin/activate

### build (függőségek telepítése)

pip install -r requirements.txt

### futtatás

python app.py

### Docker image build

docker build -t hello_world:v1 .

### Docker image futtatás

docker run --rm -p 8080:8080 hello_world:v1

#### böngészés

http://localhost:8080

### Image lehúzása Docker Hub-ról

docker pull richardtuboly/hello-devops:latest

### Futtatás

docker run --rm -p 8080:8080 richardtuboly/hello-devops:latest
