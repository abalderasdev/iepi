# iepi.consulting

Sitio principal de **IEPI Consultoría · Víctor Vargas Carrillo**.
Desplegado en GitHub Pages bajo el dominio personalizado **iepi.consulting**.

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
├── CNAME                   # Dominio personalizado (iepi.consulting)
└── .gitignore
```

## URLs

- **Principal**: https://iepi.consulting/ → consultoría de Víctor
- **Catálogo**: https://iepi.consulting/equipo/ → equipo de calibración en venta

## Despliegue

El sitio se sirve automáticamente desde la rama `main` mediante GitHub Pages.
El dominio personalizado está configurado en el archivo `CNAME`.

### Configuración DNS necesaria (en el proveedor de `consulting`)

Si aún no la tienes, crea:

| Tipo | Nombre | Valor |
|---|---|---|
| CNAME | `@` | `abalderasdev.github.io` |
| CNAME | `www` | `abalderasdev.github.io` |

(O registros A si prefieres apex):
- `185.199.108.153`
- `185.199.109.153`
- `185.199.110.153`
- `185.199.111.153`

Una vez propagado, en GitHub → Settings → Pages → Custom domain verás el check
verde "DNS check in progress" pasar a "HTTPS supported".

## Stack técnico

- HTML5 + CSS3 + JavaScript vanilla
- Sin frameworks, sin tracking, sin build step
- Single-file por sección
- Diseño responsivo (mobile, tablet, desktop)

## Mantenimiento

Para actualizar:
1. Edita el archivo correspondiente localmente
2. `git add . && git commit -m "mensaje" && git push`
3. GitHub Pages redespliega en ~30 segundos

Para secciones del sitio principal, edita `/index.html`.
Para el catálogo de equipo, edita `/equipo/index.html` (las imágenes viven en `/equipo/assets/`).

---

Hecho con ♥ por **ABDev · Alberto Balderas**.
