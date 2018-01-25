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

4.  Ejecutar: 
	Desde consola `./gradlew check`
	Desde Android Studio `gradlew check`
	En caso negativo se obtendrá `BUILD FAILED`
	En caso positivo se obtendrá `BUILD SUCCESSFUL`
	Se generarán los reportes en `\MiRepositorio\app\build\reports`, donde se visualizarán los errores en caso existan
5. En el archivo `build.gradle` agregar `apply from: '../config/quality/quality.gradle'` para enlazar el archivo gradle que se encuentra en la carpeta <kbd>config</kbd>

6. Ahora, antes de hacer un `commit` se ejecutará el análisis de nuestro código  

7. En caso negativo, solucionar los errores y realizar un commit nuevamente

8. En caso positivo, subir los cambios a tu rama remota (no olvidar eliminar) y realizar un PR

Happy coding.
