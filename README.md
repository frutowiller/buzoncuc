# 📬 Buzón CUC Escucha

Micrositio de sugerencias estudiantiles para la Corporación Universidad de la Costa — Facultad de Ingeniería.

---

## 🗂️ Descripción del proyecto

Plataforma web donde cualquier estudiante puede dejar una sugerencia de forma sencilla sobre bienestar, servicios, clases, inclusión y más.

**Campos del formulario:**
- Nombre completo
- Correo institucional
- Programa académico
- Mensaje / Sugerencia

---

## 📋 Flujo de trabajo con Git y GitHub

### Paso 1 — Inicializar Git en el directorio de trabajo

```bash
cd mi-app
git init
```

### Paso 2 — Configurar usuario e email (repositorio local)

```bash
git config user.name  "Tu Nombre"
git config user.email "usuario@cuc.edu.co"
```

Para verificar la configuración:
```bash
git config --list
```

### Paso 3 — Configurar el repositorio local (primer commit)

```bash
git add .
git commit -m "feat: estructura inicial del micrositio Buzón CUC Escucha"
```

### Paso 4 — Configurar el repositorio remoto en GitHub

```bash
git remote add origin https://github.com/<usuario>/buzon-cuc-escucha.git
git branch -M main
git push -u origin main
```

---

### Paso 5 — Rama 1: cambio de color de fondo

```bash
# Crear y moverse a la nueva rama
git checkout -b rama-estilo

# Editar index.html → cambiar la variable --bg en :root
# De: --bg: #F0F4FF;
# A:  --bg: #E8F5E9;   (o el color elegido)

git add index.html
git commit -m "style: cambio de color de fondo a verde claro (rama-estilo)"

# Fusionar con main
git checkout main
git merge rama-estilo
git push origin main
```

---

### Paso 6 — Rama 2: nuevo campo en el formulario + Pull Request

```bash
# Crear segunda rama desde main actualizado
git checkout -b rama-formulario

# Editar index.html → agregar campo "Semestre actual"
# (ver cambio en el formulario)

git add index.html
git commit -m "feat: agrega campo Semestre actual al formulario (rama-formulario)"

# Subir la rama al repositorio remoto
git push origin rama-formulario

# Crear el Pull Request en GitHub:
# GitHub → Pull requests → New pull request
# base: main  ←  compare: rama-formulario
```

---

### Paso 7 — Verificar historial de commits

```bash
git log --oneline --graph --all
```

Salida esperada:
```
* abc1234 (HEAD -> main, origin/main) Merge branch 'rama-estilo'
* def5678 style: cambio de color de fondo a verde claro (rama-estilo)
* ghi9012 feat: estructura inicial del micrositio Buzón CUC Escucha
```

---

### Paso 8 — URLs del proyecto

| Recurso | URL |
|---------|-----|
| Repositorio GitHub | `https://github.com/<usuario>/buzon-cuc-escucha` |
| Sitio en Netlify | `https://<sitio>.netlify.app` |

---

## 🚀 Despliegue en Netlify

1. Inicia sesión en [netlify.com](https://www.netlify.com)
2. **Add new site → Import an existing project**
3. Selecciona **GitHub** y elige el repositorio `buzon-cuc-escucha`
4. Configuración de build:
   - **Branch to deploy:** `main`
   - **Build command:** *(dejar vacío)*
   - **Publish directory:** `.` (raíz del proyecto)
5. Haz clic en **Deploy site**
6. Netlify asignará automáticamente una URL pública

---

## 🛠️ Tecnologías usadas

- HTML5 semántico
- CSS3 (variables CSS, Flexbox, Grid, gradientes)
- JavaScript vanilla (ES6+)
- Google Fonts — Inter
- Git + GitHub
- Netlify (despliegue continuo)

---

## 🎓 Información académica

**Asignatura:** Buenas Prácticas de Desarrollo de Software  
**Unidad:** No. 1 — Control de versiones y despliegue continuo  
**Institución:** Corporación Universidad de la Costa — CUC  
**Facultad:** Ingeniería  
