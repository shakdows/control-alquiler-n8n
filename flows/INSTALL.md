# Instalación — Control de Alquiler con n8n

Guía paso a paso para instalar y configurar el sistema.

---

## 1. Importar flujos en n8n

### Flujo 1 — Admin API
1. En n8n → **Import**
2. Seleccionar `flows/flujo-1-admin.json`
3. Guardar

### Flujo 2 — Cron automático
1. En n8n → **Import**
2. Seleccionar `flows/flujo-2-cron.json`
3. Guardar

---

## 2. Configurar Google Sheets

Crear un Google Sheet con **exactamente** estas hojas:

### Hoja: `inquilinos`

### Hoja: `cargos`

### Hoja: `pagos`

---

## 3. Conectar Google Sheets en n8n

En cada nodo de Google Sheets:
1. Seleccionar credencial Google
2. Documento → **From list**
3. Elegir el archivo correcto
4. Hoja → elegir la hoja correspondiente

---

## 4. Activar flujos

- Activar **Flujo 1** (API)
- Activar **Flujo 2** (Cron)

---

## 5. Probar API (Flujo 1)

Endpoint:

Ejemplo:
```json
{
  "action": "cargos.list"
}

---

### 3️⃣ Guardar
- Clic **Commit changes**

---

## SIGUIENTE PASO
Después de esto pasamos al **PASO 3: Versionado + Changelog**.

Cuando termines dime:
> **INSTALL listo**
