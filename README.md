# ProgramacionEstructurada
# 📦 FASTDROP API

## 📌 Descripción  
FASTDROP API es un sistema que permite gestionar envíos, manejar créditos de usuarios y registrar productos asociados a esos envíos. Los usuarios pueden recargar créditos para realizar envíos y revisar su saldo disponible en cualquier momento.

## 🚀 Instalación y ejecución

1. **Clonar el repositorio**  
```bash
git clone https://github.com/Bryan010206/ProgramacionEstructurada.git
cd fastdrop-api
```

2. **Instalar dependencias**  
```bash
npm install
```

3. **Conectar con MongoDB**  
Debe estar activo en `localhost:27017`. Usa colecciones `usuarios` y `envios`.

4. **Iniciar el servidor**  
```bash
node server.js
```

## 📡 Endpoints de la API

### `GET /api/usuario/:id/credito`  
Consulta créditos disponibles.

### `POST /api/usuario/:id/comprar-creditos`  
Compra créditos.

### `POST /api/envios`  
Registra un envío.  
Ejemplo: Carlos Méndez, Col. Los Pinos, caja de herramientas.

### `GET /api/envios/:usuarioId`  
Consulta envíos del usuario.

### `DELETE /api/envios/:envioId`  
Elimina un envío y reembolsa créditos.

## ✅ Notas finales
- Créditos = saldo de envíos.
- Se descuentan automáticamente.
- Registro, consulta y eliminación fáciles.
