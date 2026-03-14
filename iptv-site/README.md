# 📡 IPTV Lists

Sitio estático para alojar y compartir listas IPTV, desplegado en Netlify.

## Estructura

```
/
├── index.html              ← Página principal
├── build.js                ← Genera los índices automáticamente
├── netlify.toml            ← Configuración de Netlify
└── listas/
    ├── tv/                 ← Sube aquí tus .m3u de canales en vivo
    ├── series/             ← Sube aquí tus .m3u de series
    └── movies/             ← Sube aquí tus .m3u de películas
```

## Cómo subir archivos

1. Ve a tu repositorio en **GitHub**
2. Navega a la carpeta correspondiente (`listas/tv/`, `listas/series/`, o `listas/movies/`)
3. Haz clic en **"Add file" → "Upload files"**
4. Arrastra tu archivo `.m3u` o `.m3u8`
5. Haz clic en **"Commit changes"**
6. Netlify detecta el cambio, ejecuta `node build.js` y actualiza el sitio automáticamente (~30 segundos)

## Formatos soportados

- `.m3u`
- `.m3u8`
- `.txt`
- `.list`

## Despliegue inicial en Netlify

1. Crea un repositorio en GitHub y sube este proyecto
2. En Netlify: **Add new site → Import an existing project → GitHub**
3. Selecciona el repositorio
4. Netlify detecta automáticamente la configuración de `netlify.toml`
5. Haz clic en **Deploy site**

## URLs del sitio

| Ruta | Contenido |
|------|-----------|
| `/` | Página principal |
| `/listas/` | Índice de categorías |
| `/listas/tv/` | Lista de archivos TV |
| `/listas/series/` | Lista de archivos Series |
| `/listas/movies/` | Lista de archivos Movies |
