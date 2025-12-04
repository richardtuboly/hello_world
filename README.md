# virtuális környezet létrehozása

python -m venv venv
source venv/bin/activate

# függőségek telepítése

pip install -r requirements.txt

# futtatás

python app.py

# Docker image build

docker build -t hello-devops:v1 .

# Docker image futtatás

docker run --rm -p 8080:8080 hello-devops:v1

# böngészés

http://localhost:8080
