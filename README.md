# hola-mundo

Este es mi primer repositorio en GitHub.  
Estoy practicando comandos de Git y GitHub usando Git Bash.

---

## 🧰 Comandos utilizados paso a paso

| Paso | Comando | Descripción |
|------|---------|-------------|
| 1️⃣ | `mkdir practica-github` | Crear una carpeta nueva para trabajar |
| 2️⃣ | `cd practica-github` | Entrar a la carpeta creada |
| 3️⃣ | `git clone https://github.com/GustavoRodriguez79/hola-mundo.git` | Clonar el repositorio desde GitHub |
| 4️⃣ | `cd hola-mundo` | Entrar a la carpeta del repositorio clonado |
| 5️⃣ | `echo "# hola-mundo" > README.md` | Crear el archivo README.md con título inicial |
| 6️⃣ | `notepad README.md` | Abrir el archivo en el bloc de notas para editarlo (opcional) |
| 7️⃣ | `git status` | Verificar los archivos modificados o nuevos |
| 8️⃣ | `git add README.md` | Agregar el archivo al área de preparación (staging) |
| 9️⃣ | `git commit -m "Agrego README.md inicial"` | Crear un commit con mensaje descriptivo |
| 🔟 | `git push origin main` | Subir los cambios al repositorio en GitHub |

---

## 🧹 ¿Qué hace la opción "Automatically delete head branches"?

Cuando activás **“Automatically delete head branches”**, GitHub borra automáticamente la rama que fue usada en un **pull request (PR)** una vez que:

✅ El pull request fue **completado** (mergeado) a la rama principal (por ejemplo, `main`).  
🚫 Solo borra ramas que ya no se necesitan.  
📦 El contenido de la rama **no se pierde**, porque ya fue fusionado.

---

### 📦 ¿Por qué conviene activarla?

- Mantiene tu repositorio **limpio**.
- Elimina ramas que ya no se usan y **evita confusiones**.
- Mejora la organización cuando trabajás con **muchas ramas** (por ejemplo, en proyectos colaborativos).

---

### 🔁 ¿Se puede recuperar una rama borrada?

✅ **Sí.** GitHub permite restaurarla desde la interfaz web si la necesitás más tarde.  
En el historial del pull request hay un botón que dice **“Restore branch”**.

---

### 🧠 En resumen

| Opción      | Resultado |
|-------------|-----------|
| ✅ Activada  | GitHub borra automáticamente la rama del PR después de hacer merge. |
| ❌ Desactivada | Tenés que borrar manualmente las ramas después del merge. |

---

# 📘 Guía para trabajar con ramas creadas desde GitHub en Git Bash

Este documento explica cómo sincronizar una rama que fue creada directamente en GitHub y cómo trabajar con ella localmente desde Git Bash.

---

## 🌿 ¿Qué es una rama?

Una rama (branch) es una línea de trabajo paralela dentro de tu proyecto. Permite desarrollar nuevas funcionalidades o hacer pruebas sin afectar el código principal (`main`).

---

## 🛠️ Procedimiento completo

### 1️⃣ Crear la rama en GitHub (por la web)

- Ingresá a tu repositorio en GitHub.
- Hacé clic en el menú desplegable de ramas (donde dice `main`) y escribí el nombre de la nueva rama (por ejemplo: `SPD`).
- Presioná Enter para crearla.

> 📌 Esto solo crea la rama en GitHub (repositorio remoto), **no está disponible localmente aún**.

---

### 2️⃣ Abrir Git Bash en tu repositorio local

Asegurate de estar en la carpeta correcta, por ejemplo:
```bash
cd ~/practica-github/hola-mundo
```
### 3️⃣ 🧠 Resumen de comandos

| Comando                            | Descripción                                                |
|-----------------------------------|------------------------------------------------------------|
| `git fetch origin`                | Trae las ramas del repositorio remoto                     |
| `git branch -a`                   | Lista ramas locales y remotas                             |
| `git checkout -b SPD origin/SPD`  | Crea una nueva rama local basada en la remota SPD         |
| `git branch`                      | Muestra en qué rama estás                                 |
| `git add README.md`               | Agrega el archivo al área de staging                      |
| `git commit -m "mensaje"`         | Crea un commit con un mensaje personalizado               |
| `git push origin SPD`             | Sube los cambios a la rama remota SPD                     |
---

## ✅ Pasos para traer los cambios de main a SPD:

| Comando                            | Descripción                                                |
|-----------------------------------|------------------------------------------------------------|
| `git checkout SPD`                | Asegurate de estar en la rama SPD                     |
| `git merge main`                   | Esto va a fusionar los cambios de la rama main en tu rama SPD |
| `git add README.md` | Agregar el archivo al área de preparación (staging) |
|`git commit -m`|Crea un commit con un mensaje personalizado | 
|`git push origin SPD`|Subís los cambios a GitHub|
---
