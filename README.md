# UrbanGrocers API Testing

## Descripción del proyecto

Este proyecto consistió en probar nuevas funcionalidades de la API de **Urban.Grocers**, específicamente enfocadas en:

- La gestión de productos dentro de kits
- El cálculo y disponibilidad del servicio de entrega “Order and Go”

Se diseñó una lista de comprobación que cubre escenarios positivos y negativos para ambas funcionalidades, con el objetivo de validar la lógica del backend. Las pruebas se realizaron utilizando **Postman**, y se reportaron los errores encontrados en **Jira**.

---

## Funcionalidades probadas

### 1. Agregar productos a un kit

- Se utilizó el endpoint `POST /api/v1/kits/{id}/products`
- Se probaron escenarios como:
  - Agregar productos válidos
  - Envío de listas vacías
  - Exceso en el número máximo de productos (más de 30)
  - Combinación de productos repetidos y nuevos

### 2. Servicio de entrega “Order and Go”

- Se utilizó el endpoint `POST /order-and-go/v1/delivery`
- Se validó:
  - Cálculo correcto del precio según el peso del pedido
  - Disponibilidad del servicio según dirección y región
  - Respuestas ante datos inválidos o incompletos

---

## Herramientas utilizadas

- **Postman** – para ejecutar las pruebas de los endpoints
- **Google Sheets** – para diseñar y registrar las listas de comprobación  
- **Jira** – para documentar y reportar errores encontrados

---

## Documentación de las pruebas

Puedes revisar la lista de comprobación y los resultados aquí:

[Lista de comprobación y resultados - UrbanGrocers API](https://docs.google.com/spreadsheets/d/1FxSqRzj-nk54QHwxq6U3AFB3KxkE0BXj/edit?usp=sharing&ouid=113710068924394112718&rtpof=true&sd=true)

---

## Resultados

Se ejecutaron todas las pruebas previstas. Durante el proceso se detectaron fallos como:

- Respuesta de error 400 no especificada correctamente al exceder el límite de productos
- Inconsistencias en la validación de regiones en el servicio de entrega

Los errores encontrados fueron reportados con sus respectivos ID y están documentados en la hoja de cálculo correspondiente.

---

## Conclusiones

El proyecto permitió evaluar la robustez de la lógica del backend de Urban.Grocers en áreas críticas. Aunque se identificaron algunos errores funcionales, la arquitectura general de la API muestra un diseño coherente y modular.

Estas pruebas aportaron evidencia útil sobre la necesidad de mejoras en validaciones y manejo de excepciones, y representaron una buena oportunidad para reforzar habilidades en pruebas de API, documentación técnica y uso de herramientas como Postman y Jira.
