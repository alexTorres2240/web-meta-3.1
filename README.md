# Meta 3.1 - API REST con Express - Gestión de Tareas (MVC)

El presente proyecto presenta una API REST de gestión de tareas que cuenta con un CRUD completo para guardar las tareas en memoria y gestionarlas mediante funciones básicas: listar, buscar, crear, actualizar y eliminar.

## Instrucciones de instalación y ejecución

Para instalar el proyecto, primero hay que obtener el mismo directamente del respositorio en github.

```Shell
git clone https://github.com/alexTorres2240/web-meta-3.1.git
```

Después, hay que instalar las dependencias del proyecto.

```Shell
npm install
```

Finalmente, se inicia el servidor.

```Shell
npm run dev
npm start
```

## Métodos y Endpoints disponibles

En la siguiente tabla se presentan los endpoints disponibles para cada método junto a una breve descripción.

| Método | Endpoint                   | Descripción                        |
| ------- | -------------------------- | ----------------------------------- |
| GET     | /                          | Mensaje de bienvenida.              |
| GET     | /api/tareas                | Obtiene todas las tareas.           |
| GET     | /api/tareas/buscar?q=texto | Busca tareas por título.           |
| GET     | /api/tareas/:id            | Obtiene una tarea por ID.           |
| POST    | /api/tareas                | Crea una nueva tarea.               |
| PUT     | /api/tareas/:id            | Reemplaza una tarea completa.       |
| PATCH   | /api/tareas/:id            | Actualiza solo los campos enviados. |
| DELETE  | /api/tareas/:id            | Elimina una tarea.                  |

## Capturas de pantalla

A continuación se muestran capturas de pantalla de los resultados para cada petición en test-collection.http.

```HTTP
GET {{host}}/
```

![1791692387991](image/README/1791692387991.png)

```HTTP
GET {{host}}/api/tareas?formato=text
```

![1791692397143](image/README/1791692397143.png)

```HTTP
GET {{host}}/api/tareas
```

![1791692404072](image/README/1791692404072.png)

```HTTP
GET {{host}}/api/tareas/1
```

![1791692461897](image/README/1791692461897.png)

```HTTP
POST {{host}}/api/tareas

Content-Type: application/json

{
    "titulo": "Nueva tarea",
    "completada": false
}
```

![1791692470826](image/README/1791692470826.png)

```HTTP
PUT {{host}}/api/tareas/1

Content-Type: application/json

{
    "titulo": "Tarea actualizada",
    "completada": true
}
```

![1791692484131](image/README/1791692484131.png)

```HTTP
PATCH {{host}}/api/tareas/1

Content-Type: application/json

{
    "completada": false
}
```

![1791692686220](image/README/1791692686220.png)

```HTTP
GET {{host}}/api/tareas/buscar?q=express
```

![1791692692664](image/README/1791692692664.png)

```HTTP
GET {{host}}/api/tareas/buscar?q=EXPRESS
```

![1791692698523](image/README/1791692698523.png)

```HTTP
GET {{host}}/api/tareas/buscar
```

![1791692703831](image/README/1791692703831.png)

```HTTP
DELETE {{host}}/api/tareas/3
```

![1791692709231](image/README/1791692709231.png)
