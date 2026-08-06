# IEPI — Instrumentación y Electrosistemas en Procesos Industriales

Sitio web institucional de IEPI con tres secciones independientes, cada una con su propia URL.

## Estructura del proyecto

```
.
├── index.html              # Corporativo IEPI (35 años)
├── consultoria/            # Consultoría de Víctor Vargas
│   ├── index.html
│   └── assets/victor.jpg
├── instrumentos/           # Catálogo de equipos en venta
│   ├── index.html
│   └── assets/             # Manuales PDF + fotos de productos
├── vercel.json             # Config de Vercel
└── README.md
```

## URLs

| URL                                          | Contenido                              |
|----------------------------------------------|----------------------------------------|
| `https://iepi.consulting/`                   | Corporativo IEPI (35 años)             |
| `https://victor.iepi.consulting/`            | Consultoría de Víctor Vargas            |
| `https://iepi.consulting/instrumentos`       | Catálogo de equipos en venta            |

## Despliegue en Vercel

### 1) Importar el repo

1. Ve a [https://vercel.com/new](https://vercel.com/new)
2. Selecciona el repo `abalderasdev/iepi`
3. Framework preset: **Other** (sitio estático)
4. Build command: (vacío)
5. Output directory: `.` (raíz)
6. Click **Deploy**

### 2) Configurar los dominios

En **Project Settings → Domains** agrega:

- `iepi.consulting` → raíz del proyecto
- `victor.iepi.consulting` → apunta a la raíz (mismo proyecto) **o** redirige a `/consultoria`
- `iepi.consulting/instrumentos` → ya queda automático por la estructura de carpetas

### 3) DNS en el proveedor del dominio `consulting`

| Tipo   | Nombre      | Valor                  |
|--------|-------------|------------------------|
| CNAME  | `@`         | `cname.vercel-dns.com.` |
| CNAME  | `victor`    | `cname.vercel-dns.com.` |

Vercel verifica automáticamente y emite el certificado TLS.

## Stack técnico

- HTML5 + CSS3 + JavaScript vanilla
- Sin frameworks, sin tracking, sin build step
- Single-file por sección
- Diseño responsivo (mobile, tablet, desktop)
- **Vercel** para hosting + CDN global + TLS automático

## Mantenimiento

Para actualizar el sitio:

1. Edita localmente el archivo correspondiente
2. `git add . && git commit -m "mensaje" && git push origin main`
3. Vercel redespliega automáticamente en ~30 segundos

---

Hecho con ♥ por **ABDev · Alberto Balderas**.
