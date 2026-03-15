# Microservicios - Calendario Laboral Colombia

## Punto 1 — API Festivos

**Tecnologías:** Node.js · Express · MongoDB

**Puerto:** `8080`

**Cómo ejecutar:**
```bash
cd festivos-api
npm install
mongosh < BDFestivos.mjs
npm start
```

**Endpoints:**
```
GET /api/festivos/verificar/:anio/:mes/:dia
GET /api/festivos/obtener/:anio
```

---

## Punto 2 — API Calendario

**Tecnologías:** Java · Spring Boot · PostgreSQL

**Puerto:** `8081`

**Cómo ejecutar:**
1. Crear la base de datos `CalendarioLaboral` en PostgreSQL
2. Ejecutar el DDL para crear las tablas `Tipo` y `Calendario`
3. Insertar los tipos en PostgreSQL
4. Configurar usuario y contraseña en `application.properties`
5. Tener el Punto 1 corriendo antes de ejecutar este
```bash
cd calendario
mvn spring-boot:run
```

**Endpoints:**
```
GET /api/festivos/obtener/:anio
GET /api/calendario/generar/:anio
GET /api/calendario/listar/:anio
```
