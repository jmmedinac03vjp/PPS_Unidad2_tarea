# Tarea Unidad 1 - RA5. Tarea para entregar Unidad1

**Lee la tarea hasta el final** para ver lo que tienes que entregar e ir cogiendo las evidencias y ver lo que tienes que documentar.

**Índice**

[Objetivos](#objetivos)

[Resultados de aprendizaje y Criterios de Evaluación](#resultados-de-aprendizaje-y-criterios-de-evaluación)

[Desarrollo](#desarrollo)

[Entrega](#entrega)

---

# OBJETIVOS
Esta actividad tiene como objetivo poner en práctica los contenidos tratados en esta unidad:

- Analizar y comprender la estructura interna del código (clases, métodos, flujos de control) y su modelo de ejecución (transiciones de estado y manejo de excepciones) para determinar los puntos críticos de prueba.

- Aplicar las herramientas del IDE (Integrated Development Environment) para la ejecución, depuración paso a paso y seguimiento del flujo de control, identificando y resolviendo posibles errores lógicos o de sintaxis.

- Diseñar, implementar y ejecutar pruebas unitarias que cubran la totalidad de los requisitos funcionales y no funcionales, validando la lógica individual de cada componente del código.

- Verificar que la aplicación maneja correctamente las reglas de negocio (precios, transiciones de fase y gestión de estados de error), tal como se define en la documentación.

- Ejecutar la aplicación en un entorno controlado para simular su comportamiento en un contexto real, validando la interacción entre sus componentes y el entorno de runtime.


---

# RESULTADOS DE APRENDIZAJE Y CRITERIOS DE EVALUACION

Esta actividad se relaciona con el resultado de aprendizaje y criterios de evaluación RA 1 a, b,c, d y e.

---
# PREPARAR EL REPOSITORIO

Utilizaremos **`GitHub Classroom`** para la entrega de esta actividad.

- Usa este código de invitación que tienes en la plataforma `Moodle` para realizar esta tarea.

1. Pincha en el enlace y **acepta la asignación**.

![](./docs/images/tu3.png)

2. Es posible que te aparezca un mensaje de problemas de acceso al repositorio:

![](./docs/images/tu1.png)

3. Si es así es posible que recibas en el email vinculado a tu `Github`, un correo con la asignación.

![](./docs/images/tu2.png)

4. Pincha en el enlace que te ha llegado al correo, **acepta la asignación** y sigue los pasos que te indican.

![](./docs/images/tu4.png)

5.  Puedes acceder a la tarea desde el **enlace de `github` o** clonando el repositorio **desde `Visual Studio Code`**.

![](./docs/images/tu31.png)

6. Ya podrás **acceder al repositorio** con la tarea a realizar.

7. **Guarda la dirección ya que está tarea no aparecerá en tu repositorio** al ser un repositorio del classroom https://github.com/PPS-CETI-vjp/NombreTarea-TuUSUARIOGITHUB

**Si le das a Acceder con Visual Studio Code**, tendrás que dar a permitir abrir, enlaces, descargar extensiones para vscode, confiar en los autores,etc. Se creará tu repositorio en `$HOME/Github-classroom/`.

![](./docs/images/tu32.png)

- Si le das al repositorio, te llevará a tu repositorio. Te habrá creado un repositorio en tu espacio personal de `github classroom` que tendrás que modificar.

![](./docs/images/tu33.png)

- Desde mi panel de control tendré acceso a tu repositorio, o sea que **ya no tendrás que poner tu repositorio como público**. Como profesor, yo tendré acceso.

---

# DESARROLLO

> **Nota importante**    
> Documenta explicando claramente los procesos realizados, incluyendo fragmentos de código con los comandos utilizados y/o adjuntado las capturas de pantallas necesarias que demuestren que has realizado las operaciones, así como el resultado de los productos.
>
> Las capturas de pantalla serán a pantalla completa y deberá visualizarse tu nombre en el terminal o bien la imagen de tu usuario en la plataforma.
>
> Deberás de añadir como colaborador en tu repositorio de GitHub al profesor: `PPSvjp` **Settings** > **Collaborators**.
Lee la tarea hasta el final para ver lo que tienes que entregar e ir cogiendo las evidencias y ver lo que tienes que documentar.

## 1. Documentación y prueba del programa

Aquí tienes [un archivo comprimido con el código de la aplicacion `lavadero` y `main_app`.](./src.zip)   
La aplicación de la que se proporciona el código, y con nombre `lavadero` se ha creado según las siguientes premisas:

1. Cuando se crea un lavadero, éste no tiene ingresos, no está ocupado, está en fase 0 y todas las opciones de lavado (prelavado a mano, secado a mano y encerado) están puestas a false.
2. Cuando se intenta comprar un lavado con encerado pero sin secado a mano, se produce una ValueError.
3. Cuando se intenta hacer un lavado mientras que otro ya está en marcha, se produce una ValueError.
4. Si seleccionamos un lavado con prelavado a mano, los ingresos de lavadero son 6,50€.
5. Si seleccionamos un lavado con secado a mano, los ingresos son 6,00€.
6. Si seleccionamos un lavado con secado a mano y encerado, los ingresos son 7,20€.
7. Si seleccionamos un lavado con prelavado a mano y secado a mano, los ingresos son 7,50€.
8. Si seleccionamos un lavado con prelavado a mano, secado a mano y encerado, los ingresos son 8,70€.
9. Si seleccionamos un lavado sin extras y vamos avanzando fases, el lavadero pasa por las fases 0, 1, 3, 4, 5, 6, 0.
10. Si seleccionamos un lavado con prelavado a mano y vamos avanzando fases, el lavadero pasa por las fases 0, 1, 2, 3, 4, 5, 6, 0.
11. Si seleccionamos un lavado con secado a mano y vamos avanzando fases, el lavadero pasa por las fases 0, 1, 3, 4, 5, 7, 0.12. 
12. Si seleccionamos un lavado con secado a mano y encerado y vamos avanzando fases, el lavadero pasa por las fases 0, 1, 3, 4, 5, 7, 8, 0.
13. Si seleccionamos un lavado con prelavado a mano y secado a mano y vamos avanzando fases, el lavadero pasa por las fases 0, 1, 2, 3, 4, 5, 7, 0.
14. Si seleccionamos un lavado con prelavado a mano, secado a mano y encerado y vamos avanzando fases, el lavadero pasa por las fases 0, 1, 2, 3, 4, 5, 7, 8, 0.


> Utiliza el **IDE Visual Studio Code** o tu IDE preferido para hacer las siguientes acciones:
>
> **Apartado 1**. Añade los comentarios al código de la aplicación indicando para que sirven las diferentes sentencias, funciones, etc. 
>> Si has realizado la actividad [Actividad-ElementosProgramaPython](../Actividad-ElementosProgramaPython/README.md) puedes adjuntar el `cuaderno Jupyter Notebook`, si no es así, inserta comentarios directamente en el código fuente. 
> 
>
> **Apartado 2**. Ejecuta el programa mediante las opciones de Ejecución y Depuración del IDE.
>
> !!!IMPORTANTE¡¡¡ Este código tiene errores (tendrás que solucionar los errores antes de ejecutarlo). Este apartado tiene relación con la actividad [Actividad-EntornosDesarrollo](../Actividad-EntornosDesarrollo/README.md).
> 
> Documenta los errores encontrados indicando a que se debian esos errores y cómo lo has solucionado.

## 2. Realización de los test unitarios de la aplicación.

> Dado el [código que representa la aplicación de un lavadero de coches](./src.zip) que va pasando por diferentes fases, crea un clase de test en pyton3 (Pytest o Unittest, el que prefieras) llamada Lavadero que compruebe el funcionamiento del programa. 
>
> Tienes el archivo de pruebas incluido en el archivo comprimido [test_lavadero_unittest.py](./src.zip) que te puede servir de inicio y ayuda para realizar los tests.
>
> El **nombre de la función** que realiza el test debe de **contener en número del test**, por ejemplo: `def test1_estado_inicial_inactivo` se correspondería con el **test 1**.
>
> Las diferentes **pruebas deben corresponderse con cada uno de los enunciados siguientes**, y deberán incluir en el  comentario, el **número de test** correspondiente:

1. Cuando se crea un lavadero, éste no tiene ingresos, no está ocupado, está en fase 0 y todas las opciones de lavado (prelavado a mano, secado a mano y encerado) están puestas a false.

Por ejemplo  parte del test 1 sería algo similar a esto en `Unittest`:
```python 
def test1_estado_inicial_inactivo(lavadero_vacio):
    """Test 1: Verifica el estado inicial del lavadero."""
    assert lavadero_vacio.fase == Lavadero.FASE_INACTIVO
    assert lavadero_vacio.ingresos == 0.0
    assert lavadero_vacio.ocupado is False

```

2. Cuando se intenta comprar un lavado con encerado pero sin secado a mano, se produce una ValueError.

En este otro caso sería algo así, también en `Unittest`:

```python
def test2_excepcion_encerado_sin_secado(lavadero):
    """
    Comprueba que encerar sin secado a mano lanza ValueError.
    """
    with self.assertRaises(ValueError):
    self.lavadero._hacer_lavado(False, False, True)
```
> Este test de excepción se puede completar para que nos compare la cadena de mensaje de error.

3. Cuando se intenta hacer un lavado mientras que otro ya está en marcha, se produce una ValueError.
4. Si seleccionamos un lavado con prelavado a mano, los ingresos de lavadero son 6,50€.
5. Si seleccionamos un lavado con secado a mano, los ingresos son 6,00€.
6. Si seleccionamos un lavado con secado a mano y encerado, los ingresos son 7,20€.
7. Si seleccionamos un lavado con prelavado a mano y secado a mano, los ingresos son 7,50€.
8. Si seleccionamos un lavado con prelavado a mano, secado a mano y encerado, los ingresos son 8,70€.

> Para los siguientes tests recuerda que tienes la función `def ejecutar_y_obtener_fases(self, prelavado, secado, encerado)`
> Esta función auxiliar nos devuleve una lista con las fases por las que ha pasado un lavado.
```python
    # Esta función es útil para pruebas unitarias, no es parte del lavadero real
    # nos crea un array con las fases visitadas en un ciclo completo

    def ejecutar_y_obtener_fases(self, prelavado, secado, encerado):
        """Ejecuta un ciclo completo y devuelve la lista de fases visitadas."""
        self._hacer_lavado(prelavado, secado, encerado)
        fases_visitadas = [self.fase]
        
        while self.ocupado:
            # Usamos un límite de pasos para evitar bucles infinitos en caso de error
            if len(fases_visitadas) > 15:
                raise Exception("Bucle infinito detectado en la simulación de fases.")
            self.avanzarFase()
            fases_visitadas.append(self.fase)
            
        return fases_visitadas
```

9. Si seleccionamos un lavado sin extras y vamos avanzando fases, el lavadero pasa por las fases 0, 1, 3, 4, 5, 6, 0. En este caso el test podría ser algo así: 

```python
    def test9_flujo_rapido_sin_extras(self):
        """Test 9: Simula el flujo rápido sin opciones opcionales."""
        fases_esperadas = [0, 1, 3, 4, 5, 6, 0]
        # Ejecutar el ciclo completo y obtener las fases
        fases_obtenidas = self.lavadero.ejecutar_y_obtener_fases(prelavado=False, secado=False, encerado=False)
        
        # Verificar que las fases obtenidas coinciden con las esperadas
        self.assertEqual(fases_obtenidas, fases_esperadas, 
                        f"Secuencia de fases incorrecta.\nEsperadas: {fases_esperadas}\nObtenidas: {fases_obtenidas}")
      
 

```
10. Si seleccionamos un lavado con prelavado a mano y vamos avanzando fases, el lavadero pasa por las fases 0, 1, 2, 3, 4, 5, 6, 0.
11. Si seleccionamos un lavado con secado a mano y vamos avanzando fases, el lavadero pasa por las fases 0, 1, 3, 4, 5, 7, 0. 
12. Si seleccionamos un lavado con secado a mano y encerado y vamos avanzando fases, el lavadero pasa por las fases 0, 1, 3, 4, 5, 7, 8, 0.
13. Si seleccionamos un lavado con prelavado a mano y secado a mano y vamos avanzando fases, el lavadero pasa por las fases 0, 1, 2, 3, 4, 5, 7, 0.
14. Si seleccionamos un lavado con prelavado a mano, secado a mano y encerado y vamos avanzando fases, el lavadero pasa por las fases 0, 1, 2, 3, 4, 5, 7, 8, 0.


> !!!IMPORTANTE¡¡¡ Este código tiene errores que deberían de descubrir las pruebas.
>
> **Apartado 3**. A partir de los resultados de los tests, se deben corregir también los problemas encontrados en el código hasta que todos los tests sean correctos.
> 
> **Documenta los errores encontrados** indicando a qué se debían esos errores y cómo lo has solucionado y adjunta los test pasados.
> Ejecuta los test con modificador `-v` (Verbose), para que nos muestre información de los tests:

```python
# Para Unittest 
# PYTHONPATH=src python3 -m unittest ./tests/ruta_al_test.py -v
# también podemos usarlo con discover indicando carpeta de tests
# PYTHONPATH=src python3 -m unittest discover -v /tests
# En Pytest podemos también usar -v
# PYTHONPATH=src pytest tests/ruta_al_test.py -v
```
## 3. Ejecución de la aplicación en un entorno controlado

> **Apartado 4**: Ejecuta la aplicación en un entorno controlado (Sandbox). Si has realizado la actividad [Actividad de Sandboxing](../Actividad-Sandboxing/) con otra aplicación, también es válida.

## 4. Reflexión sobre comparación de la infraestructura de seguridad de los lenguajes.

> **Apartado 5**. Has podido leer en [los contenidos teóricos](../ContenidosTeoricos/PPSUnidad1-InfraestructurasSeguridad.pdf)las medidas de seguridad que incorporan algunos de los lenguajes. **Escribe una reflexión personal** acerca de ellos. También puedes basarte en la tabla comparativa o en búsquedas sobre los lenguajes de programación más seguros. 
---

# ENTREGA
## Indicaciones de entrega

Al acceder a la tarea en `classroom.github.com` se te ha creado un repositorio en tu espacio de `Github Classroom`. En él es en el que tendrás que documentar la realización de los diferentes apartados de la tarea.

> Observa que al ser repositorio privado, no te va a permitir configurar `GitHub Pages`. No obstante **deberás configurar `Mkdocs` para que genere las páginas html** sobre los archivos `.md` donde estás documentando todo.
> Recuerda **añadir toda la estructura de `mkdocs`**, `requeriments.txt` y el `workflow` de `GitHub Actions` para que se genere la documentación en la rama `GH-Pages`.
>
> **Para visualizar los archivos `html`** que se están creando con ` mkdocs`, con php podemos **crear un servidor web** para visualizar los archivos creados: `php -S 0:8080` nos muestra el contenido web del directorio actual, por lo que si yo estoy en la rama `gh-pages` podré ver los archivos `html` generados.

```bash
# creo una carpeta donde visualizar mi web
mkdir /ruta/a/carpeta/web
# Clono mi respositorio
git clone Mirespositorio/MiTareaUnidadX.git 
# Me coloco en la carpeta clonada
cd MiTareaUnidadX
# Me cambio a la rama gh-pages
git checkout gh-pages
# Levantamos el servidor web con php
php -S 0:8080
```

Visualizaríamos el contenido web de nuestro respositorio en <http://localhost:8080>

![](./docs/images/tu37.png)

---

Una vez realizada la tarea, el envío se realizará a través de la plataforma.

**Deberás de entregar** al menos:

- El **repositorio** que has creado, **comprimido** en un archivo.
- El **enlace** a tu repositorio en la página de `classroom.github.com`.

La documentación generada en la rama `gh-pages` del repositorio (*recuerda que se generan los archivos .md colocados en la carpeta docs*) debe de contener al menos:
- Archivo **Index.md** con enlace al resto de secciones.

La documentación en `GitHub Pages` debe de contener al menos:
- Archivo **Index.md** con **secciones**:
    - **Elementos de Python**: donde figure el código comentado que has creado o enlace a `Jupyter Notebook`.
    - **Ejecución y Depuración**: Problemas que había en el código y cómo se ha solucionado. Debe de estar explicado y contener capturas de pantalla. (Recuerda que las capturas de pantalla deben de ser a pantalla completa y deben de observarse el terminal con tu nombre y/o tu imagen de la plataforma moodle).
    - **Pruebas** con la explicación sobre que las pruebas que has hecho, errores encontrados, el código de dichas pruebas y la ejecución del conjunto de pruebas en el IDE.
    - **Ejecución en Sandbox** con la explicación del proceso de ejecución en una **SandBox** y capturas de pantalla del proceso.
    - **Reflexión sobre comparación de la infraestructura de seguridad de los lenguajes** con la reflexión que has hecho en el punto 4.

El archivo comprimido se nombrará siguiendo las siguientes pautas:

`PPS-Unidad-TareaRA-Apellido1_Apellido2_Nombre`

Asegúrate que el nombre no contenga la letra ñ, tildes ni caracteres especiales extraños. Así por ejemplo la alumna Begoña Sánchez Mañas para la primera unidad del MP de PPS, debería nombrar esta tarea como...

PPS-Unidad2-TareaRA2-sanchez_manas_begona

## Calificación de la tarea

La puntuación de los apartados es la siguiente:

Si **no se adjunta el repositorio comprimido, no se indica la dirección del enlace a la documentación en GitHub.io o no se añade como colaborador en el repositorio al profesor**, la tarea será **calificada como 0**

> NOTA IMPORTANTE
> 
>Aquellos apartados/subapartados en los que las capturas de pantalla no sean claras o no tengan como fondo de pantalla la plataforma con tu usuario mostrando claramente la foto de tu perfil, no serán corregidos.

En el resto de los casos, la puntuación de los apartados es la siguiente:

- Apartado 1. Creación del repositorio  (hasta 1,5 puntos).  
- Apartado 2. Creación de WorkFlow de `GitHub Actions` (hasta 1,5 puntos).  
- Apartado 3. Vinculación con GitHub Pages (hasta 1,5 puntos).  
- Apartado 4. Creación de un contenedor de servicios `NGINX` con Docker(hasta 1,5 puntos).  
- Apartado 5. Documentación: presentación, extensión, exactitud, riqueza en síntaxis de MarkDown, etc. (hasta 4 puntos).

---
[![Licencia: CC BY-NC-SA 4.0](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
