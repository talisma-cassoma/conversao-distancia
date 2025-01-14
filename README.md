# conversao-distancia

- [x] Gere uma imagem Docker a partir do Dockerfile criado.

    ```dockerfile
    FROM python

    WORKDIR /usr/app

    COPY requirements.txt .

    RUN pip3 install -r requirements.txt

    COPY . .

    EXPOSE 5000

    CMD [ "gunicorn", "--bind", "0.0.0.0:5000", "app:app" ]
    ```
- [x] Execute um contêiner a partir da imagem para garantir que a aplicação esteja acessível na porta 5000.
    <img src="assets/terminal.png">

- [x] Realize testes básicos na aplicação para verificar a funcionalidade de conversão de métricas.
    <img src="assets/web_app.png">

    link para imagem : https://hub.docker.com/repository/docker/talisma/conversao-distancia/general
    

    comando para baixar da imagem  
    
    ```bash
    docker pull talisma/conversao-distancia:latest
    ```