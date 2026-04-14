# Laboratorio - Flujo Git colaborativo
# Author: Laura Paneque Moreno

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