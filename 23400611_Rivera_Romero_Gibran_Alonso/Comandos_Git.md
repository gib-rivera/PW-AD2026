## 1. `git init`

**Descripción:**
Inicializa un nuevo repositorio de Git dentro de un directorio. Al ejecutarlo, Git crea la estructura necesaria para comenzar a controlar las versiones del proyecto.

**Ejemplo de caso de uso:**

```bash
mkdir proyecto
cd proyecto
git init
```

Se utiliza cuando se tiene un proyecto local que todavía no cuenta con un repositorio Git.

---

## 2. `git clone`

**Descripción:**
Crea una copia local de un repositorio remoto, incluyendo sus archivos, ramas e historial de cambios.

**Ejemplo de caso de uso:**

```bash
git clone https://github.com/usuario/proyecto.git
```

Se utiliza cuando se desea descargar un proyecto existente desde GitHub para trabajar con él localmente.

---

## 3. `git status`

**Descripción:**
Muestra el estado actual del repositorio, incluyendo archivos modificados, archivos preparados para commit y archivos que todavía no están siendo rastreados.

**Ejemplo de caso de uso:**

```bash
git status
```

Se puede utilizar antes de realizar un commit para comprobar qué archivos han cambiado.

---

## 4. `git add`

**Descripción:**
Agrega cambios al área de preparación (*staging area*) para que puedan incluirse posteriormente en un commit.

**Ejemplo de caso de uso:**

```bash
git add index.html
```

También se pueden agregar todos los archivos modificados:

```bash
git add .
```

Se utiliza después de modificar archivos y antes de ejecutar `git commit`.

---

## 5. `git commit`

**Descripción:**
Guarda los cambios que se encuentran en el área de preparación como una nueva versión dentro del historial del repositorio.

**Ejemplo de caso de uso:**

```bash
git commit -m "Agrega página principal"
```

Se utiliza cuando se ha terminado una modificación y se desea registrarla en el historial.

---

## 6. `git log`

**Descripción:**
Muestra el historial de commits realizados en el repositorio.

**Ejemplo de caso de uso:**

```bash
git log
```

Una versión más resumida puede utilizarse para consultar rápidamente el historial:

```bash
git log --oneline
```

Se utiliza para conocer qué cambios se han realizado anteriormente y quién los realizó.

---

## 7. `git diff`

**Descripción:**
Muestra las diferencias entre las versiones de los archivos o entre diferentes estados del repositorio.

**Ejemplo de caso de uso:**

```bash
git diff
```

Se puede utilizar para revisar exactamente qué líneas fueron modificadas antes de realizar un commit.

---

## 8. `git branch`

**Descripción:**
Permite listar, crear o eliminar ramas (*branches*) dentro del repositorio.

**Ejemplo de caso de uso:**

```bash
git branch nueva-funcion
```

Esto crea una rama llamada `nueva-funcion`.

Para consultar las ramas existentes:

```bash
git branch
```

Se utiliza para trabajar en diferentes características del proyecto sin modificar directamente la rama principal.

---

## 9. `git switch`

**Descripción:**
Permite cambiar de una rama a otra. También puede utilizarse para crear una nueva rama y cambiarse a ella.

**Ejemplo de caso de uso:**

```bash
git switch nueva-funcion
```

Para crear y cambiar a una rama nueva:

```bash
git switch -c nueva-funcion
```

Se utiliza cuando se desea comenzar a trabajar en una característica independiente del proyecto.

---

## 10. `git merge`

**Descripción:**
Combina los cambios de una rama con otra rama.

**Ejemplo de caso de uso:**

```bash
git switch main
git merge nueva-funcion
```

Se utiliza cuando una característica desarrollada en otra rama ya está terminada y se desea integrarla a `main`.

---

## 11. `git remote`

**Descripción:**
Permite administrar las conexiones entre el repositorio local y los repositorios remotos.

**Ejemplo de caso de uso:**

```bash
git remote -v
```

Muestra las direcciones de los repositorios remotos configurados.

Para agregar un repositorio remoto:

```bash
git remote add origin https://github.com/usuario/proyecto.git
```

Se utiliza para conectar un proyecto local con un repositorio alojado en GitHub u otro servicio.

---

## 12. `git push`

**Descripción:**
Envía los commits realizados en el repositorio local hacia un repositorio remoto.

**Ejemplo de caso de uso:**

```bash
git push origin main
```

Se utiliza para publicar en GitHub los cambios que ya fueron registrados mediante commits.

---

## 13. `git pull`

**Descripción:**
Obtiene los cambios realizados en un repositorio remoto y los integra en la rama local actual.

**Ejemplo de caso de uso:**

```bash
git pull origin main
```

Se utiliza antes de comenzar a trabajar cuando otros integrantes del equipo pueden haber realizado cambios en el repositorio remoto.

---

## 14. `git fetch`

**Descripción:**
Descarga información y cambios del repositorio remoto, pero no los integra automáticamente en la rama local actual.

**Ejemplo de caso de uso:**

```bash
git fetch origin
```

Se utiliza cuando se desea conocer los cambios disponibles en el repositorio remoto antes de decidir si se quieren integrar.

---

## 15. `git restore`

**Descripción:**
Permite restaurar archivos del directorio de trabajo a una versión anterior o retirar cambios del área de preparación.

**Ejemplo de caso de uso:**

```bash
git restore archivo.txt
```

Se utiliza cuando se realizaron modificaciones en un archivo, pero se desea descartar esos cambios locales. Git diferencia `restore` de `reset` y `revert`, ya que `restore` está orientado principalmente a restaurar archivos.

---

## 16. `git reset`

**Descripción:**
Permite mover `HEAD` y modificar el estado de la rama y/o del área de preparación. Puede utilizarse para deshacer commits o retirar archivos del área de preparación.

**Ejemplo de caso de uso:**

```bash
git reset HEAD archivo.txt
```

Se utiliza, por ejemplo, cuando se agregó accidentalmente un archivo con `git add` y se desea quitarlo del área de preparación.

---

## 17. `git revert`

**Descripción:**
Crea un nuevo commit que revierte los cambios introducidos por un commit anterior.

**Ejemplo de caso de uso:**

```bash
git revert abc1234
```

Se utiliza cuando se necesita deshacer un cambio ya registrado sin eliminar el commit original del historial.

---

## 18. `git stash`

**Descripción:**
Guarda temporalmente los cambios que todavía no se han confirmado mediante un commit, permitiendo trabajar con un directorio limpio.

**Ejemplo de caso de uso:**

```bash
git stash
```

Posteriormente, los cambios pueden recuperarse con:

```bash
git stash pop
```

Se utiliza cuando se está trabajando en una característica, pero se necesita cambiar temporalmente de rama sin realizar un commit incompleto.

---

## 19. `git tag`

**Descripción:**
Permite crear, consultar o eliminar etiquetas que identifican puntos específicos del historial del proyecto.

**Ejemplo de caso de uso:**

```bash
git tag v1.0.0
```

Se utiliza para marcar una versión importante del proyecto, por ejemplo, la versión `1.0.0`.

---

## 20. `git config`

**Descripción:**
Permite consultar y modificar las opciones de configuración de Git, como el nombre y correo electrónico utilizados en los commits.

**Ejemplo de caso de uso:**

```bash
git config --global user.name "Nombre del Usuario"
git config --global user.email "usuario@example.com"
```

Se utiliza normalmente al configurar Git por primera vez en una computadora.
