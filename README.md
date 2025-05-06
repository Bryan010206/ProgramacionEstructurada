# ProgramacionEstructurada
PARCIAL APIPOSTMAIL
API REST con Node.js + Express + MongoDB para:

Comprar créditos

Registrar envíos

Eliminar envíos (con reembolso de créditos)

Consultar envíos, créditos y productos disponibles

💠 Recursos usados
Node.js

Express

MongoDB + Mongoose

🥪 Endpoints disponibles
Usuarios

GET /usuario/:id/credito → Muestra créditos de un usuario

POST /usuario/:id/comprar-creditos → Compra créditos (paquetes: 30, 40, 60)

Cuerpo JSON:

json
{ "paquete": "30" }
Envíos

POST /envios → Registrar nuevo envío Cuerpo JSON:

json
{
  "usuarioId": "USR001",
  "producto": "ID_DEL_PRODUCTO"
}
GET /envios/:usuarioId → Muestra envíos de un usuario

DELETE /envios/:envioId → Elimina un envío y reembolsa créditos según peso

Productos

GET /productos → Lista de productos disponibles

POST /productos → (Si está habilitado) Crea un producto

Ejemplo JSON:

json
{
  "nombre": "iphone",
  "descripcion": "iphone SE 2020",
  "peso": 4
}
🎯 Lógica de créditos
Si el peso del producto es ≤ 3kg → cuesta 1 crédito

Si es > 3kg → cuesta Math.ceil(peso / 3) créditos

Al eliminar un envío, se reembolsan créditos

Estructura del proyecto
postmail-api
├── models/       # Esquemas de usuario, producto y envío
├── services/     # Lógica de envío y conexión DB
├── routes/       # Rutas de la API
├── .env          # Variables de entorno
├── index.js      # Punto de entrada
└── package.json  # Configuración del proyecto


y eso es todo
