# Laboratorio - Flujo Git colaborativo
## Author: Laura Paneque Moreno

## Tarea 1 - Fork y configuración inicial

1. En primer lugar realizo un fork del repositorio del instructor en mi cuenta de GitHub.
2. Clono el fork en mi ordenador utilizando el comando

```
git clone https://github.com/lpmoreno/punto-partida-practica-modulo-git.git
```
3. Instalo las dependencias y arranco la app para confirmar que funciona.

```
npm i
nmp run dev
```

4. Añado el repositorio del instructor como remote con el nombre `upstream` con el siguiente comando:

```
git remote add upstream https://github.com/Lemoncode/punto-partida-practica-modulo-git.git
```
 
5. Verifico con `git remote -v` que tengo tanto `origin` (tu fork) como `upstream` (el instructor).
```
git remote -v
```

6. Creo la rama `dev` a partir de main y la subo a mi fork.

```
git switch -c dev
git push -u origin dev
```

Un fork o bifurcación es la creación de una copia independiente a partir de un proyecto de software para desarrollar por caminos separados. Permite modificar el código sin afectar el proyecto original.

Upstream hace referencia al repositorio original desde el que se ha clonado (forked) un proyecto. Nos permite mantener nuestra copia actualizada con los cambios de otros desarrolladores. Además, podemos solicitar la integración de nuestros cambios en el repositorio original.

![Imagen 1. Terminal con `git remote -v` mostrando `origin` y `upstream` ](capturas/Captura1.png)
![Imagen 2. GitHub con la rama `dev` visible en el desplegable de ramas ](capturas/Captura2.png)


## Tarea 2 — Feature branch A: añadir la Opción 5

1. Creo la rama `feature/opcion-5` a partir de `dev`.

En primer lugar nos aseguramos de estar en la rama dev con git branch o git status y creamos la rama:
```
git switch -c feature/opcion-5
```

2. Edito `src/app.tsx` para incluir la tarjeta 5 al array `OPTIONS`:

```tsx
```

3. Además, modifico el campo `description` de la **Opción 3** de su valor actual a:

```tsx
description: "Flujo de trabajo",
```

4. Arrancamos la app y verificamos en el navegador que aparece la Opción 5.
```
npm run dev
```

5. Hacemos un commit con el mensaje: `feat: añadir Opción 5 y actualizar descripción de Opción 3`
```
git add .
git commit -m "feat: añadir Opción 5 y actualizar descripción de Opción 3"
```

6. Sube la rama a tu fork.
```
git push -u origin feature/opcion-5
```

La rama parte de dev porque en este proyecto el desarrollo se está realizando sobre la rama dev. La rama main es la rama estable y los cambios en ella se realizarán de forma muy controlada para evitar pérdidas de datos.

![Imagen 3. La app en el navegador con la Opción 5 recién añadida](capturas/Captura3.png)
