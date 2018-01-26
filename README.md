Pre-commit
===================

Este repositorio ayudará a verificar nuestro código antes de pasar a nuestro repositorio Git.

Pasos a seguir
-------------

1. Copiar el archivo <kbd>pre-commit</kbd>
	En \MiRepositorio\.git\hooks 
	**Eliminar** el archivo pre-commit.sample

2.  Copiar la carpeta <kbd>config</kbd> en \MiRepositorio\ 

3.  **Sincronizar** el proyecto
4.  Por primera vez ejecutar desde consola `./gradlew check` o desde Android Studio `gradlew check` para que descarguen todas las dependencias
 	- Si tienen el error `-bash: ./gradlew: Permission denied` ejecutar <kbd>chmod a+x gradlew</kbd> en la consola
6.  Ejecutar: 
	- Desde consola `./gradlew check`
	- Desde Android Studio `gradlew check`
	- En caso negativo se obtendrá `BUILD FAILED`
	- En caso positivo se obtendrá `BUILD SUCCESSFUL`
	- Se generarán los reportes en `\MiRepositorio\app\build\reports`, donde se visualizarán los errores en caso existan
7. En el archivo `build.gradle` agregar `apply from: '../config/quality/quality.gradle'` para enlazar el archivo gradle que se encuentra en la carpeta <kbd>config</kbd>

8. Ahora, antes de hacer un `commit` se ejecutará el análisis de nuestro código  

9. En caso negativo, solucionar los errores y realizar un commit nuevamente

10. En caso positivo, subir los cambios a tu rama remota (no olvidar eliminar) y realizar un PR

Happy coding.
