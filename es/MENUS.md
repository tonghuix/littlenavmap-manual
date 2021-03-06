## Menús y barras de herramientas {#menus-and-toolbars}

Este capítulo describe todas las opciones de menú de _Little Navmap_. 
Encontrará la mayor parte de esta funcionalidad en las barras de herramientas, las cuales no están descritas por separado. Las combinaciones de teclas se pueden ver en los elementos del menú y no se enumeran en este manual.

![Little Navmap Menu and Toolbars](../images/menutoolbar.jpg "Little Navmap Menu and Toolbars")

_**Imagen superior:** Menú y barras de herramientas colocadas en sus posiciones predeterminadas._

### Menú Archivo {#file-menu}

#### ![New Flight Plan](../images/icons/filenew.png "New Flight Plan") Nuevo Plan de Vuelo {#new-flight-plan}

Borra el plan de vuelo actual.

Tiene que utilizar el diálogo [Menú Contextual de la tabla de resultados de búsqueda](SEARCH.md#search-result-table-view-context-menu), [Menú contextual del Mapa](MAPDISPLAY.md#map-context-menu) o el [Descripción de la Ruta del Plan de Vuelo](ROUTEDESCR.md) para crear un plan de vuelo.

#### ![Open Flight Plan](../images/icons/fileopen.png "Open Flight Plan") Abrir el Plan de Vuelo {#open-flight-plan}

Abre el archivo de plan de vuelo PLN de FSX, PLN de FS9, PNL de FSC, FMS de X-Plane o FLP. El tipo de archivo se determina por el contenido, no por su extensión. Consultar [Flight Plan Formats](FLIGHTPLANFMT.md) para obtener más información.

El plan de vuelo abierto se volverá a cargar de nuevo al inicio \(la recarga y el centrado se pueden desactivar en el diálogo `Opciones` dentro de las pestañas `Inicio` e `Interfaz de usuario`\).

La información de procedimientos y la velocidad sobre el terreno se añadirá al plan de vuelo si se guarda el archivo como PLN en _Little Navmap_. La información adicional se ignorará en FSX o P3D pero  _Little Navmap_ permite cargar toda la información.

#### ![Append flight plan](../images/icons/fileappend.png "Append flight plan") Adjuntar el Plan de Vuelo {#append-flight-plan}

Agrega salidas, llegadas y todos los waypoints del plan de vuelo actual.

El uso de `Adjuntar Plan de Vuelo` permite cargar o fusionar planes de vuelo completos o o fragmentos a un nuevo plan de vuelo. Todos los waypoints se añaden al final del plan de vuelo actual. Entonces puede usar las opciones del menú contextual `Borrar tramos seleccionados` y `Mover los tramos seleccionaos arriba/abajo` para organizar los waypoints y aeropuertos como sea necesario. Consultar [Menú contextual de la tabla de planes de vuelo](FLIGHTPLAN.md#flight-plan-table-view-context-menu).

Todos los procedimientos de salida se eliminan cuando se adjunta un plan de vuelo.

#### ![Save Flight Plan](../images/icons/filesave.png "Save Flight Plan") Grabar el Plan de Vuelo {#save-flight-plan}

#### ![Save Flight Plan as PLN](../images/icons/filesaveas.png "Save Flight Plan as PLN") Grabar el Plan de Vuelo como PLN {#save-flight-plan-as}

Graba el plan de vuelo como archivo para FSX/P3D \(formato XML\). 
Este formato de anotación permite guardar todos los tributos del plan de vuelo de *Little Navmap*.

`Grabar Plan de Vuelo en formato PLN` cambia el tipo y nombre de archivo actual en *Little Navmap* lo que significa que todos los guardados siguientes irán con el nuevo formato de archivo PLN.

Es recomendable grabar todos los planes de vuelo en este formato para mantener toda la información del plan. Incluso cuando se utiliza el formato limitado FMS para X-Plane. Consultar [Formatos de Planes de Vuelo](FLIGHTPLANFMT.md) para obtener más información.

_Little Navmap_ permitirá la creación de planes de vuelo que pueden ser útiles como un fragmento de plan de vuelo pero que el simulador de vuelo no puede usar. Esto ocurre si un plan de vuelo no tiene un aeropuerto de salida o de destino. Se mostrará un cuadro de diálogo de advertencia al guardar un plan de vuelo incompleto.

Los procedimientos se grabarán como anotaciones en el archivo del plan de vuelo si contiene algunos. Esto no causa ningún problema para los simuladores y la mayoría de los otros programas. Utilice [Exportar en formato plano como PLN](MENUS.md#export-clean-flight-plan) si tuvo problemas en la lectura de archivos PLN grabados con _Little Navmap_.

Tenga en cuenta que los puntos waypoints de un procedimiento no se guardan con el plan de vuelo. Esto no es compatible con FSX o P3D. Use el GPS, FMC u otras formas de seleccionar un procedimiento en su aeronave.

La velocidad sobre el terreno establecida también se guarda con el plan de vuelo.

**Tenga en cuenta que P3D v4.2 sobrescribe el plan de vuelo al cargar, lo que borra todas las anotaciones. Guarde una copia del plan en otra ubicación si desea mantener toda la información sobre los procedimientos o la velocidad.**

#### ![Save Flight Plan as X-Plane FMS 11](../images/icons/saveasfms.png "Save Flight Plan as X-Plane FMS 11") Grabar el Plan de vuelo como X-Plane FMS 11 {#save-flight-plan-as-fms11}

Graba el plan de vuelo utilizando el nuevo formato de X-Plane FMS 11. **Este formato puede ser usado solo en X-Plane 11.10 y superior. No intente cargarlo en el FMS o GPS de X-Plane 11.05. Esto puede colgar el simulador.**

Se mostrará un cuadro de diálogo de advertencia con la advertencia anterior al guardar.

Consultar [Formatos del Plan de Vuelo](FLIGHTPLANFMT.md) para obtener más información sobre las limitaciones.

Esta opción cambia el tipo y nombre del archivo actual, lo que significa que todos los guardados futuros irán al nuevo archivo FMS y el archivo se volverá a cargar en el próximo inicio.

Almacene los archivos FMS en el directorio `Output/FMS plans` dentro del directorio de X-Plane si desea utilizar el plan de vuelo en el GPS X-Plane, el G1000 o el FMS.

#### ![Save Flight Plan FLP](../images/icons/saveasflp.png "Save Flight Plan FLP") Grabar el Plan de Vuelo como FLP {#save-flight-plan-as-flp}

Exporta el plan de vuelo actual como un archivo FLP utilizable por X-Plane FMS, Aerosoft Airbus y otros add-ons adicionales. Este formato es limitado por lo que se muestra un cuadro de diálogo si se detectan características no compatibles en el plan de vuelo actual.

Consultar [Formatos de Plan de Vuelo](FLIGHTPLANFMT.md) para obtener más información sobre las limitaciones.

Esta opción cambia el tipo y nombre del archivo actual, lo que significa que todos los guardados futuros irán al nuevo archivo FLP y el archivo se volverá a cargar en el próximo inicio.

Almacene los archivos FMS en el directorio `Output/FMS plans` dentro del directorio de X-Plane si desea utilizar el plan de vuelo en el FMS de X-Plane.

#### ![Export as Clean PLN](../images/icons/filesaveclean.png "Export as Clean PLN") Exportar en formato plano como PLN {#export-clean-flight-plan}

Guarda un plan de vuelo sin ningún procedimiento o anotaciones de velocidad si los programas tienen problemas para leer los archivos PLN guardados por _Little Navmap_. Esto rara vez es necesario.

Como cualquier otra función de exportación, esto no cambia el nombre y tipo de archivo actual. Las copias guardadas seguirán usando el mismo nombre y formato de archivo que antes.

Consultar además [Formatos de Plan de Vuelo](FLIGHTPLANFMT.md).

#### ![Export Flight Plan as X-Plane FMS 3](../images/icons/saveasfms.png "Export Flight Plan as X-Plane FMS 3") Exportar el Plan de Vuelo como formato X-Plane FMS 3 {#export-flight-plan-as-fms3}

Guarda el plan de vuelo utilizando el anterior formato de X-Plane FMS 3, que es limitado pero puede ser cargado por X-Plane 10 y X-Plane 11.05. Se muestra un cuadro de diálogo de advertencia si se detectan características no compatibles en el plan de vuelo actual.

Consultar [Flight Plan Formats](FLIGHTPLANFMT.md) para obtener más información sobre las limitaciones.

Esta función de exportación no cambia el nombre y tipo de archivo actual. Las copias guardadas seguirán usando el mismo nombre y formato de archivo que antes.

Almacene los archivos FMS en el directorio `Output/FMS plans` dentro del directorio de X-Plane si desea utilizar el plan de vuelo en el GPS o FMS de X-Plane.

#### Exportar el Plan de Vuelo a otros Formatos (Sub-Menu) {#export-submenu}

Consultar [Formatos de Plan de Vuelo](FLIGHTPLANFMT.md) para información más detallada sobre los formatos de exportación disponibles.

Las funciones de exportación no modifican el nombre o tipo del actual archivo. Los guardados posteriores usarán el mismo nombre de archivo y formato anterior.

##### Exportar el Plan de Vuelo como Garmin GTN GFP {#save-flight-plan-as-gfp}

Exporta el plan de vuelo en el formato GFP usado por _Flight1 GTN 650/750_.

Los procedimientos no se incluyen en el archivo exportado.

Consultar [Formatos de Plan de Vuelo](FLIGHTPLANFMT.md#flight-plan-formats-gfp) para obtener más información sobre este formato de exportación y como trabajar alrededor de waypoints bloqueados.

##### Exportar el Plan de Vuelo como GFP para Reality XP GTN {#save-flight-plan-as-rxpgtn}

Guarda el plan de vuelo como archivo GFP utilizable por _Reality XP GTN 750/650 Touch_. Este formato permite guardar procedimientos y aerovías.

Consultar también [Notas sobre los Formatos de Garmin GFP y FPL](FLIGHTPLANFMT.md#garmin-notes) para información sobre rutas y otras observaciones.

##### Exportar el Plan de Vuelo a FPL para Reality XP GNS {#save-flight-plan-as-rxpgns}

Guarda el plan de vuelo como FPL utilizable por _Reality XP GNS 530W/430W V2_.

Los procedimientos y sus respectivos waypoints no se incluyen en el archivo exportado.

El directorio por defecto para guardar los planes de vuelo para las unidades GPS de todos los simuladores es
`C:\ProgramData\Garmin\GNS Trainer Data\GNS\FPL`. El directorio se creará automáticamente por _Little Navmap_ en la primera exportación si este no existe.

Consultar también [Notas sobre los Formatos GFP y FPL de Garmin](FLIGHTPLANFMT.md#garmin-notes).

##### Exportar el Plan de Vuelo como PMDG RTE {#export-flight-plan-as-rte}

Exporta el plan de vuelo como archivo PMDG RTE.

Los procedimientos y sus respectivos waypoints no se incluyen en el archivo exportado.

##### Exportar el Plan de Vuelo como TXT {#export-flight-plan-as-txt}

Exporta el plan de vuelo actual como archivo TXT utilizable en los aviones de JARDesign o Rotate Simulations.

Ni los procedimientos ni sus respectivos waypoints se incluyen en el archivo exportado.

##### Exportar el Plan de Vuelo com Majestic Dash FPR {#export-flight-plan-as-fpr}

Exporta del plan de vuelo actual para el software Majestic MJC8 Q400. 

Tenga en cuenta que la exportación se limita actualmente a una lista de waypoints.

El plan de vuelo debe guardarse en `FSXP3D\SimObjects\Airplanes\mjc8q400\nav\routes`.

##### Exportar el Plan de Vuelo como IXEG FPL {#export-flight-plan-as-fpl}

Exporta el plan de vuelo actual como archivo FPL utilizable por el Boeing 737 classic de IXEG.

SIDs, STARs o procedimientos de aproximación no se exportan.

El archivo se debe de guardar en `XPLANE\Aircraft\X-Aviation\IXEG 737 Classic\coroutes`. Tendría que crear este directorio manualmente si no existe.

##### Exportar el Plan de Vuelo a corte.in para el Airbus de Flight Factor {#export-flight-plan-as-fpl}

Adjunta el plan de vuelo al archivo de las rutas de compañía `corte.in` para el avión Airbus de Flight Factor.

El fichero se creará automáticamente si no existe. De lo contrario, el plan de vuelo se adjuntará al archivo. Debe eliminar el plan de vuelo manualmente del archivo `corte.in` con un simple editor de texto si desea deshacerse de él.
La ubicación del archivo depende del tipo de aeronave.

##### Exportar el plan de Vuelo para iFly {#export-flight-plan-as-ifly}

Guarde el plan de vuelo como archivo FLTPLAN para iFly 737NG. El formato no permite guardar los procedimientos.

Guarde el archivo en `FSXP3D\iFly\737NG\navdata\FLTPLAN`.

##### Exportar el Plan de Vuelo para ProSim {#export-flight-plan-as-prosim}

Adjunta el plan de vuelo al archivo `companyroutes.xml` para el simulador [ProSim](https://prosim-ar.com). El formato no permite guardar los procedimientos.

Crear un archivo de backup llamado `companyroutes.xml_lnm_backup` antes de modificar el archivo.

##### Exportar el Plan de Vuelo como PLN para BBS Airbus {#export-flight-plan-as-bbs}

Guarda el plan de vuelo como archivo PLN para el Airbus de Blackbox Simulations. El formato no permite guardar los procedimiento.

Guarda el archivo en `FSXP3D\BlackBox Simulation\Airbus A330` o `FSXP3D\Blackbox Simulation\Company Routes` dependiendo del avión.

##### Exportar el Plan de Vuelo para UFMC {#export-flight-plan-as-ufmc}

Guarda el plan de vuelo como archivo [UFMC](http://ufmc.eadt.eu). El formato no permite guardar los procedimientos.

Guarda el plan de vuelo en `XPLANE\Custom Data\UFMC\FlightPlans`.

##### Exportar el Plan de Vuelo para X-FMC {#export-flight-plan-as-xfmc}

Guarda el plan de vuelo como archivo FPL file utilizable por [X-FMC](https://www.x-fmc.com). El formato no permite guardar los procedimientos.

El archivo debe guardarse en la ruta `XPLANE\Resources\plugins\XFMC\FlightPlans`.

##### Exportar el Plan de Vuelo como GPX {#export-flight-plan-as-gpx}

Exporta el plan de vuelo actual en un archivo de formato de intercambio GPS que puede leer Google Earth y la mayoría de las demás aplicaciones SIG.

El plan de vuelo se exporta como una ruta y la aeronave sigue una trayectoria que incluye el tiempo y la altitud del simulador.

La ruta tiene la elevación de salida y destino y la altitud de crucero establecidas para todos los waypoints. Los waypoints de todos los procedimientos están incluidos en el archivo exportado. Tenga en cuenta que los waypoints no permitirán reproducir todas las partes de un procedimiento como esperas o procedimientos de viraje.

**No olvide limpiar el rastro de la aeronave \([Borrar trazos de trayectoria de aeronave](MENUS.md#delete-aircraft-trail)\) antes del vuelo para evitar segmentos antiguos en el archivo GPX exportado. O, deshabilite la recarga de los trazos en las opciones de diálogo de la página `Startup`**.


##### Mostrar el Plan de vuelo en SkyVector {#export-flight-plan-as-skyvector}

Abre el navegador por defecto y muestra el plan de vuelo actual en [SkyVector](https://skyvector.com). Los procedimientos no se muestran.

Ejemplo: [ESMS NEXI2B NILEN L617 ULMUG M609 TUTBI Z101 GUBAV STM7C ENBO](https://skyvector.com/?fpl=ESMS%20NILEN%20L617%20ULMUG%20M609%20TUTBI%20Z101%20GUBAV%20ENBO). Observe que faltan las SID y STAR en SkyVector.

##### Grabar Waypoints para aproximaciones {#export-flight-plan-approach-waypoints}
##### Grabar Waypoints para SID y STAR {#export-flight-plan-sid-star-waypoints}

Guarda waypoints de procedimiento en lugar de información de procedimiento si está marcada. Esto afecta a todos los formatos de exportación y guardado del plan de vuelo.

Utilice esto si su simulador, GPS o FMC no admite la carga o visualización de procedimientos de aproximación, SID o STAR.

La información del procedimiento se reemplaza por los respectivos waypoints que permiten mostrar los procedimientos en unidades GPS o FMS limitadas.

Guardar los planes de vuelo con este método tiene varias limitaciones:

* Varios tipos de tramos de aproximación, como las esperas, los virajes y los procedimientos de viraje, no se pueden mostrar correctamente utilizando solo puntos de referencia/coordenadas.
* Las limitaciones de velocidad y altitud no se incluyen en los tramos exportados.
* La información del procedimiento se elimina del plan de vuelo guardado y no se puede volver a cargar correctamente en _Little Navmap_. Por lo tanto, verá los puntos de referencia de un SID o STAR, pero no la información detallada del procedimiento. Debe eliminar los puntos de ruta adicionales y volver a seleccionar los procedimientos después de la carga.

Debido a estas limitaciones, se recomienda guardar una copia del plan de vuelo con información completa antes de habilitar una de estas opciones.

#### ![Add Google Earth KML](../images/icons/kmlfileopen.png "Add Google Earth KML") Agregar Google Earth KML {#add-google-earth-kml}

Permite agregar uno o más archivos KML o KMZ de Google Earth a la visualización del mapa. Todos los archivos KML o KMZ agregados se volverán a cargar al inicio. La recarga y el centrado se pueden desactivar en el cuadro de diálogo `Opciones` en la pestaña `Inicio` e `Interfaz de usuario`.

Debido a la variedad de archivos KML no se puede garantizar que se visualizarán correctamente en el mapa todos los archivos.

#### ![Clear Google Earth KML from Map](../images/icons/cancel.png "Clear Google Earth KML from Map") Borrar KML de Google Earth de la Carta del Mapa {#clear-google-earth-kml-from-map}

Elimina del mapa todos los archivos KML cargados.

#### ![Offline](../images/icons/offline.png "Offline") Trabajar sin conexión {#work-offline}

Interrumpe la carga de datos en el mapa a través de internet. Esto afecta a  _OpenStreetMap_, _OpenTopoMap_ y a todos los otros temas online así como a los datos de elevación.
Una indicación `Sin conexión` en rojo se muestra en la barra de estado si se activa este modo.

Debe reiniciar la aplicación después de volver a conectarse.

### ![Save Map as Image](../images/icons/mapsaveasimage.png "Save Map as Image") Grabar el mapa como imagen {#save-map-as-image}

Guarda la vista actual del mapa como archivo de imagen. Los formatos permitidos son JPEG, PNG y BMP.

### ![Print Map](../images/icons/printmap.png "Print Map") Imprimir Mapa {#print-map}

Permite imprimir la vista actual del mapa. Consultar [Imprimir el mapa](PRINT.md#printing-the-map) para obtener más información.

### ![Print Flight Plan](../images/icons/printflightplan.png "Print Flight Plan") Imprimir Plan de Vuelo {#print-flight-plan}

Abre el diálogo de impresión que le permite seleccionar información relacionada del plan de vuelo para ser impresa. Consultar [Imprimir el mapa del plan de vuelo](PRINT.md#printing-the-flight-plan) para obtener más información.

### ![Quit](../images/icons/application-exit.png "Quit") Salir {#file-quit}

Abandona la aplicación. Pedirá una confirmación si se ha modificado el plan de vuelo.

### Menú del Plan de Vuelo {#flight-plan-menu}

#### ![Undo](../images/icons/undo.png "Undo")![Redo](../images/icons/redo.png "Redo") Deshacer/Rehacer {#undo-redo}

Permite deshacer y rehacer todos los cambios del plan de vuelo.

#### ![Select a Start Position for Departure](../images/icons/parkingstartset.png "Select a Start Position for Departure") Seleccionar el punto de Inicio para la Salida {#select-a-start-position-for-departure}

Se puede seleccionar un lugar de estacionamiento \(puerta, rampa o estación de combustible\), pista o helipuerto como posición de inicio en el aeropuerto de salida. También se puede seleccionar una posición de estacionamiento con la opción de menú contextual en el mapa [Establecer como punto de partida del plan de vuelo] (MAPDISPLAY.md#set-as-flight-plan-departure) al hacer clic derecho en una posición de estacionamiento. Si no se selecciona ninguna posición, el extremo de la pista principal más largo se selecciona automáticamente como inicio.

![Select Start Position Dialog](../images/selectstartposition.jpg "Select Start Position Dialog")

_**Imagen anterior:** El diálogo de selección de la posición de partida para EDDN._

#### ![Edit Flight Plan on Map](../images/icons/routeedit.png "Edit Flight Plan on Map") Editar el Plan de Vuelo en el mapa {#edit-flight-plan-on-map}

Toggles the flight plan drag and drop edit mode on the map. See [Flight Plan Editing](MAPFPEDIT.md#map-flight-plan-editing).

#### ![New Flight Plan from Route Description](../images/icons/newroutefromstring.png "New Flight Plan from Route Description") Plan de Vuelo nuevo desde descripción de la ruta {#new-flight-plan-from-description}

Abre un diálogo con la descripción de ruta del plan de vuelo actual que además permite modificar el actual plan de vuelo o introducir uno nuevo.
[Plan de Vuelo desde la descripción de ruta](ROUTEDESCR.md) da mejor información sobre este asunto.

#### ![Copy Flight Plan Route to Clipboard](../images/icons/routestring.png "Copy Flight Plan Route to Clipboard") Copia la Ruta del Plan de Vuelo al portapapeles {#flight-plan-route-clipboard}

Copia la descripción de ruta del plan de vuelo actual al portapapeles usando los ajustes del diálogo [Plan de Vuelo desde descripción de ruta](ROUTEDESCR.md#flight-plan-from-route-description) .

#### ![Calculate Direct](../images/icons/routedirect.png "Calculate Direct") Calcular Plan de Vuelo directo {#calculate-direct}

Elimina todos los waypoints intermedios y conecta salida y destino usando una gran línea.

Puede calcular un plan de vuelo entre cualquier tipo de waypoint, incluso puntos definidos por el usuario \(click derecho en el mapa y seleccionar `Agregar posición al plan de vuelo` para crear uno\). Esto permite la creación de fragmentos que pueden fusionarse en los planos de vuelo. Por ejemplo, puede usar esta característica para cruzar el Atlántico Norte con distintas salidas y destinos. Esto se aplica a todos los modos de cálculo del plan de vuelo.

#### ![Calculate Radionav](../images/icons/routeradio.png "Calculate Radionav") Calcular Radionavegación {#calculate-radionav}

Crea un plan de vuelo que usa solo estaciones VOR y NDB como waypoints 
e intenta asegurar la recepción de al menos una estación a lo largo de todo el plan de vuelo. Tenga en cuenta que si es posible las estaciones VOR son preferidas antes que las estaciones NDB y DME. El cálculo fallará si no se encuentran suficientes radioayudas entre la salida y el destino. Construya el plan de vuelo manualmente si este es el caso.

Este cálculo además puede ser usado para crear un fragmento del plan de vuelo entre cualquier tipo de waypoint.

#### ![Calculate high Altitude](../images/icons/routehigh.png "Calculate high Altitude") Cálculo a gran Altitud {#calculate-high-altitude}

Utiliza aerovías para crear el plan de vuelo.

Los planes de vuelo calculados a lo largo de las aerovías obedecerán todas las restricciones de estas, como el mínimo y la altitud. El programa también se ajustará a las restricciones de altitud unidireccional y altitud máxima basado en el Navdata de X-Plane.

En el campo de altitud del plan de vuelo se establece la altitud mínima resultante. El campo de altitud del plan de vuelo no cambia si no se encuentran restricciones de altitud a lo largo del plan de vuelo.

Se usa la regla mnemotécnica este/oeste para ajustar la altitud de crucero a valores impares/pares \(esto puede desactivarse en el diálogo `Opciones` en la pestaña `Plan de Vuelo`\).

El comportamiento por defecto es saltar desde el aeropuerto de salida al siguiente waypoint por la aerovía adecuada y viceversa para el aeropuerto de destino. Esto puede modificarse en el diálogo `Options` en la pestaña  `Plan de Vuelo` si se prefieren las estaciones VOR o NDB como puntos de transición a las aerovías.

La red de aerovías del simulador de vuelo no está completa \(por ejemplo, faltan las rutas del Atlántico norte - estas cambian diariamente\), por lo tanto el calculo en grandes áreas oceánicas puede fallar.

Cree la vía aérea manualmente como una solución temporal o use una herramienta de planificación en línea para obtener una cadena de ruta y use la opción `Nuevo plan de vuelo de la cadena` para crear el plan de vuelo.

Este cálculo puede utilizarse además para crear un fragmento del plan de vuelo entre cualquier tipo de waypoint.

#### ![Calculate low Altitude](../images/icons/routelow.png "Calculate low Altitude") Cálculo a baja Altitud {#calculate-low-altitude}

Calcula aerovías Victor de baja altitud para crear el plan de vuelo. Todo lo demás es igual al `Cálculo a gran Altitud`.

#### ![Calculate based on given Altitude](../images/icons/routealt.png "Calculate based on given Altitude") Cálculo basado en una Altitud dada {#calculate-based-on-given-altitude}

Use el valor en el campo de altitud del plan de vuelo para encontrar un plan de vuelo a lo largo de aerovías de baja altitud (Victor) y/o gran altitud (Jet). El cálculo fallará si el valor de altitud es demasiado bajo. Todo lo demás es igual que en `Cálculo a gran altitud`.

#### ![Reverse Flight Plan](../images/icons/routereverse.png "Reverse Flight Plan") Invertir Plan de Vuelo {#reverse-flight-plan}

Intercambia la salida y el destino e invierte el orden de todos los waypoints intermedios. Se asigna una pista predeterminada para la nueva posición de inicio de salida.

Tenga en cuenta que esta función no considera las vías aéreas de un solo sentido en la base de datos de X-Plane y puede dar como resultado un plan de vuelo no válido.

#### ![Adjust Flight Plan Altitude](../images/icons/routeadjustalt.png "Adjust Flight Plan Altitude") Ajustar Altitud del Plan de Vuelo {#adjust-flight-plan-alt}

Modifica la altitud del plan de vuelo de acuerdo a la regla mnemotécnica Este/Oeste y al tipo de ruta actual \(IFR o VFR\). Redondea la altitud en 1000 pies \(o metros\) hasta el siguiente valor impar para planes de vuelo dirección este o en 1000 pies \(o metros\) hasta el siguiente valor par para planes de vuelo dirección oeste. Añade 500 pies para planes de vuelo VFR.

### Menú Mapa {#map-menu}

#### ![Goto Home](../images/icons/home.png "Goto Home") Ir a la vista principal {#goto-home}

Va al área de inicio que se configuró usando [Definir partida](MAPDISPLAY.md#set-home) usando la posición y distancia de zoom guardada. El centro de la vista principal se resalta con el símbolo ![Home Symbol](../images/icons/homesymbol.png "Home Symbol") .

#### ![Go to Center for Distance Search](../images/icons/centermark.png "Go to Center for Distance Search") Ir al Centro de la Distancia de Búsqueda {#go-to-center-for-distance-search}

Va al punto central utilizado para la distancia de búsqueda. Consultar [Definir centro para distancia de búsqueda](MAPDISPLAY.md#set-center-for-distance-search). El centro para la distancia de búsqueda queda resaltado con el símbolo ![Distance Search Symbol](../images/icons/distancemark.png "Distance Search Symbol") .

#### ![Center Flight Plan](../images/icons/centerroute.png "Center Flight Plan") Centro del Plan de Vuelo {#center-flight-plan}

Aleja el mapa \(si es necesario\) para mostrar el plan de vuelo completo en el mapa.

#### ![Center Aircraft](../images/icons/centeraircraft.png "Center Aircraft") Centrar Aeronave {#center-aircraft}

Se acerca a la aeronave del usuario si está conectado directamente a un simulador de vuelo o se conecta de forma remota con [Little Navconnect](https://albar965.github.io/littlenavconnect.html) y mantiene la aeronave centrada en el mapa.

El centrado de la aeronave puede modificarse en el diálogo `Opciones` en la pestaña `Aeronave Simulada`.

#### ![Delete Aircraft Trail](../images/icons/aircrafttraildelete.png "Delete Aircraft Trail") Borra Trayectoria de la Aeronave {#delete-aircraft-trail}

Elimina la trayectoria de la aeronave del usuario. Esta es eliminada cuando se conecta al simulador de vuelo. La trayectoria se queda guardada y se cargará al arrancar el programa.

#### ![Map Position Back](../images/icons/back.png "Map Position Back") ![Map Position Forward](../images/icons/next.png "Map Position Forward") Posición del mapa Anterior/Posterior {#map-position-back-forward}

Salta hacia adelante o hacia atrás en el histórico de posición del mapa. El histórico completo se guarda y se restaura cuando se inicia _Little Navmap_.

### Menú Ver {#view-menu}

#### ![Reset Display Settings](../images/icons/centeraircraft.png "Reset Display Settings") Reinicializar Configuración de Pantalla {#reset-display-settings}

Reinicializa todos los ajustes del la pantalla de mapa a sus valores por defecto.

![By Reset Affected Settings](../images/resetdisplaysettings.jpg "By Reset Affected Settings")

_**Imagen superior:** Todos los botones de la barra de herramientas resaltados son afectados por _`Reinicializar configuración de pantalla`_._

#### Detalles

##### ![More Details](../images/icons/detailmore.png "More Details") Más Detalles {#more-details}

##### ![Default Details](../images/icons/detaildefault.png "More Details") Detalles por defecto {#default-details}

##### ![Less Details](../images/icons/detailless.png "Less Details") Menos Detalles {#less-details}

Aumenta o disminuye el nivel de detalle del mapa. Más detalles significa más aeropuertos, más ayudas a la navegación, más información de texto e iconos más grandes.

Tenga en cuenta que la información del mapa se truncará si se eligen demasiados detalles. Aparecerá un mensaje de advertencia rojo en la barra de estado si este es el caso.

El nivel de detalle se muestra en la barra de estado. El rango es -5 para el mínimo de detalles a +5 para el máxima de los detalles.

#### ![Force Show Addon Airports](../images/icons/airportaddon.png "Force Show Addon Airports") Forzar Mostrar los Aeropuertos Agregados {#force-show-addon-airports}

Los aeropuertos agregados siempre se muestran independientemente de los otros ajustes del mapa del aeropuerto si se selecciona esta opción. Esto permite ver solo aeropuertos agregados al marcar esta opción y deshabilitar la visualización de aeropuertos con pistas de asfalto, de tierra o vacíos.

#### ![Show Airports with hard Runways](../images/icons/airport.png "Show Airports with hard Runways") Mostrar Aeropuertos con pistas Duras {#show-airports-with-hard-runways}

Muestra aeropuertos que tengan al menos una pista con superficie dura.

#### ![Show Airports with soft Runways](../images/icons/airportsoft.png "Show Airports with soft Runways") Mostrar aeropuertos con pistas Blandas {#show-airports-with-soft-runways}

Muestra los aeropuertos que tienen solo superficies blandas o solo pistas de agua. Este tipo de aeropuertos podrían estar ocultos en el mapa dependiendo de la distancia de zoom.

#### ![Show empty Airports](../images/icons/airportempty.png "Show empty Airports") Mostrar Aeropuertos Vacios {#show-empty-airports}

Mostrar aeropuertos vacíos. Este botón o elemento de menú podría no ser visible según la configuración en el cuadro de diálogo `Opciones` en la pestaña `Visualización de mapa`. El estado de este botón se combina con los otros botones del aeropuerto. Esto significa, por ejemplo: debe habilitar la visualización del aeropuerto de superficie blanda y los aeropuertos vacíos para ver los aeropuertos vacíos que tienen solo pistas blandas.

Un aeropuerto vacío se define como que no tiene estacionamientos ni calles de rodaje ni aprons, y tampoco es uno agregado. Estos aeropuertos se tratan de manera diferente en _Little Navmap_ ya que son los más aburridos de todos los aeropuertos por defecto. Los aeropuertos vacíos se representan en gris y detrás de todos los otros aeropuertos en el mapa.

Los aeropuertos que solo tienen pistas de agua están excluidos de esta definición para evitar el ocultamiento involuntario.

##### X-Plane y los aeropuertos 3D

La función se puede extender a los aeropuertos de X-Plane que no están catalogados como `3D`. Esto puede hacerse seleccionando `Considerar todos los aeropuertos de X-Plane no 3D vacíos` en el diálogo `Opciones` dentro de la pestaña `Mapa`. Todos los aeropuertos que no estén marcados como `3D` se mostrarán en gris en el mapa y se pueden ocultar si están habilitados como se describe arriba.
Se considera un aeropuerto 3D si se encuentra en
`XPLANE/Custom Scenery/Global Airport Scenery/Earth nav data/apt.dat`.

Aunque la definición de `3D` es arbitraria. Un aeropuerto `3D` puede contener un solo objeto como un poste de luz o un cono de tráfico o puede ser un aeropuerto principal totalmente construido.

#### ![Show VOR Stations](../images/icons/vor.png "Show VOR Stations") Show VOR Stations {#show-vor-stations}

#### ![Show NDB Stations](../images/icons/ndb.png "Show NDB Stations") Mostrar estaciones VOR {#show-ndb-stations}

#### ![Show Waypoints](../images/icons/waypoint.png "Show Waypoints") Mostrar Waypoints {#show-waypoints}

#### ![Show ILS Feathers](../images/icons/ils.png "Show ILS Feathers") Mostrar las direcciones ILS {#show-ils-feathers}

#### ![Show Victor Airways](../images/icons/airwayvictor.png "Show Victor Airways") Mostrar las rutas aéreas Victor {#show-victor-airways}

#### ![Show Jet Airways](../images/icons/airwayjet.png "Show Jet Airways") Mostrar aerovías de Jets {#show-jet-airways}

Muestra u oculta en el mapa estas instalaciones o radioayudas. Las radioayudas pueden estar ocultas en el mapa dependiendo de la distancia de zoom.

#### Espacios Aéreos {#airspaces}

Tenga en cuenta que los espacios aéreos están ocultos si se muestra el diagrama del aeropuerto.

##### ![Show Airspaces](../images/icons/airspace.png "Show Airspaces") Mostrar espacios aéreos {#show-airspaces}

Permite habilitar o deshabilitar la visualización de todos los espacios aéreos con un solo click. Utilice los elementos del menú debajo de este o los botones de la barra de herramientas para mostrar u ocultar los diversos tipos de espacio aéreo.

La barra de herramientas de espacios aéreos contiene botones que tienen cada uno un menú desplegable que permite configurar la pantalla del espacio aéreo para mostrar u ocultar ciertos tipos de espacio aéreo. Cada menú desplegable también tiene entradas `Todos` y `Ninguno` para seleccionar o anular la selección de todos los tipos en el menú.

##### ![Show Online Network Airspaces](../images/icons/airspaceonline.png "Show Online Network Airspaces") Mostrar Espacios Aéreos de red en línea {#show-online-airspaces}

Este botón u opción de menú solo es visible si la red online está activada.

Permite ocultar o mostrar los centros, Torre, tierra, aproximación y otros espacios aéreos de la red en línea seleccionada actualmente, independientemente del simulador o Navigraph.

Los espacios aéreos online también se pueden mostrar u ocultar por tipo, usando los elementos del menú a continuación.

Tenga en cuenta que los círculos del espacio aéreo visualizados no representan los límites reales del espacio aéreo, sino que son meramente un indicador de la presencia de un centro o torre activo.

Consultar [Redes Online](ONLINENETWORKS.md) y [Vuelo Online](OPTIONS.md#online-flying).

##### ![ICAO Airspaces](../images/icons/airspaceicao.png "ICAO Airspaces") Espacio aéreo ICAO {#icao-airspaces}

Allows selection of Class A to Class E airspaces.

##### ![FIR Airspaces](../images/icons/airspacefir.png "FIR Airspaces") Espacio aéreo FIR {#fir-airspaces}

Permite la selección de los espacios aéreos Clase F y Clase G o regiones de información de vuelo.

##### ![Restricted Airspaces](../images/icons/airspacerestr.png "Restricted Airspaces") Espacios Aéreos Restringidos {#restricted-airspaces}

Muestra u oculta espacios aéreos MOA \(Area de operaciones militares\), restringidos, prohibidos y peligrosos.

##### ![Special Airspaces](../images/icons/airspacespec.png "Special Airspaces") Espacios Aéreos Especiales {#special-airspaces}

Muestra u oculta espacios aéreos de advertencia, alerta y entrenamiento.

##### ![Other Airspaces](../images/icons/airspaceother.png "Other Airspaces") Otros Espacios Aéreos {#other-airspaces}

Muestra centro, torre, categoría C y otros espacios aéreos.

##### ![Airspace Altitude Limitations](../images/icons/airspacealt.png "Airspace Altitude Limitations") Espacios Aéreos con limitación de Altitud {#airspace-altitude-limitations}

Permite filtrar la visualización del espacio aéreo por altitud. Ya sea por debajo o por encima de 10,000 pies o 18,000 pies o solo espacios aéreos que se cruzan con la altitud del plan de vuelo.

#### Puntos de Usuario

Permite ocultar o mostrar por tipo los waypoints definidos de usuario.

La opción del menú `Tipos Desconocidos` muestra u oculta todos los tipos que no pertenecen a un tipo conocido.

El tipo `Desconocido` ![Unknown](../images/icons/userpoint_Unknown.png "Airspace Altitude Limitations")
 muestra u oculta todos los puntos de usuario que son exactamente del tipo  `Desconocido`.

Consultar [Waypoints definidos por el Usuario](USERPOINT.md) para obtener más información sobre los puntos definidos por el usuario.

#### ![Show Flight Plan](../images/icons/route.png "Show Flight Plan") Mostrar Plan de Vuelo {#show-flight-plan}

Muestra u oculta el plan de vuelo. El plan de vuelo se muestra independiente de la distancia de zoom.

#### ![Show Missed Approaches](../images/icons/missed.png "Show Missed Approaches") Mostrar Aproximaciones Frustradas {#show-missed-approaches}

Muestra u oculta aproximaciones frustradas del plan de vuelo actual. Esto no afecta la previsualización en la pestaña de búsqueda `Procedimientos`.

**Tenga en cuenta que esta función modifica la secuencia de tramos del plan de vuelo actual:** La secuencia del tramo activo se detendrá si se alcanza el destino y no se muestran las aproximaciones frustradas. De lo contrario, la secuencia continuará con la aproximación frustrada y el progreso de la aeronave del simulador mostrará la distancia restante hasta el final de la aproximación frustrada.

#### ![Show Aircraft](../images/icons/aircraft.png "Show Aircraft") Mostrar Aeronave {#show-aircraft}

Muestra la aeronave del usuario y la mantiene centrada en el mapa si está conectado al simulador. La aeronave del usuario se muestra siempre independientemente de la distancia de zoom.

El color y la forma del icono indican el tipo de avión y si el avión está en tierra \(contorno gris\).

![User Aircraft](../images/icons/aircraft_small_user.png "User Aircraft") Aeronave del usuario en vuelo.

Un click sobre la aeronave del usuario muestra más información en el panel  `Aeronave del Simulador`.

Se puede encontrar más información para modificar el comportamiento mientras de vuela en el diálogo `Opciones` dentro de la pestaña [Aeronave del Simulador](OPTIONS.md#simulator-aircraft).

El centrado de la aeronave se desconectará cuando se utilice una de las siguientes funciones. Tenga en cuenta que este comportamiento predeterminado se puede modificar en el cuadro de diálogo de opciones.

* Hacer Doble-click dentro de la vista de table o ventana del mapa para hacer un zoom a un aeropuerto o radioayuda.
* Opción de menú contextual `Mostrar en mapa`.
* `Ir al Inicio` o `Ir al centro de la distancia de búsqueda`.
* `Mapa` enlace dentro del panel `Información`.
* `Mostrar Plan de Vuelo`, cuando se selecciona manualmente, o automáticamente después de cargar un plan de vuelo.
* Centrar un archivo KLM/KMZ de Google Earth KML/KMZ después de cargar

Esto permite una rápida inspección de un aeropuerto o radioayuda durante el vuelo. Para mostrar la aeronave de nuevo utilizar `Volver a posición mapa` o activar de nuevo `Mostrar Aeronave`.

#### ![Show Aircraft Trail](../images/icons/aircrafttrail.png "Show Aircraft Trail") Mostrar Trayectoria de la Aeronave {#show-aircraft-trail}

Muestra la trayectoria del avión del usuario. La trayectoria se muestra siempre independientemente de la distancia de zoom. Se guarda y se volverá a cargar al iniciar el programa.

La trayectoria se borra cuando se conecta al simulador de vuelo o bien puede borrarse manualmente seleccionado `Menú principal` -&gt; `Mapa` -&gt; `Borrar Trayectoria de Aeronave`. También se borra la trayectoria cuando la aeronave del usuario salta una gran distancia cuando se asigna un nuevo aeropuerto por ejemplo.

La longitud se limita por razones de rendimiento. Si excede de la longitud máxima, la trayectoria se parte y se pierden los segmentos antiguos.

#### ![Show Compass Rose](../images/icons/compassrose.png "Show Compass Rose") Mostrar la Rosa de los Vientos {#show-compass-rose}

Muestra la rosa de los vientos en el mapa el cual indica el norte verdadero y norte magnético. El rumbo y ruta de la aeronave se indican si está conectado el simulador.

La rosa se centra en la aeronave del usuario si está conectado. De lo contrario se centra en la vista del mapa.

Consultar [Rosa de los Vientos](COMPASSROSE.md) para más detalles.

#### ![Show AI and Multiplayer Aircraft](../images/icons/aircraftai.png "Show AI and Multiplayer Aircraft") ![Show AI and Multiplayer Ships](../images/icons/boatai.png "Show AI and Multiplayer Ships") Mostrar Aeronaves o barcos AI y Multijugador {#show-map-ai-aircraft}

Muestra las aeronaves o barcos multijugador en el mapa. Se pueden mostrar vehículos multijugador desde por ejemplo sesiones FSCloud, VATSIM or Steam.

El color y la forma del icono indican el tipo de aeronave y si esta está en tierra \(contorno gris\).

![AI or Multiplayer Aircraft](../images/icons/aircraft_small.png "AI or Multiplayer Aircraft") Aeronave AI o multijugador desde el simulador. Esto incluye aeronaves cargadas desde varias redes de clientes online. Un click en la aeronave o barco AI muestra más información en el panel  `Aeronave del simulador` dentro de la pestaña `AI / Multijugador`.

![Online Multiplayer Aircraft](../images/icons/aircraft_online.png "User Aircraft") Multiplayer aeronave/cliente desde una red online. Consultar [Redes Online](ONLINENETWORKS.md). Un click sobre la aeronave online  muestra información en el panel `Información` dentro de la pestaña separada `Clientes Online`.

Tenga en cuenta esto, en X-Plane, el tráfico de barcos no está disponible y la información IA es limitada.

Los vehículos mostrados están limitados por el sistema multiplayer utilizado si _Little Navmap_ no está conectado en una red online como VATSIM o IVAO. La aeronave multijugador desaparecerá dependiendo de la distancia respecto la aeronave del usuario. Para el AI en FSX o P3D esto actualmente está alrededor de 100 millas náuticas o 200 kilómetros.

Los barcos pequeños solo se generan por el simulador dentro de un radio pequeño alrededor de la aeronave del usuario.

_Little Navmap_ limita la visualización de los vehículos AI dependiendo de su tamaño. Hacer un zoom para ver las aeronaves o barcos pequeños.

En la distancia de zoom más baja, todos los aviones y barcos se dibujan a escala en el mapa.

Las etiquetas de las aeronaves se ven obligadas a mostrarse independientemente del nivel de zoom para las siguientes cinco aeronaves AI / multijugador más cercanas al usuario que estén a 20 millas de distancia y 5000 pies de altura.

Todos los iconos de las aeronaves pueden personalizarse: [Iconos de aeronaves AI y Multiplayer](CUSTOMIZE.md#customize-aircraft-icons).

#### ![Show Map Grid](../images/icons/mapgrid.png "Show Map Grid") Mostrar cuadrícula en el Mapa {#show-map-grid}

Muestra la cuadricula latitud/longitud así como el [meridiano](https://en.wikipedia.org/wiki/Prime_meridian) and [antimeridiano](https://en.wikipedia.org/wiki/180th_meridian) \(cerca de la línea de fecha\) en el mapa.

#### ![Show Country and City Names](../images/icons/cities.png "Show Country and City Names") Mostrar Nombre de Países y Ciudades {#show-country-and-city-names}

Muestra países, ciudades y otros puntos de interés. La disponibilidad de estas opciones depende del tema de mapa seleccionado. Consultar [Tema](MENUS.md#theme).

#### ![Show Hillshading](../images/icons/hillshading.png "Show Hillshading") Mostrar sombreado de alturas {#show-hillshading}

Muestra el sombreado de los relieves en el mapa. La disponibilidad de estas opciones depende del tema de mapa seleccionado. Consultar [Tema](MENUS.md#theme).

#### Proyección {#projection}

##### Mercator {#mercator}

La proyección plana proporciona un movimiento más fluido y nítido al usar temas basados en mapas en línea como _OpenStreetMap_ o _OpenTopoMap_.

##### Esférico {#spherical}

Muestra la tierra como un globo que es la proyección más natural. El movimiento puede parpadear ligeramente cuando se utiliza el mosaico de imágenes basado en temas de mapas en línea como _OpenStreetMap_ o _OpenTopoMap_. Use los temas del mapa `Simple`,`Plano` o `Atlas` para evitar esto.

Los mapa online pueden aparecer ligeramente borrosos cuando se utiliza esta proyección. Este es el resultado de convertir la imagen plana de mosaicos a una proyección esférica.

![Little Navmap Spherical projection and Simple Map Theme](../images/sphericalpolitical.jpg "Little Navmap Spherical projection and Simple Map Theme")

_**Imagen superior:** Mapa con proyección esférica con el tema de mapa  _`Simple`_ seleccionado._

#### Tema {#theme}

Tenga en cuenta que todos los mapas en línea se entregan desde servicios gratuitos, por lo tanto, no se pueden garantizar altas velocidades de descarga y alta disponibilidad. En cualquier caso, es fácil entregar e instalar un nuevo origen de mapa en línea sin crear una nueva versión _Little Navmap_. Consulte [Crear o agregar temas de mapa] (MAPTHEMES.md) para obtener más información.

##### OpenStreetMap {#openstreetmap}

Este es un mapa de trama online \(es decir, basado en imágenes\) que incluye una opción de sombreado de montañas. Tenga en cuenta que el sombreado de montañas _OpenStreetMap_ no cubre todo el mundo.

![OpenStreetMap and Hill shading](../images/osmhillshading.jpg "OpenStreetMap and Hill shading")

_**Imagen anterior:** Vista de un aeropuerto Italiano usando el tema OpenStreetMap theme con el sombreado de montañas._

##### OpenMapSurfer {#openmapsurfer}

La capa [OSM Roads](http://korona.geog.uni-heidelberg.de) proporcionada por [Heidelberg University](https://www.geog.uni-heidelberg.de/giscience.html). Este tema incluye un sombreado de montañas opcional disponible para el mundo entero.

Tenga en cuenta que la opción de sombreado de montañas de este tema está en fase experimental.

Los datos para este mapa son proporcionados por los contribuyentes © [OpenStreetMap](https://www.openstreetmap.org), renderizados por [GIScience Research Group @ Heidelberg University](https://www.geog.uni-heidelberg.de/giscience.html) y el estilo de mapa por Maxim Rylov.

[SRTM](http://srtm.csi.cgiar.org); ASTER GDEM es un producto de [METI](http://www.meti.go.jp/english/index.html) y [NASA](https://lpdaac.usgs.gov/dataset_discovery/aster/aster_policies).

![OSM Roads and Hill shading](../images/osmroad.jpg "OSM Roads and Hill shading")

_**Imagen superior:** Vista de un aeropuerto Italiano utilizando el tema  OpenMapSurfer theme y el sombreado de montañas._

##### OpenTopoMap {#opentopomap}

Un mapa de trama en línea que imita un mapa topográfico. Incluye sombreado de colinas y curvas de nivel de elevación a distancias de zoom bajas.

Los mosaicos para este mapa son proporcionados por [OpenTopoMap](https://www.opentopomap.org).

![OpenTopoMap](../images/otm.jpg "OpenTopoMap")

_**Imagen superior:** Vista de la parte oeste de los Alpes utilizando el tema OpenTopoMap. Aparece un plan de vuelo al norte de los Alpes._

##### Terreno Estambre {#stamen-terrain}

Un mapa del terreno con sombreado de montañas y colores de vegetación natural. El sombreado de montañas está disponible en todo el mundo.

Mosaicos del mapa de [Stamen Design](https://stamen.com), bajo [CC BY 3.0](https://creativecommons.org/licenses/by/3.0). Datos por [OpenStreetMap](https://www.openstreetmap.org), bajo [ODbL](https://www.openstreetmap.org/copyright).

![Stamen Terrain](../images/stamenterrain.jpg "Stamen Terrain")

_**Imagen superior:** Vista mostrando el tema terreno Estambre._

##### CARTO Clara {#carto-light} \(New in version 1.4.4\)

Un mapa muy brillante llamado *Positron* que permite concentrarse en las características de aviación en la visualización del mapa. El mapa incluye la misma opción de sombreado de montañas que el _OpenStreetMap_.

Mosaicos del Mapa y estilo por [CARTO](https://carto.com/). Data by [OpenStreetMap](https://www.openstreetmap.org), bajo [ODbL](https://www.openstreetmap.org/copyright).

##### CARTO Oscuro {#carto-light} \(New in version 1.4.4\)

Un mapa oscuro llamado *Dark Matter*. El mapa incluye la misma opción de sombreado de montañas que _OpenStreetMap_.

Mosaicos del Mapa y estilo por [CARTO](https://carto.com/). Datos por [OpenStreetMap](https://www.openstreetmap.org), bajo [ODbL](https://www.openstreetmap.org/copyright).

##### Simple \(Offline\) {#simple-offline}

Este es un mapa político con polígonos de países de color. Los límites y las masas de agua se representan gruesos. El mapa incluido en _Little Navmap_ tiene una opción para mostrar los nombres de ciudades y países.

##### Plano \(Offline\) {#plain-offline}

Un mapa muy simple. El mapa está incluido en _Little Navmap_ y tiene una opción para mostrar los nombres de ciudades y países. Los límites y las masas de agua se representan gruesos.

##### Atlas \(Offline\) {#atlas-offline}

Un mapa muy simple que incluye sombreado grueso y colores del terreno. El mapa está incluido en _Little Navmap_ y tiene una opción para mostrar los nombres de ciudades y países. Los límites y las masas de agua se representan gruesos.

### Menú de Biblioteca de Escenarios {#scenery-library-menu}

#### Simuladores de Vuelo {#flight-simulators}

Se crea un elemento de menú para cada instalación de Simulador de Vuelo o base de datos encontrada. Estos elementos de menú permiten el cambio de bases de datos en vuelo. El elemento del menú está deshabilitado si solo encontró un Simulador de Vuelo.

El ciclo de AIRAC se muestra solo en X-Plane ya que la información no está disponible para los simuladores FSX o P3D.

**Tiene que configurar primero la ruta base del directorio de X-Plane en**`Diálogo de Carga de la Biblioteca de Escenarios`** para activar la opción de menú para X-Plane.**

Este menú se sincroniza con la selección del simulador en [Diálogo de Carga de la Biblioteca de Escenarios](SCENERY.md#load-scenery-library-dialog). Una vez que una base de datos se carga con éxito, la pantalla, el plan de vuelo y la búsqueda cambiarán a los datos del simulador recién cargados.

**Tenga en cuenta que el programa no evita que utilice una base de datos de escenarios de X-Plane mientras está conectado a FSX / Prepar3D o viceversa. Obtendrá efectos no deseados como información meteorológica incorrecta si utiliza dicha configuración.**

El programa puede cambiar un plan de vuelo cargado si cambia entre diferentes bases de datos. Esto puede suceder si se establece una posición de salida en el plan que no existe en la otra base de datos. Haga clic en `Nuevo plan de vuelo` antes de cambiar para evitar esto.

#### Navigraph {#navigraph}

Este submenú también indica que el ciclo de AIRAC se agrega si se encuentra una base de datos de Navigraph en el directorio de la base de datos.

Consulte el capítulo [Bases de datos de navegación](NAVDATA.md) para obtener más información sobre estas bases de datos y los tres modos de visualización diferentes que se muestran a continuación.

##### Usar Navigraph para todas las características {#navigraph-all}

Ignora completamente la base de datos del simulador y toma toda la información de la base de datos de Navigraph.

##### Usar Navigraph para Radioayudas y Procedimientos {#navigraph-navaid-proc}

Este modo combina las radioayudas y más de la base de datos de Navigraph con la base de datos del simulador. Esto afecta a la visualización del mapa, toda la información y todas las ventanas de búsqueda.

##### No Usar la Base de Datos de Navigraph {#navigraph-none}

Ignora la base de datos de Navigraph y muestra solo la información leída desde los escenarios del simulador.

#### Mostrar Archivos de Base de Datos {#show-database-files}

Abra el directorio de la base de datos de _Little Navmap_ en un explorador de archivos. Consulte [Ejecutar sin una instalación de Simulador de Vuelo](RUNNOSIM.md#running-without-flight-simulator-installation) para obtener más información sobre cómo copiar archivos de bases de datos entre diferentes ordenadores. Esto permite que _Little Navmap_ se ejecute en un ordenador remoto \(por ejemplo, Windows, Mac o Linux \) utilizando la misma base de datos que se creó en el ordenador que ejecuta el simulador de vuelo.

#### ![Load Scenery Library](../images/icons/database.png "Load Scenery Library") Cargar Biblioteca de Escenarios {#load-scenery-library}

Abrir el diálogo `Cargar la Librería de Escenarios`. Consultar [Diálogo de Carga de Biblioteca de Escenarios](SCENERY.md#load-scenery-library-dialog) para obtener más información. Este elemento del menú está desactivado si no se encuentran instalaciones de simulador de vuelo.

#### ![Copy Airspaces to X-Plane Database](../images/icons/airspacecopy.png "Copy Airspaces to X-Plane Database") Copiar Espacios Aéreos a la base de datos de X-Plane {#copy-airspaces-to-xplane}

Copia la información del espacio aéreo desde una base de datos de FSX o P3D a una base de datos X-Plane. Esto es necesario ya que X-Plane viene con información limitada del espacio aéreo.

Todos los espacios aéreos y cargados desde X-Plane se borran antes del copiado. Consultar [Espacios Aéreos de X-Plane](SCENERY.md#load-scenery-library-dialog-xp-airspaces) para obtener más información.

Primero debe cambiar a una base de datos del simulador FSX o P3D para habilitar este elemento del menú.

La información del espacio aéreo se elimina al volver a cargar la base de datos de X-Plane. Por lo tanto, debe copiar los espacios aéreos nuevamente después de volver a cargar.

### Menú Datos de Usuario {#userdata-menu}

Consultar [Waypoints definidos por el usuario](USERPOINT.md) para obtener más información sobre waypoints definidos por el usuario.

#### Mostrar Búsqueda {#userdata-menu-show-search}

Despliegue la ventana del panel `Búsqueda` y la pestaña` Puntos de Usuario` donde puede editar, agregar eliminar y buscar waypoints definidos por el usuario.

#### Importar CSV {#userdata-menu-import-csv}

Importa un archivo CSV que sea compatible con el formato ampliamente utilizado desde Plan-G y agregue todo el contenido a la base de datos.

Tenga en cuenta que el formato CSV es el único formato que permite escribir y leer todos los campos de datos admitidos.

Consultar [Formato de Datos CSV](USERPOINT.md#userpoints-csv) para obtener una descripción más detallada.

#### Importar user_fix.dat de X-Plane {#userdata-menu-import-user-fix}

Importa waypoints definidos por el usuario desde el archivo `user_fix.dat`. El archivo por defecto en X-Plane y tiene que crearse ya sea manualmente o exportándolo desde _Little Navmap_.

La localización por defecto es `XPLANE/Custom Data/user_fix.dat`.

Los puntos de usuario importados son del tipo `Waypoint` ![Waypoint](../images/icons/userpoint_Waypoint.png "Waypoint") los cuales pueden ser modificados utilizando la funcionalidad de edición en masa.

El formato está descrito por Laminar Research aquí: [XP-FIX1101-Spec.pdf](https://developer.x-plane.com/wp-content/uploads/2016/10/XP-FIX1101-Spec.pdf).

Consultar [Formato de Datos user_fix.dat de X-Plane](USERPOINT.md#userpoints-xplane) para obtener más información.

#### Importar GTN de Garmin {#userdata-menu-import-garmin-gtn}

Lee waypoints definidos por el usuario desde el archivo `user.wpt` de Garmin. Consulte el manual de la unidad Garmin que está utilizando para obtener más información sobre el formato y la ubicación del archivo.

Los puntos de usuario importados son del tipo `Waypoint` ![Waypoint](../images/icons/userpoint_Waypoint.png "Waypoint") los cuales pueden ser modificados utilizando la funcionalidad de edición en masa.

Consultar [Formato de Datos user.wpt de Garmin](USERPOINT.md#userpoints-garmin) para obtener más información.

#### Exportar CSV {#userdata-menu-export-csv}

Crea o anexe waypoints definidos por el usuario a un archivo CSV. Un cuadro de diálogo pregunta si solo se deben exportar los puntos de usuario seleccionados y si los puntos de usuario deben anexarse a un archivo ya presente.

Tenga en cuenta que el archivo exportado contiene una columna adicional `Región` en comparación con el formato Plan-G. El campo de descripción admite más de una línea de texto y caracteres especiales. Por lo tanto, no todos los programas pueden importar este archivo. Si es necesario, adapte los puntos de referencia definidos por el usuario.

#### Exportar user_fix.dat de X-Plane  {#userdata-menu-export-user-fix}

Solo se pueden exportar los puntos de usuario seleccionados o todos. Los datos exportados pueden adjuntarse opcionalmente a un archivo ya presente.

No todos los campos de datos se pueden exportar a este formato. El campo de identificación es requerido para exportar.

Además, debe asegurarse de que el identificador de punto de referencia del usuario sea único dentro de `user_fix.dat`.

Consultar [Limitaciones del formato user_fix.dat de X-Plane](USERPOINT.md#userpoints-xplane) para obtener más información sobre las limitaciones.

#### Exportar GTN de Garmin {#userdata-menu-export-garmin-gtn}

Solo se pueden exportar los puntos de usuario seleccionados o todos. Los datos exportados pueden adjuntarse opcionalmente a un archivo ya presente.

No todos los campos de datos se pueden exportar a este formato. El campo de identificación es requerido para exportar.
Algunos campos como el nombre están adaptados a las limitaciones.

Consultar [Formato de Datos user_fix.dat de X-Plane](USERPOINT.md#userpoints-xplane) para obtener más información sobre las limitaciones.

#### Exportar XML de FSX/P3D BGL Compilado {#userdata-menu-export-bgl}

Esta opción de exportación crea un archivo XML que se puede compilar en un archivo BGL que contiene waypoints.

Los campos de región e identificación son necesarios para esta opción de exportación.

Consulte la documentación de Prepar3D SDK para obtener información sobre cómo compilar el BGL y cómo agregarlo al simulador.

#### Crear entradas al Libro de Registro Logbook {#userdata-menu-create-logbook}

Seleccionando esta opción de menú se activa la característica simple de logbook.

_Little Navmap_ creará el punto de usuario tipo `Logbook` ![Logbook](../images/icons/userpoint_Logbook.png "Logbook") en cada despegue y aterrizaje cuando esté conectado al simulador.

Estas dos entradas del libro de registro contienen toda la información disponible, como el plan de vuelo, el tiempo, el combustible consumido y mucho más.

#### Borrar Base de Datos {#userdata-menu-clear-database}

Elimina de la base de datos todos los los waypoints definidos por el usuario.

Un archivo CSV de backup llamado `little_navmap_userdata_backup.csv` se crea en el directorio de ajustes `C:\Users\SUNOMBREDEUSUARIO\AppData\Roaming\ABarthel` antes de borrar todos los waypoints definidos por el usuario.

_Little Navmap_ además crea una copia de seguridad completa de la base de datos en cada arranque. Consultar [Archivos](FILES.md#userdata).

### Menú Herramientas {#tools-menu}

#### ![Flight Simulator Connection](../images/icons/network.png "Flight Simulator Connection") Conexión con el Simulador de Vuelo {#flight-simulator-connection}

Abre el diálogo `Conectando` que permite a _Little Navmap_ conectar directamente al Simulador de Vuelo con el plugin para X-Plane *Little Xpconnect*, o remotamente usando el agente [Little Navconnect](https://albar965.github.io/littlenavconnect.html). Consultar [Conectar al Simulador de Vuelo](CONNECT.md#connecting-to-a-flight-simulator) para obtener más información.

#### Reiniciar todos los mensajes {#reset-all-messages}

Vuelve a habilitar todos los cuadros de diálogo que se inhabilitaron seleccionando `No mostrar este cuadro de diálogo` o mensajes similares.

#### ![Options](../images/icons/settings.png "Options") Opciones {#options}

Abre el cuadro de diálogo [Opciones](OPTIONS.md#options-dialog).

### Menú Ventana {#window-menu}

#### Sobreimpresión de Mapas {#map-overlays}

Muestra u oculta las superposiciones de mapas flotantes, como la vista general en la esquina superior izquierda o la brújula en la esquina superior derecha de la ventana del mapa.

#### ![Search](../images/icons/searchdock.png "Search") Búsqueda {#search}

#### ![Flight Plan](../images/icons/routedock.png "Flight Plan") Plan de Vuelo {#flight-plan}

#### ![Information](../images/icons/infodock.png "Information") Información {#information}

#### ![Flight Plan Elevation Profile](../images/icons/profiledock.png "Flight Plan Elevation Profile") Perfil de Elevación Plan de Vuelo {#flight-plan-elevation-profile}

#### ![Simulator Aircraft](../images/icons/aircraftdock.png "Simulator Aircraft") Aeronave del Simulador {#simulator-aircraft}

#### ![Legend](../images/icons/legenddock.png "Legend") Leyenda {#legend}

Abre y cierra estos paneles. El panel de mapa no se puede cerrar.

#### Menú Principal, Barra de Herramientas del Mapa, Barra de Herramientas de Espacios Aéreos, Barra de Opciones de Mapa, Barra de Plan de Vuelo, Barra de Paneles, Barra de Estado {#main-toolbar-options}

Muestra u oculta estas barras de herramientas y la barra de estado.

#### Reiniciar Diseño de Ventana {#reset-layout}

Restablece el diseño las ventanas a su valor predeterminado. Esto implica visibilidad, posición y estado de todas las ventanas, así como las barras de herramientas. Esta función puede ser útil si se pierde una ventana en configuraciones de monitores múltiples.

### Menu Ayuda {#help-menu}

#### ![Contents \(Online\)](../images/icons/help.png "Contents \(Online\)") Contenidos \(Online\) {#help-contents}

Muestra el manual de usuario online en el explorador predeterminado.

#### ![Contents \(Offline, PDF\)](../images/icons/help.png "Contents \(Offline, PDF\)") Contenidos \(Offline, PDF\) {#help-contents-offline}

Muestra el manual PDF incluido en el visor PDF por defecto.

#### ![NavMap Legend](../images/icons/help.png "NavMap Legend") Leyenda del NavMap {#navmap-legend-map-legend}

Muestra la leyenda del mapa relacionada con la navegación en el panel `Leyenda`. También puede acceder a la leyenda desde aquí: [Leyenda Navmap](LEGEND.md).

#### ![Map Legend for current Map Theme](../images/icons/help.png "Map Legend for current Map Theme") Leyenda del Mapa para el Tema Actual {#navmap-legend-map-legend}

Muestra la leyenda del mapa dependiendo del tema de mapa en el panel `Leyenda`. Tenga en cuenta que la leyenda no está disponible para todos los temas de mapa.

#### ![About Little Navmap](../images/icons/littlenavmap.png "About Little Navmap") Acerca de Little Navmap {#about-little-navmap}

Mostrar la versión y el número de revisión de _Little Navmap_, también contiene enlaces al directorio de la base de datos, al archivo de configuración, al archivo de registro y a la dirección de correo electrónico del autor.

#### ![About Marble](../images/icons/marble.png "About Marble") Acerca de Marble {#about-marble}

Muestra información sobre [Marble widget](https://marble.kde.org) el cual es usado para descargar y mostrar los mapas.

#### ![About Qt](../images/icons/qticon.png "About Qt") Acerca de Qt {#about-qt}

Muestra información sobre [Qt application framework](https://www.qt.io) que se usa en _Little Navmap_.

#### ![Donate for this Program](../images/icons/about.png "Donate for this Program") Donar para este Programa {#donate}

Abre la página web de donación en su navegador predeterminado.

Si desea mostrar su agradecimiento, puede donar utilizando PayPal.

Las donaciones son puramente opcionales pero muy apreciadas.

#### ![Check for Updates](../images/icons/revert.png "Check for Updates") Chequear actualizaciones {#check-updates}

Permite verificar manualmente las actualizaciones. Esto también mostrará actualizaciones que fueron ignoradas recientemente al presionar 'Ignorar esta actualización' en el cuadro de diálogo de notificación.

Consultar [Chequear actualizaciones](UPDATE.md) para obtener más información.

## Barra de Estado {#statusbar}

La barra de estado en la parte inferior de la ventana principal muestra varias indicaciones \(de izquierda a derecha \):

* Última acción o ayuda rápida que explica un elemento del menú o un botón de la barra de herramientas.
* Estado de conexión para una conexión local o remota. La información sobre herramientas proporciona más detalles sobre el estado, como el nombre de host para conexiones remotas.  
  * `Conectando ...`: El programa está intentando establecer una conexión que se inició de forma manual o automática.
  * `Conectado`: se estableció una conexión.
  * `Desconectado`: el simulador o _Little Navconnect_ se desconectó.
* Indicador que muestra los tipos de aeropuertos, espacios aéreos, radioayudas o vehículos de IA actualmente visibles en el mapa. La información sobre herramientas proporciona más detalles.
  * Se mostrará un mensaje de advertencia rojo `Demasiados objetos` si se muestran demasiados objetos en el mapa debido a un nivel de detalle demasiado alto. La visualización del mapa estará incompleta si esto sucede.
  * Se mostrará un mensaje rojo de `Base de datos vacía` si la base de datos seleccionada actualmente no tiene contenido y necesita ser cargada.
* Nivel de detalle del mapa. El rango es -5 para el mínimo de detalles a +5 para el máximo de detalles.
* Indicador de progreso de descarga de mapas en línea. Esto muestra el estado de la descarga del mapa actual. El texto tiene un prefijo rojo con una indicación de `Fuera de línea` si el modo fuera de línea está habilitado.
  * `Listo.`: Todos los datos del mapa se cargaron con éxito.
  * `Esperando datos ...`: los datos del mapa faltan en el caché y se solicitó la descarga. Esperando ahora respuesta.
  * `Esperando actualización ...`: los datos del mapa ya están cargados pero caducaron después de dos semanas. Esperando nuevos datos después de solicitar una actualización.
  * `Incompleto`: Descarga fallida. Tenga en cuenta que el indicador de progreso puede parecer que está detenido en el mensaje `Esperando datos ...` si no hay sombreado disponible para una región _OpenStreetMap_ o si el zoom es demasiado cercano cuando usa ciertos mapas en línea.
* Distancia de zoom \ (distancia del punto de vista a la superficie de la tierra \) en millas o kilómetros náuticos.
* Posición del cursor en el mapa como latitud y longitud dependiendo de la unidad seleccionada en el diálogo `Opciones`.
  * Elevación del suelo debajo del cursor después de un breve retraso si se selecciona la información de elevación fuera de línea [GLOBE] (https://ngdc.noaa.gov/mgg/topo/globe.html).
  * Variación magnética en la posición del cursor en grados Oeste o Este.
* Fecha actual del mes y hora zulú/UTC `horas: minutos: segundos`. Este es el tiempo del mundo real y no el tiempo del simulador. La información sobre herramientas proporciona más información de fecha y hora.

![Statusbar](../images/statusbar.jpg "Statusbar")

_**Imagen superior:** Barra de estado de la versión 1.8.5 con un mensaje de la última acción en el lado izquierdo \(_`Opciones Cambiadas.`_\), el estado de la conexión y la información sobre las herramientas que indica cual se muestra actualmente en el mapa. Se muestran todas las características del mapa. El nivel de detalle del mapa no se modifica y las coordenadas del mapa se muestran en la parte inferior derecha. La altitud en el cursor también se muestra ya que los datos de elevación están instalados. La barra de progreso de descarga de mapas online muestra _`Hecho.`_ indicando que todos los mosaicos del mapa se han descargado. La distancia de Zoom es de 7.8 millas náuticas._

