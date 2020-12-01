## Autenticación

`POST /o/token/`

> Ejemplo de petición

> Reemplaza `USERNAME` y `PASSWORD` con tus credenciales de Admetricks.

```shell
curl -X 'POST' 'https://clientela.admetricks.com/o/token/?client_id=IW8M80h7qgCaSz4hPm3gr3wJP89NiJTPyhkwPurT&client_secret=KnBW84uyHlxwlNrKOXyym6Ro1IT6IlYdhScdop63hHddCzJIxUwDG7VItNgEONb1U2ebEH6fBmkYgX9LrZD4uqFJlYscHYn9MLxOm2qVccNE2WGEuePpKA7t3jQ2CvMu&grant_type=password&username=USERNAME&password=PASSWORD'
```

```javascript
const credentials = {
  username: "USERNAME",
  password: "PASSWORD"
}

const client = {
  id: "IW8M80h7qgCaSz4hPm3gr3wJP89NiJTPyhkwPurT",
  secret: "KnBW84uyHlxwlNrKOXyym6Ro1IT6IlYdhScdop63hHddCzJIxUwDG7VItNgEONb1U2ebEH6fBmkYgX9LrZD4uqFJlYscHYn9MLxOm2qVccNE2WGEuePpKA7t3jQ2CvMu"
}

const endpoint = `https://clientela.admetricks.com/o/token/?username=${credentials.username}&password=${credentials.password}&client_id=${client.id}&client_secret=${client.secret}&grant_type=password`

fetch(endpoint, {
  body: null,
  method: "POST",
})
  .then(response => response.json())
  .then(token => console.log(token)) // print your token data
```

```python
import requests

url = 'https://clientela.admetricks.com/o/token/?username=USERNAME&password=PASSWORD&client_id=IW8M80h7qgCaSz4hPm3gr3wJP89NiJTPyhkwPurT&client_secret=KnBW84uyHlxwlNrKOXyym6Ro1IT6IlYdhScdop63hHddCzJIxUwDG7VItNgEONb1U2ebEH6fBmkYgX9LrZD4uqFJlYscHYn9MLxOm2qVccNE2WGEuePpKA7t3jQ2CvMu&grant_type=password'
response = requests.post(url)

# print your token data
print(response)
```

> Ejemplo de respuesta (200 OK)

```json
{
  "access_token": "YOUR_TOKEN",
  "expires_in": 36000,
  "token_type": "Bearer",
  "scope": "read write",
  "refresh_token": "REFRESH_TOKEN"
}
```

El API de Clientela utiliza tokens para autentificar las solicitudes.

Tu token tiene muchos privilegios,  **¡asegúrate de mantenerlo seguro!** No lo compartas ni lo expongas en áreas de acceso público como GitHub o código de *front-end*.

**Este *endpoint* acepta los siguientes parámetros:**

| Parámetro       | Descripción                                                               | En             |
| ----------------| --------------------------------------------------------------------------|----------------|
| `username`      | Tu nombre de usuario en Admetricks                                        | Query string   |
| `password`      | Tu contraseña en Admetricks                                               | Query string   |
| `client_id`     | key específico de Clientela. Este valor siempre es el mismo para todos    | Query string   |
| `client_secret` | secret específico de Clientela. Este valor siempre es el mismo para todos | Query string   |
| `grant_type`    | El valor siempre es "password"                                            | Query string   |


Los valores para la identificación del cliente y el secreto del cliente son:

- **client_id:** `IW8M80h7qgCaSz4hPm3gr3wJP89NiJTPyhkwPurT`
- **client_secret:** `KnBW84uyHlxwlNrKOXyym6Ro1IT6IlYdhScdop63hHddCzJIxUwDG7VItNgEONb1U2ebEH6fBmkYgX9LrZD4uqFJlYscHYn9MLxOm2qVccNE2WGEuePpKA7t3jQ2CvMu`


El *endpoint* de autenticación entrega las siguientes respuestas:

Estado        | Descripción
------------- | -------
200           | OK
401           | Credenciales inválidas
404           | Servicio no disponible
405           | Método inválido (ejemplo: `GET` en vez de `POST`)

Recuerda que tu usuario **debe estar habilitado** para el uso de la API. Si tu usuario aún no está habilitado, ponte en contacto con nuestro equipo de Customer Success.