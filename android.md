# android
- [android](#android)
  - [caracetrísticas](#caracetrísticas)
  - [Android Studio vs. IntelliJ IDEA](#android-studio-vs-intellij-idea)
  - [crear proyecto](#crear-proyecto)
  - [descarga](#descarga)
  - [Ejemplo](#ejemplo)


Android Studio es el entorno de desarrollo integrado oficial para crear aplicaciones Android . Reúne todas las herramientas que un desarrollador de apps necesita en un solo lugar. Android Studio está basado en el potente software IntelliJ IDEA de JetBrains, pero ha sido modificado y mejorado por Google específicamente para el desarrollo de Android . Fue anunciado en 2013 y lanzado oficialmente en 2014, reemplazando a Eclipse como el IDE oficial para este propósito

## caracetrísticas

* Editor Inteligente: Soporta de forma nativa Kotlin, Java y C++ . Ofrece autocompletado de código, detección de errores en tiempo real y refactorización (renombrar variables, mover métodos, etc.) de forma segura y automática.

* Sistema de Compilación Flexible (Gradle): El corazón de la construcción de proyectos. Gradle te permite crear diferentes "variantes" de tu app desde un solo proyecto, por ejemplo, una versión gratuita con anuncios y una versión de pago sin ellos, personalizando cada aspecto del proceso de compilación . Los archivos de configuración se llaman build.gradle.kts (usando Kotlin, que es el recomendado) o build.gradle (con Groovy) .

* Emulador Rápido y Potente: Olvídate de necesitar un teléfono físico para cada prueba. El emulador de Android Studio te permite crear dispositivos virtuales de prácticamente cualquier modelo, tamaño de pantalla y versión de Android (teléfonos, tablets, relojes, TVs) para probar tus apps directamente en tu computadora .

* Diseño de Interfaces (Jetpack Compose): Para crear las pantallas de tu app, Android Studio ofrece herramientas visuales que te permiten arrastrar y soltar componentes (botones, textos, imágenes) y ver los cambios reflejados en tiempo real, sin necesidad de compilar todo el proyecto de nuevo .

* Perfiladores y Herramientas de Depuración: Incluye analizadores en tiempo real del uso de CPU, memoria, red y batería de tu app. Puedes pausar la ejecución, inspeccionar el valor de las variables, y encontrar "cuellos de botella" o fugas de memoria que afectarían el rendimiento.

## Android Studio vs. IntelliJ IDEA


|Característica	|Android Studio	|IntelliJ IDEA (Community)|
|---------------|---------------|-------------------------|
|Enfoque Principal	|Desarrollo de apps para Android (móviles, tablets, wearables, TV) .	|Desarrollo general para JVM (Kotlin, Java, backend, aplicaciones de escritorio).|
|Creador / Soporte	|Desarrollado por Google (sobre la base de IntelliJ) .	|Desarrollado por JetBrains (los creadores de Kotlin).|
|Herramientas Exclusivas	|Emulador de Android, editores de diseño de layouts (XML y Compose), herramientas específicas de Google Play (firmado, análisis de APK) .	|Soporte superior para desarrollo web, frameworks de backend (Spring, Ktor), bases de datos y herramientas de diagramación UML.|

¿Cuál elegir?	Es la elección obligatoria si quieres crear apps para Android .	Es la mejor opción si quieres aprender Kotlin para backend, scripts de consola o aplicaciones de escritorio multiplataforma .
En resumen, todo lo que puedes hacer en Android Studio está basado en IntelliJ IDEA . Son "hermanos", pero cada uno está especializado en un tipo de proyecto.

## crear proyecto

Creación de un Proyecto (Paso Rápido)

El proceso es muy similar al de IntelliJ que ya conoces, con pequeñas variaciones propias de Android:

1. Al abrir Android Studio, selecciona "New Project" .
2. Elige una plantilla para tu primera pantalla. Se abrirá una ventana con varias opciones. Aquí debes seleccionar la pestaña "Phone and Tablet" y luego elegir la plantilla "Empty Activity".¿Por qué esta plantilla? Es la más recomendada para empezar con Compose. Crea un proyecto simple con una sola pantalla y todo lo necesario para que veas tu primer "Hola Mundo" funcionando
3. Configura tu proyecto: En la siguiente pantalla, completa los detalles de tu app. Los más importantes son:
    * Name: El nombre de tu aplicación (por ejemplo, "MiPrimeraAppCompose").
    * Package name: El identificador único de tu app (suele ser algo como com.tunombre.miprimeraappcompose).
    * Save location: La carpeta donde se guardará el proyecto.
    * Language: Asegúrate de que esté seleccionado Kotlin. Es el único lenguaje compatible con Compose.
    * Minimum SDK: Selecciona API 24: Android 7.0 (Nougat) o una versión posterior. Esto define la versión más antigua de Android en la que funcionará tu app.
    * Use Jetpack Compose UI: Asegúrate de que esta casilla esté marcada. ¡Esto es crucial! Activa todas las configuraciones necesarias para usar Compose.
4. Define el Minimum SDK: esto determina la versión de Android más antigua en la que funcionará tu app (elige la que quieras, por ejemplo, API 24: Android 7.0).
5. Haz clic en "Finish". Android Studio generará toda la estructura de carpetas y archivos y sincronizará el proyecto con Gradle automáticamente.

Breve descripción:

**Gradle Scrpts** es un archivo de configuración, si abres **build.gradle.kts** veras, en *plugings* los módulos importados, en *android* la descripción de proyecto.

**app/kotlin+java**/com.sunombre.suproyecto/ui.theme contiene los estilos de compose.
**app/kotlin+java**/MainActivity es el código principal.



## descarga

[Descargar Android studio](https://developer.android.com/studio?hl=es-419)

> Nota Requerimientos: memoria 8mb, SO recomendado 64 bits, procesador intel core 2da generacion+. Disco 16 gb+, resolución 1920*1080.

## Ejemplo

Crear una aplicacción movil cpon jetpack compose. Jetpack Compose es el kit de herramientas moderno de Android para construir interfaces de usuario (UI) de forma declarativa utilizando código Kotlin. Fue lanzado por Google para reemplazar el sistema tradicional de vistas basado en XML (como LinearLayout, TextView, Button, etc.). Ejemplo: en lugar de decir cómo construir la UI paso a paso (imperativo), con Compose declaras cómo debe verse la UI según el estado actual de los datos. Antes `findViewById<TextView>(R.id.texto).text = "Hola"` ahora: `Text("Hola")`

Interfaz de la app:

<svg version="1.1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 257 431.99999999999994" width="257" height="431.99999999999994"><!-- svg-source:excalidraw --><metadata></metadata><defs><style class="style-fonts">
      @font-face { font-family: Excalifont; src: url(data:font/woff2;base64,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); }</style></defs><rect x="0" y="0" width="257" height="431.99999999999994" fill="#ffffff"></rect><g stroke-linecap="round" transform="translate(10 10) rotate(0 118.5 205.99999999999997)"><path d="M32 0 C92.82 -2.33, 154.88 0.43, 205 0 M32 0 C72.89 -0.02, 115.19 -1.33, 205 0 M205 0 C228.06 -0.68, 236.49 11.26, 237 32 M205 0 C227.12 -1.44, 237.34 10.91, 237 32 M237 32 C235.37 154.17, 235.51 276.04, 237 380 M237 32 C235.94 139.39, 236.59 246.53, 237 380 M237 380 C238.92 399.57, 226.45 410.37, 205 412 M237 380 C238.23 399.54, 226.14 412.71, 205 412 M205 412 C147.59 411.6, 92.77 412.39, 32 412 M205 412 C153.21 412.65, 103.73 412.66, 32 412 M32 412 C11.34 410.86, -0.81 401.17, 0 380 M32 412 C11.03 411.13, -1.97 403.44, 0 380 M0 380 C-2.67 241.81, -0.41 107.31, 0 32 M0 380 C-1.73 285.07, -1.53 188.81, 0 32 M0 32 C1.33 11.72, 12.4 0.53, 32 0 M0 32 C-0.61 10.58, 9.69 1.72, 32 0" stroke="#1e1e1e" stroke-width="2" fill="none"></path></g><g transform="translate(43.75592483193168 93.26880836938778) rotate(0.5509039792185391 84.0799560546875 37.5)"><text x="0" y="17.619999999999997" font-family="Excalifont, Xiaolai, sans-serif, Segoe UI Emoji" font-size="20px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="alphabetic">Google pixel Xpro</text><text x="0" y="42.62" font-family="Excalifont, Xiaolai, sans-serif, Segoe UI Emoji" font-size="20px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="alphabetic">Cloudy white</text><text x="0" y="67.62" font-family="Excalifont, Xiaolai, sans-serif, Segoe UI Emoji" font-size="20px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="alphabetic">128 GB</text></g><g transform="translate(43.75688861488334 185.29952851258497) rotate(0.5509039792185391 63.229957580566406 37.5)"><text x="0" y="17.619999999999997" font-family="Excalifont, Xiaolai, sans-serif, Segoe UI Emoji" font-size="20px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="alphabetic">Apple i phone</text><text x="0" y="42.62" font-family="Excalifont, Xiaolai, sans-serif, Segoe UI Emoji" font-size="20px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="alphabetic">128 GB</text><text x="0" y="67.62" font-family="Excalifont, Xiaolai, sans-serif, Segoe UI Emoji" font-size="20px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="alphabetic">Blue</text></g><g transform="translate(43.760749518338116 288.67244161258833) rotate(0.5509039792185391 90.70253727003319 38.03362917821539)"><text x="0" y="17.87073456320413" font-family="Excalifont, Xiaolai, sans-serif, Segoe UI Emoji" font-size="20.284602228381534px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="alphabetic">Samsung Galaxy Z</text><text x="0" y="43.22648734868105" font-family="Excalifont, Xiaolai, sans-serif, Segoe UI Emoji" font-size="20.284602228381534px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="alphabetic">64 GB</text><text x="0" y="68.58224013415796" font-family="Excalifont, Xiaolai, sans-serif, Segoe UI Emoji" font-size="20.284602228381534px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="alphabetic">5500</text></g><g stroke-linecap="round"><g transform="translate(42 178.00000000000006) rotate(0 89 -0.22173113696939595)"><path d="M0 0 C41.41 0.36, 80.26 -1.27, 178 0 M0 0 C41.53 -0.73, 82.95 -0.02, 178 0" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g></g><mask></mask><g stroke-linecap="round"><g transform="translate(41 275.22173113696937) rotate(0 89 -0.7147098659867765)"><path d="M0 0 C64.8 -3.37, 127.13 0.26, 178 0 M0 0 C64.19 -1.61, 129.26 -1.08, 178 0" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g></g><mask></mask><g stroke-linecap="round"><g transform="translate(44 382.22173113696937) rotate(0 89 0.11907035707861269)"><path d="M0 0 C48.22 -1.11, 95.04 1.59, 178 0 M0 0 C49.17 -0.1, 97.08 0.66, 178 0" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g></g><mask></mask><g transform="translate(69 25.500000000000057) rotate(0 53.33995056152344 12.5)"><text x="0" y="17.619999999999997" font-family="Excalifont, Xiaolai, sans-serif, Segoe UI Emoji" font-size="20px" fill="#1e1e1e" text-anchor="start" style="white-space: pre;" direction="ltr" dominant-baseline="alphabetic">Disponibles</text></g><g stroke-linecap="round"><g transform="translate(45 70.22173113696937) rotate(0 89 0.3139599031575244)"><path d="M0 0 C59.06 -0.02, 113.03 0.41, 178 0 M0 0 C50.85 0.68, 101.25 0.98, 178 0" stroke="#1e1e1e" stroke-width="1" fill="none"></path></g></g><mask></mask></svg>

1. Crea un nuevo proyecto 
    * file/new proyect/ 
    * elige la plantilla `empty activity`
    * elige nombre del **Package name** 
    * en **Build configuration language** elegir **kotlin** 
    * en **minimun sdk** versión mínima de **Android** donde correra tu app.
    * da clic en `next`.
2. revisa el archivo `/src/MainActivity.kt` es el equivalente al `main()` en lenguaje C.
3. Ubica una api fake: [Api fake](https://restful-api.dev/)
4. elige [all](https://api.restful-api.dev/objects)
5. crea una clase para almacenar los datos:
   1. colocate en el paquete principal: **com.sunombre.suproyecto**/clic derecho/new/(kotlin class/file)
   2. elije **data class**
   3. ponle como nombre *device*
   4. ponle las propiedades:
   ```kotlin
   data class device(
        val id: Long,
        val name: String,
        val data: spec?
    )
   ```
   5. observa que data hace referencia a spec (especificaciones del objeto como color y capacidad [observa los datos]), por tanto necesitamos crear una nueva class data que llamaremos *spec*, construyela con los coampos:
   ```kotlin
   data class spec(
        val color: String?,
        val capacity: String?
    )
   ```
   6. código

Observa en el archivo `Main.activity` que tenemos una clase que hereda de `ComponentActivity` Una Activity es un componente fundamental de una aplicación Android que representa una pantalla con la que el usuario puede interactuar.

La función `fun onCreate()` se ejecuta al crear la actividad, dentro puede ver `setContent {}` que es una sentencia del Jetpack Compose que añade la interfaz gráfica a la actividad. `DeviceTheme{}` define el tema, es tomado de Material design.

`scaffold{}` es el contenedor principal de la interfaz.

dentro se llama a la función `Greeting(name = "Android", modifier = Modifier.padding(innerPadding))` Las vistas en Jetpack compose se construyen a partir de funciones kotlin marcadas con `@Composable` y se deben escribir en Pascal Case.

en la función `Greeting` tenemos un componente:
```kotlin
    Text(
        text = "Hello $name!",
        modifier = modifier
    )
```

   >Nota Una **Data Class** es una clase especial en Kotlin diseñada exclusivamente para almacenar datos. Automáticamente genera código útil como equals(), hashCode(), toString(), copy(), y los métodos de componente para destructuración.

   >Nota Un componente de Android es un bloque de construcción fundamental de una aplicación Android. Cada componente tiene un propósito específico y un ciclo de vida propio, y pueden activarse de diferentes maneras (por el usuario, el sistema u otros componentes).