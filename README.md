# iepi.consulting

Sitio principal de **IEPI Consultoría · Víctor Vargas Carrillo**.
Desplegado en **Vercel** bajo el dominio personalizado **iepi.consulting**.

---

## Estructura

```
.
├── index.html              # Página principal: Víctor Vargas Carrillo (consultoría)
├── assets/
│   └── victor.jpg          # Foto del consultor
├── equipo/
│   ├── index.html          # Catálogo de equipo IEPI en venta (Fluke + Additel)
│   └── assets/             # Imágenes y manuales PDF del equipo
├── vercel.json             # Config de Vercel (cleanUrls, headers, cache)
└── .gitignore
```

## URLs

- **Principal**: https://iepi.consulting/ → consultoría de Víctor
- **Catálogo**: https://iepi.consulting/equipo → equipo de calibración en venta

## Despliegue en Vercel

### 1) Importar el repo
1. Ve a https://vercel.com/new
2. Selecciona el repo `abalderasdev/iepi`
3. Framework preset: **Other** (sitio estático)
4. Build command: (vacío)
5. Output directory: `.` (raíz)
6. Click **Deploy**

### 2) Asignar el dominio personalizado `iepi.consulting`
1. Project Settings → Domains
2. Escribe `iepi.consulting` → Add
3. Vercel te muestra los registros DNS a configurar

### 3) DNS en el proveedor del dominio
Donde compraste `consulting` (Namecheap, GoDaddy, Google Domains, etc.):

| Tipo | Nombre | Valor |
|---|---|---|
| CNAME | `www` | `cname.vercel-dns.com.` |
| A | `@` | `76.76.21.21` |

(También `A` secundario: `66.225.18.42` si tu proveedor pide dos registros A)

Vercel verifica automáticamente y emite el certificado TLS.

## Verificación

- [ ] `https://iepi.consulting/` carga con candado verde
- [ ] La foto de Víctor aparece en "Sobre mí"
- [ ] El WhatsApp flotante abre chat con número correcto
- [ ] `https://iepi.consulting/equipo` carga el catálogo de instrumentos
- [ ] Las imágenes del equipo se ven correctamente

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
