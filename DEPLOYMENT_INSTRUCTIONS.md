# Instrucciones para Configurar GitHub Pages

## ✅ Pasos Completados

1. ✅ Código pusheado al nuevo repositorio: https://github.com/Oppita/Grek
2. ✅ Workflow de GitHub Actions configurado
3. ✅ Configuración de Vite actualizada para `/Grek/`

## 🔧 Configuración Manual Requerida en GitHub

Para que el deployment funcione, necesitas configurar GitHub Pages manualmente:

### Paso 1: Ir a Settings
1. Abre https://github.com/Oppita/Grek/settings/pages
2. O navega: `Settings` → `Pages` (en el menú lateral izquierdo)

### Paso 2: Configurar Source
En la sección **"Build and deployment"**:
- **Source**: Selecciona `GitHub Actions`
- NO selecciones "Deploy from a branch"

### Paso 3: Verificar el Deployment
1. Ve a https://github.com/Oppita/Grek/actions
2. Verifica que el workflow "Deploy to GitHub Pages" se esté ejecutando
3. Si hay errores, revisa los logs

### Paso 4: Acceder a la Aplicación
Una vez que el deployment sea exitoso, tu aplicación estará disponible en:
**https://oppita.github.io/Grek/**

## 🔑 Configurar API Key (IMPORTANTE)

El deployment funcionará, pero para que la aplicación funcione correctamente, necesitas configurar la API key de Gemini:

### Opción 1: GitHub Secrets (Recomendado para producción)
1. Ve a https://github.com/Oppita/Grek/settings/secrets/actions
2. Click en "New repository secret"
3. Nombre: `GEMINI_API_KEY`
4. Valor: Tu API key de Gemini
5. Click "Add secret"

### Opción 2: Variables de entorno en el código
Edita el archivo `.env` localmente y asegúrate de que esté en `.gitignore`

## 📋 Checklist de Verificación

- [ ] GitHub Pages configurado con Source = "GitHub Actions"
- [ ] Workflow ejecutándose sin errores
- [ ] Aplicación accesible en https://oppita.github.io/Grek/
- [ ] API Key configurada
- [ ] Funcionalidad de análisis de proyectos funcionando

## 🐛 Troubleshooting

### Si el workflow falla:
1. Revisa los logs en https://github.com/Oppita/Grek/actions
2. Verifica que GitHub Pages esté habilitado
3. Asegúrate de que los permisos de GitHub Actions estén correctos

### Si la aplicación no carga:
1. Verifica la consola del navegador (F12)
2. Asegúrate de que la ruta base en `vite.config.ts` sea `/Grek/`
3. Verifica que el deployment haya sido exitoso

### Si el análisis de proyectos no funciona:
1. Verifica que la API key esté configurada
2. Revisa la consola del navegador para errores de API
3. Asegúrate de que la API key tenga los permisos correctos
