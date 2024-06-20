# Aplicacion dockerizada  -- PIS5to
**Importante:** Haber inicializado Docker  
**Back-end:** http://localhost:3000/  
**Front-end:** http://localhost:7000/  

En este repositorio se encuentra la aplicacion dockerizada 
Pasos para desplegarla  
**Dirigirse al directorio de instalacion (recomendable usar el cli git bash)**
## Debe serguir los siguientes pasos (copie todas las siguientes intrucciones y presione "enter")
* git clone https://github.com/JhairDeveloper/PIS5toAplicacionDockerizada.git
* cd PIS5toAplicacionDockerizada/
* git submodule add https://github.com/Codaya007/pis-5to.git pis-5toF
* cd pis-5toF
* git checkout feature/dockerfile
* cd ..
* cp -r pis-5toF/.* pis-5to
* cp -r pis-5toF/* pis-5to
* cd pis-5to
* npm i
* cd ..
* git submodule add https://github.com/Codaya007/api-pis5to.git api-pis5toF
* cd api-pis5toF
* git checkout feature/dockerfile
* Instalacion de as variables de entorno:
  
    echo "DB_URL=mongodb+srv://grupo:9Q7MyHTMWKAstjBA@cluster0.mpdy2sr.mongodb.net/pis5to" > .env  
    echo "JWT_SECRET=mayonesa12345" >> .env  
    echo "PORT=3000" >> .env  
    echo "EMAIL_SERVICE=gmail" >> .env  
    echo "EMAIL_USER=dalton.l.maza@unl.edu.ec" >> .env  
    echo "EMAIL_PASSWORD=mdtnxkpoizqcobrq" >> .env  
    echo "BUCKET_NAME=mapu-bucket" >> .env  
    echo "ACCESS_KEY_ID=AKIATBTTQM3WCDFFIHWH" >> .env  
    echo "SECRET_ACCESS_KEY=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" >> .env  
  
* cd ..
* cp -r api-pis5toF/* api-pis5to
* cp -r api-pis5toF/.* api-pis5to
* cd api-pis5to
* npm i
* cd ..
* docker-compose up --build

