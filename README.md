# 📦 Analizador de pedidos CSV

Herramienta web que recibe un CSV de pedidos desordenado, lo **normaliza**, lo **clasifica** y entrega la **acción requerida por pedido**. Funciona 100% en el navegador: no hay backend y los datos nunca salen de tu computador.

🔗 **Demo:** https://karla-developer.github.io/organizador-pedidos/

> Prototipo creado con [Claude](https://claude.ai) como artifact y publicado en GitHub Pages.

---

## ¿Qué problema resuelve?

Quien vende por redes sociales o por encargo suele llevar los pedidos en una planilla con datos inconsistentes: estados escritos de distintas formas, fechas en varios formatos, categorías con errores de tipeo y notas que contradicen el estado del pedido (por ejemplo, "Entregado" con una nota que dice "cliente reporta no haber recibido").

Esta herramienta ordena ese caos y señala qué pedidos necesitan atención primero.

## Funcionalidades

- **Carga flexible:** arrastra el archivo o selecciónalo. Detecta automáticamente el separador (coma, punto y coma o tabulación).
- **Reconocimiento de encabezados:** acepta nombres alternativos de columnas (Pedido / ID / Order, Cliente, Categoría / Rubro, Estado, etc.).
- **Normalización de datos:**
  - Fechas a formato ISO (`AAAA-MM-DD`), marcando las inválidas.
  - Montos y cantidades numéricas.
  - Estados unificados (Completado, Cancelado, Pendiente, Enviado, En proceso).
  - Categorías agrupadas aunque tengan errores de tipeo.
- **Auditoría de notas:** detecta reclamos, errores, incidencias y conflictos entre el estado y lo que dice la nota.
- **Clasificación:** cada pedido queda como *Completo*, *En proceso* o *Por verificar*.
- **Resumen ejecutivo:** totales, alertas y conteo por tipo de incidencia.
- **Vista por categoría** con búsqueda y filtros.
- **Exportación:** copia el CSV limpio para pegarlo en Excel, Google Sheets o un archivo `.csv`.
- **Modo claro / oscuro.**
- Botón **"Probar con datos de ejemplo"** para ver la herramienta sin subir nada.

## Cómo usarla

1. Abre la [demo](https://karla-developer.github.io/organizador-pedidos/).
2. Sube tu CSV (o usa los datos de ejemplo).
3. Revisa el resumen y los pedidos marcados como *Por verificar*.
4. Haz clic en **Copiar CSV limpio** y pégalo donde lo necesites.

### Formato esperado

Una fila de encabezados y una fila por pedido. Ejemplo (ver también `Datos de prueba.csv`):

```csv
ID Pedido,Fecha,Cliente,Producto,Monto USD,Estado,Notas
P01,2024-02-18,Anna C.,Tapete tejido,35,Pagado,Enviar a Bogotá
P02,2024-03-19,Carlos M.,Cerámica roja,45,Pendiente,"Cliente dice que pagó, revisar transferencia"
```

## Ejecutarlo en local

No requiere instalación ni dependencias. Descarga o clona el repositorio y abre `index.html` en tu navegador:

```bash
git clone https://github.com/Karla-developer/organizador-pedidos.git
cd organizador-pedidos
# abre index.html en tu navegador
```

## Estructura del repositorio

```
organizador-pedidos/
├── index.html          # Aplicación completa (HTML, CSS y JavaScript)
├── Datos de prueba.csv # CSV de ejemplo con casos típicos
└── README.md
```

## Tecnologías

- HTML, CSS y JavaScript (vanilla), sin librerías externas
- Prototipado con Claude (Anthropic)
- Publicado con GitHub Pages

## Privacidad

Todo el procesamiento ocurre localmente en tu navegador. El archivo no se sube a ningún servidor.

## Autora

**Karla Miranda Rocuant** · Ingeniera en Informática
[GitHub](https://github.com/Karla-developer) · [LinkedIn](https://www.linkedin.com/in/karla-miranda-rocu%C3%A1nt-956a5a122/)
