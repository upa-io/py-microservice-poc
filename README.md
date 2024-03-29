
# PY-MICROSERVICE-POC

[![Quality gate](https://sonarcloud.io/api/project_badges/quality_gate?project=upa-io_py-microservice-poc)](https://sonarcloud.io/summary/new_code?id=upa-io_py-microservice-poc)

Proyecto PoC de REST API con FastAPI en Python.

Requisitos:

- Python 3.12
- FastAPI >=0.109.0,<0.110.1

FastAPI se basa en las siguientes librerías:
- Starlette para las partes web.
- Pydantic para las partes de datos.

Instalación

1. Clona el repositorio:

```git clone <https://github.com/upa-io/py-microservice-poc.git>```

2. Instala FastAPI

```pip install fastapi```

3. Ejecución

Para ejecutar el API, utiliza el siguiente comando:

```uvicorn app.main:app --reload```

Luego, accede a http://127.0.0.1:8000/docs para ver la documentación interactiva del API proporcionada por Swagger UI.

Endpoints del API

- GET /: Retorna un mensaje de saludo simple.
- GET /items/{item_id}: Retorna los detalles de un ítem con el ID proporcionado.
- PUT /items/{item_id}: Actualiza los detalles de un ítem con el ID proporcionado.
- DELETE /items/{item_id}: Elimina el ítem con el ID proporcionado.
- PATCH /items/{item_id}: Actualiza parcialmente el ítem con el ID proporcionado.
- OPTIONS /items/: Obtener las opciones del endpoint ítem.
- POST /items/: Creacion de nuevo ítem.

4. Ejecucion de contenedor
Construccion de imagen de docker
```docker build -t myimage .```

Ejecucion de contenedor, con la imagen creada en el paso previa.
```docker run -d --name mycontainer -p 80:80 myimage```

Se seguiran los mismos endpoints que se ha mencionado anteriormente.

Contribuciones

Si deseas contribuir a este proyecto, por favor sigue los siguientes pasos:

1. Haz un fork del repositorio.
2. Crea una rama para tu contribución: git checkout -b mi-nueva-funcionalidad
3. Realiza los cambios y realiza commits: git commit -m "Agregar nueva funcionalidad"
4. Push a tu rama: git push origin mi-nueva-funcionalidad
5. Abre una solicitud de pull (pull request) en GitHub.

Licencia

Este proyecto está licenciado bajo la Licencia GNU - ver el archivo LICENSE para más detalles.
