# Para Iniciar
Ejecutar cada servicio entrando a la carpeta y ejecutando:
npm install
node index

# Como acceder desde YARC
  1. http://localhost:7070/auth/register
     Content-Type: application/JSON
     Payload: {
              "name": "juan",
              "email": "carlos",
              "password": "234"
              }

     
  3. http://localhost:7070/auth/login
     Content-Type: application/JSON
     Payload: {
              "name": "juan",
              "email": "carlos",
              "password": "234"
              }
     
     (esto retorna un Token, que se copia y se envia en cada operacion contra los servicios)

   4. Crear varios productos:
      http://localhost:8080/product/create
        Content-Type: application/JSON
       Payload: {
                  "name": "rueda",
                  "description":"redonda",
                  "price":234
                 }
       Autorization: Bearer Token
   
   5. Crear orden:
      http://localhost:8080/product/buy
        Content-Type: application/JSON
        Payload: {
                    "ids": [
                              "64d634d1e4be013f04736d66",
                              "64d62b2be4be013f04736d65"
                            ]
}
      Autorization: Bearer Token

### Services:
  1. Auth Service
  2. Product Service
  3. Order Service
  
![ManoSriram - Service jobs](https://ik.imagekit.io/09vbfltqtgx/COM_MICRO-Page-2_qT8AiOXYJ.png)


![ManoSriram - Flow Chart](https://ik.imagekit.io/09vbfltqtgx/COM_MICRO-Page-1_zQq3E_sKrD.png)
