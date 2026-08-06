# victor.iepi.consulting

Sitio de **VVC Consultoría · Víctor Vargas Carrillo**.
Desplegado en **Vercel** bajo el subdominio **`victor.iepi.consulting`**.

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

- **Principal**: https://victor.iepi.consulting/ → consultoría de Víctor
- **Catálogo**: https://victor.iepi.consulting/equipo → equipo de calibración en venta

## Despliegue en Vercel

### 1) Importar el repo
1. Ve a https://vercel.com/new
2. Selecciona el repo `abalderasdev/iepi`
3. Framework preset: **Other** (sitio estático)
4. Build command: (vacío)
5. Output directory: `.` (raíz)
6. Click **Deploy**

### 2) Asignar el subdominio `victor.iepi.consulting`
1. Project Settings → Domains
2. Escribe `victor.iepi.consulting` → Add
3. Vercel te muestra el CNAME a configurar (típicamente `cname.vercel-dns.com`)

### 3) DNS en el proveedor del dominio `consulting`

| Tipo | Nombre | Valor |
|---|---|---|
| CNAME | `victor` | `cname.vercel-dns.com.` |

(Si Vercel te asigna un valor distinto, usa ese.)

Vercel verifica automáticamente y emite el certificado TLS para `victor.iepi.consulting`.

## Verificación

- [ ] `https://victor.iepi.consulting/` carga con candado verde
- [ ] La foto de Víctor aparece en "Sobre mí"
- [ ] El WhatsApp flotante abre chat con número correcto
- [ ] `https://victor.iepi.consulting/equipo` carga el catálogo de instrumentos
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
