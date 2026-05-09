# -*- coding: utf-8 -*-
# This file contains metadata for your plugin.

# This file should be included when you package your plugin.# Mandatory items:

[general]
name=JCCM Carreteras
qgisMinimumVersion=3.4.11
qgisMaximumVersion=3.40.99
description=JCCM. Herramienta de gestion de Carreteras y datos catastrales
version=3.02
author=Agustín Solabre Suárez / DIRECCIÓN GENERAL DE CARRETERAS
email=gis.carreteras@jccm.es
telephone=967-558141
organizacion=DIRECCIÓN GENERAL DE CARRETERAS

about=Barra de herramientas de Carreteras para Direccion General de Carreteras. Consejeria de Fomento. Junta de Comunidades de Castilla-La Mancha
    - Herramientas de gestión e información pública de carreteras de castilla la Mancha
    - Herramientas de carga, información, gestión e información de Catastro de España
    - Gestión de los ficheros GML de Catastro
    - Herramientas para el manejo avanzado de expdientes de expropiaciones
    - Buscadores avanzados
    - Incorpora plugins mejorados de acceso a ruteo, google street, o catálogos de capas propias de la JCCM
    
    Roads Toolbar for the Directorate General of Roads. Regional Government of Castilla-La Mancha
    - Road management and public information tools for Castilla-La Mancha
    - Tools for loading, information, management and information of the Spanish Cadastre
    - Management of Cadastre GML files
    - Tools for the advanced management of expropriation files
    - Advanced search engines
    - It incorporates improved plugins for accessing routing, Google Street View, and catalogs of layers specific to the JCCM (Regional Government of Castilla-La Mancha).

tracker=http://bugs
repository=http://repo
# End of mandatory metadata

# Recommended items:

hasProcessingProvider=no

# Tags are comma separated with spaces allowed
tags=roads, carreteras, gml, catastro, expropiaciones, finder, cartociudad,

# Uncomment the following line and add your changelog:
changelog=
    CAMBIOS ENTRE VERSIONES
    -----------------------------------
    3.02a
        * Mejoras de usuario en herrDP_informes_invasionDP.py, activa o no el botón CARGAR, si las parcelas ya están (7/5/26)
    3.02
        * Cambios de estructura de código en herrDP_informes_invasionDP.py, se corrigen errores de interpretación de TIPO_INVASION y otros (16/3/26)
        * Mejoras de la herramienta de gestor de Informes de Expropiaciones, corrección de Bugs (16/3/26)
        * El sistema hace una copia de la HOJA DE CÄLCULO de informes, siempre que se pretenda modificar un registro, y la puede restaurar
            si hay problemas (19/3/26)
        * La asignación de expediente en herrDP_informes_invasionDP.py se puede hacer por el último directorio o por el valor más alto del excel (19/3/26)
        * Se introduce la variable en config, de la LISTA EXPEDIENTES EXPROPIACIONES del GPKG, para que sean empleados estos datos como oficiales para diferentes herramientas (22/3/26)
        * Combo desplegable en herrDP_GDBinf_colindancia.py desde LISTA EXPEDIENTES EXPROPIACIONES, que trasladn datos a INFORMES EXPROPIACIONES (22/3/26)
        * Solución de diferentes BUGs en herrDP_GDBinf_colindancia.py, herrDP_informes_invasionDP.py y jccm_bar_config.py (22/3/26)
        * Se ponen verde o rojo la opción ZOOM A ELEMENTO, si existe o no feature en el GPKG (23/3/26)
    3.01
        * Mejoras en el buscador cartociudad por PKs. Ahora puede cargar un tramo entero de PPKK y es algo más segura la busqueda (10/3/26)
        * Se implementa una nueva herramienta en el menú EXPROPIACIONES (8/3/26)
            - Gestión de BD de INFORMES DE COLINDANCIA Y EXPROPIACIONES
            - TODA LA GESTIÓN DE INFORMES DE EXPROPIACIONES/COLINDANCIA DE DP PASA A GESTIONARSE VÍA UNA EXCEL,
                anteriormente se gestionaba por medio de access a través de un fichero texto de intercambio
                en la BD del Servicio Provincial de Carreteras de la JCCM, pero se tiende a liberar la acción vía access.
                Se mantiene VIGENTE el sistema de exportación a la BD ACCESS
        * Modificamos herrDP_informes_invasionDP.py para aceptar nueva entrada ART_LEY y las mejoras del sistema EXCEL de Inf.col. (12/3/26)
    2.20
        * Cambios de la búsqueda cartociudad, ahora permite hacerlo según tipos de búsqueda con estilos propios y en capas diferenciadas (3/3/26)
        * Pequeños arreglos en config (5/3/26)
    2.19
        * Modificaciones en el jccm_bar_config.py y en el herrExpro_copyfiles.py, para poder hacer copias directas del fichero de expropiaciones (o el que sea) a otros dir (18/2/26)
        * Eliminación de condiciones con NULL en determinadas partes de functions3.py (colaboración de IGNACIO ROMERO) (18/2/26)
        * Arreglos y mejoras del jccm_bar_config.py, coherencia de variables, colores (20/2/26)
            TODO No funciona bien el acceso al directorio de los selectores de ficheros
        * Pequeños arreglos en herrDP_informes_invasionDP.py (20/2/26)
        * Ahora los informes de expropiaciones, se guardan si existe en un excel, además de la exportación a DBF (20/2/26)
        * Resuelto pequeño error de redondeo en los GML (23/2/26)
    2.18
        * Arreglos en el config y en herrDP_informes_invasionDP.py, para mejorar la configuración de la aplicacion para los cálculos de INVASIÓN (15/2/26)
        * El menú config ahora se puede llamar por posición de pestaña o nombre (14/2/26)
        * Se mejora la herramienta de copia de seguridad (16/2/26)
    2.17
        * Resuelto un problema del zoom de buscador de tramos (19/1/26)
        * Pequeño bug en herrCTRAS_descargasAPI.py al configurar fichro de salida (29/01/26)
        * Se corrigen capas desde la antigua W: a carga vía WMS (30/01/26)
            * JCCM VIAS PECUARIAS
            * JCCM SISTEMA INFORMACIÓN URBANA
		* SE mejora la carga de grupos en gestorCapas.py para por defecto cogerlos desde la instalación del plugin (31/01/26)
		* Arreglos en en jccm_bar3.py para depurar herramientas obsoletas (12/02/26)
    2.16
        * Cada botón devuelve el cursor al general en caso de error (14/1/26)
        * En jccm_buscadorGeneral.py se resuelve un problema de poblaciones con igual nombre (14/1/26)
        * En jccm_buscadorGeneral.py se resuelve el caso de que el combo de coordenadas está vacio (15/1/26)
    2.15
        * Se añade una herramienta en el menú de expropiaciones de creación de campos según un estructura (18/10/25)
        * Modificación para simplificar catastro_generaGML.py (20/11/25)
            * Creación más simplificada del GML solo con campos localid y namespace
            * Posibilidad de modificar decimales para AREAVALUE y COORDENADAS
            * Se eliminan nodos duplicados
        * Arreglos generales en functions3.py y jccm_bar3.py (22/10/25)
        * Herramientas en pruebas de lectura de BBDD ACCESS herrExpro_controlCalidadGDB.py -PRUEBAS- (10/12/25)
        * En catastro_generaGML.py se meten varios controles, localid reptidos y de geometría idéntica
        * El GML ahora admite namespace tipo 'ES.SDGC.BU' para Building (14/1/26)

    2.14
        * Pequeña corrección en herrExpro_INFOEXPTES.py de texto 'REMIS. ' a 'REMISIÓN ' (28/7/25)
        * Nueva herramienta herrEXPRO_creaCamposExpro.py para Crear Campos de Datos de Expropiaciones (29/7/25)
        * Se añaden comentarios a todos los campos en las capas de parcelas catastrales (31/7/25)
        * Se añade el dato PARAJE  a las capas de catastro (31/7/25)
        * En catastroCargaMasiva.py, el nombre se obtiene del de la capa/tabla, se añaden contadores (18/8/25)
        * En catastroCargaMasiva.py, se mejora la botonera con colores si se puede o no usar (22/8/25)
        * En catastro_cargaXMLmasiva.py se arreglan y añaden comentarios a los campos de catastro (21/8/25)
        * Se lleva la definiciónde estructura de campos de capas catastrales a CONFIG.PY`para unificar
            las estructuras de capas catastrales de todo tipo a la de la CONSULTA MASIVA (24/8/25)
            https://www.catastro.hacienda.gob.es/ayuda/masiva/Descripcion_consulta_masiva_datos_Catastrales.pdf
        * Migración a QGIS 3.40.10 BRATISLAVA
    2.13
        * Implementados nuevos iconos de carreteras (28/2/25)
        * herrCTRAS_AFOROS.py Nueva herramienta de visualización de mapas AFOROS en PDF (28/2/25)
        * Se mete en el config la variable file_AFOROS (1/3/25)
        * Nuevos iconos de funcionalidades de carreteras y expropiaciones (4/3/25)
        * Se duplica la herramienta herrDP_informes_invasionDP.py, para permitir añadir expediente sin analizar intersección (7/3/25)
        * En herrDP_informes_invasionDP.py, se añade un TEXTO INFORME automático en función de TIPOinforme (7/3/25)
        * Se modifica la dirección de variables absolutas de usuario, de \JCCM_carreteras\ a \jccm_bar3\ (7/3/25)
            TODO: METER UNA FUNCIÓN DE MIGRACIÓN EN SETTINGS
        * En herrCTRAS_AFOROS.py, los datos seleccionados van a variables de usuario /last/ (11/3/25)
        * Se crea una herramienta para asignar atributos de parcela catastral a parcela pinchada (21/3/25)
        * Se modifica la herramienta jccm_puntoZ.py para que se coloquen los datos en un dock flotante (25/3/25)
        * jccm_puntoZ.py se ponen Prov y Muni desde datos catastro (25/3/25)
        * Resuelto problema en PK_maptool.py de consulta en GPKG siempre que no daba resultados por URL (29/3/25)
        * Se resuelven algunos errores catastrales, cuando el PROYECTO no tiene configurado un CRS (3/4/2025)
        * En PK_INFO se transforma el cuadro de dialogo a panel flotante, permitiendo ver el Pk para cada click (6/4/25)
        * Pequeñas mejoras en la intersección por INVASIÓN DE PARCELA en herrDP_informes_invasionDP.py > intersectParcelas, caso multipoligono (13/4/25)
        * Resuelto pequeño error en ASIGNAR TIPO EXPEDIENTE al dar error en poligToPKINIPKFIN (14/4/25)
        * Se modifica catastro_generaGML.py para aumentar la precisión del GML a 3 decimales (24/4/25)

    2.12
        * SE HACE UN CAMBIO GLOBAL PARA INTEGRAR FUNCIONAIDADES EN EL PLUGIN 'catastroesp' 'CATASTRO DE ESPAÑA'
            * Globalización de iconos y menús (16/2/25)
            * Modificación de funciones showJCCMessage a showMessage (16/2/25)
            * Integración de herramientas 'catastro' desde 'catastroesp'
                *  (16/2/25)
            * Herramienta de carga de capas de AFOROS (22/2/25)
            * CAMBIOS DE LIBRERÍAS EN functions3.py PARA HOMOLOGARLAS A LA INSTALACIÓN DE QGIS(23/2/25)
                # Sustituimos librería PyQt5.QtGui por qgis.PyQt.QtGui
                # Sustituimos librería PyQt5.QtCore por qgis.PyQt.QtCore
                # Sustituimos librería PyQt5.QtWidgets por qgis.PyQt.QtWidgets
            * En herrCTRAS_AFOROS.py, se añade la clase EtiquetaFija(QgsMapCanvasItem), para colocar unna etiqueta fija con el año
                cuando se cargan las capas de aforos
    2.11
        * Nueva herramienta de descarga de capas herrCTRAS_descargasAPI.py para crear GDB offline(24/12/24)
        * Pequeño arreglo para que catastro_generaGML.py solo seleccione campos 'string' (14/01/25)
        * Pequeño arreglo para resolver el problema del panel de info adicional que no enguentra la GDB PK_info_dialog.py/fun.buscaUnidadesGDB(28/1/25)

    2.10
        * Se adaptan GDBDominios.py, herrCTRAS_controlCalidadGDB.py, herrCTRAS_catalogo.py, herrCTRAS_catalogoRT.py,
            para el nuevo valor 'Tipologia_DobleC' = 'MTC' (16/12/24)
        * Se inician herrCTRAS_migracionPKSaRT.py y herrCTRAS_migracionEJESaRT.py (16/12/24)
        * Se adapta la exportación de GML de catastro al nuevo formato V4 de INSPIRE (18/12/24)
    2.09
        * Arreglos de herrCTRAS_catalogoRT.py
            - Se ordenan por 'nombre' las carreteras "id_Vial = '608xxxxxxxxx' y titular = 2" erróneas (6/12/24)
            - Se revisan ciertas estructuras de funcionamiento para que analice otras redes
            - Añadida una carga de elementos desde cartociudad de las entradas de catalogo RT erróneas (8/12/24)
            - Se separan por completo las herramientas RT en jccm_bar3.py (14/12/24)
            - Se crea RT_maptool.py y el menú RT_info.ui para el identificadr de datos WMS de RT(14/12/24)
    2.08
        * Nueva herramienta de depuración de cuñas en polígonos (13/11/24)
        * Pequeñas depuraciones sintácticas de caracter general en todos los Plugins (15/11/24)
        * Nuevo identificador de carretera contra datos IGN RT (Red de Transportes INSPIRE) (26/11/24)
        * Nueva herramienta de generación de Catalogo de carreteras en formato RT, CON EXCEL (literal) (30/11/24)
        * Se migra la herramienta 'Listado de coordenadas de un polígono' a las herramientas de catastro (4/12/24)
            - Se mantiene otro botón idéntico en las herramientas de carreteras
        * Se crea un grupo de herramientas en la botonera, respecto de la capa RT (4/12/24)
        * Se incorpora una nueva herramienta de CARGA MASIVA DE PARCELAS CATASTRALES -SIMILAR AL BUSCADOR- (4/12/24)
    2.07
        * Se resuelve un problema de la creación de un directorio, caso de no existir, en diferentes funcionalidades (10/8/24)
            - Se crea la funcionalidad fun.comprobarDirectorio
        * Pequeños arreglos en el menún PK_maptool, y PK_maptoolFICH (8/10/24)
        * Conseguimos poner arriba de la TOC los grupos en gestorCapas.py y herrExpro_cargacapas.py (10/10/24)
        * Resolvemos las prevalencias de TIPO_EXPEDIENTE ='INVASION' (10/10/24)
        * Mejoramos cartoc_buscadorGeneral.py para que cargue las geometrías buscadas en una capa (11/10/24)
        * Se añaden opciones de borrado de capas y marcas (13/10/24)
        * Se añade en CATATRSO herramienta desde modelo de CorrectorDeCapasDePoligonos.py (14/10/24)
        * El atom de descarga de catastro por municipios cambia de dirección  (15/10/24)
            DONDE DECÍA: 'http://www.catastro.minhap.es/INSPIRE/{tipoD}/{prov}/ES.SDGC.{codD}.atom_{prov}.xml'.format(tipoD=tipoDESC, codD=codDESC, prov=cp)
            DEBE DECIR:  'https://www.catastro.hacienda.gob.es/INSPIRE/{tipoD}/{prov}/ES.SDGC.{codD}.atom_{prov}.xml'.format(tipoD=tipoDESC, codD=codDESC, prov=cp)
        * Se añade en HERREXPRO herramienta desde modelo de herrExpro_CalculaReparcelacionParaGml.py (16/10/24)
        * Se resuelve un problema con la RC14 de la parte invadida en herrDP_informes_invasionDP.py (17/10/24)
        * Se rehacen enlaces a datos de ZONAS INUNDABILIDAD (2/11/24)
    2.06
        * Inicio Migración a QGIS 3.34 (15/9/24)
        * Se mejoran ciertas cuestiones de la creación y estado de la botonera -hundidos- (17/9/24)
        * Se consigue hacer funcionar de nuevo herrCTRAS_descargas.py, tanto desde la funcionalidad
            de descargas, como desde la identificación de PK (20/9/24)
            Falla la carga de valor M
        * El BUSCADOR GENERAL ahora admite buscar CTRA, PK, DISTEJE (23/9/24)
            TODO El caso CTRA, PK, [disteje] solo funciona en tipo_consultaCAPA = 'url'
        * En diferentes scripts se homogeiniza self.setVar o Qsettings() con self.qs (25/9/24)
            jccm_buscadorGeneral.py, jccm_bar3.py, herrExpro_creaGMLExpteEXPRO.py, herrExpro_creaExpteEXPRO.py, catastro_generaGML.py
        * Mejorados los datos de info de menús 'about_dialog.py' y 'jccm_bar_config.py' (26/9/24)
        * PARECE TERMINADA LA TRANSICIÓNA 3.34 (27/9/24)
        * En MACRO_INICIO.py Cambia configparser.SafeConfigParser() por configparser.ConfigParser() (01/10/24)
        * Se eliminan errores de indentacion de herrDP_informes_invasionDP.py (01/10/24)

    2.05
        * Se crea una herramienta herrCTRAS_DATOSfromXY.py, similar a herrCTRAS_CAPAfromXY.py que asigna valors CTRA, PK, DIST, ACIMUT, XE YE, XP YP
          calculados dentro de la tabla (2678/24)
        * Se añade una funcionalidad de CALCULADORA DE RUTAS a partir del plugin mejorado del repositorio de QGIS. (6/9/24)
            AUTOR ORIGINAL: 2018 by Mehmet Selim BILGIN https://github.com/MSBilgin/OnlineRoutingMapper
    2.03
        * Se estudia el calculo de herrCTRAS_CAPAfromCTRAPKS teniendo en cuenta distancia al eje en elementos lineales (16/7/24)
            Esto retoca:
                herrCTRAS_CAPAfromCTRAPKS.py (mostrarEventos)
                jccm_buscadorGeneral.py (goToTRAMO_clicked) TODO
                functions3.py (mostraEventosFromCSVLayer, addEventoLineal, getTramoCtra, se crea desplazaEje)
        * Añadido un contador en el buscador de parcelas desde tabla o fichero (4/8/24)
        * Se mejoran ciertas funciones de carga de parcela catastral en caso de parcla DESCUENTO
            f.cargarCapaParcelaCatastral (6/8/24)
        * Se mete un contador de parcelas en el buscador esencialmente para la carga múltiple desde capa (7/8/24)
        * Se resuelve un pequeño error con el bbox de algunas parcelas al hacer zoom en buscadorCatastral (7/8/24)
    2.02
        * Se meten campos DIRECCION, PROVINCIA, REF_CAT, COD_INE en tabla de parcelas (8/6/24)
        * Se deshace el tema del SRS en PK_maptool.py (sigue sin cambiar el EPSG bien) (06/05/24)
        * Hay algún problema de suma de superficies en el supTOTAL de fun.consultaCatastroDATPARCELA, se reseulve en la carga del GML (06/05/24)
    2.01
        * Resuelto un pequeño error de srs en PK_maptool.py (no cambia el EPSG bien) (26/3/24)
    2.00
        * SE HA PRODUCIDO UNA CAIDA DE LOS SERVICIOS DE CONSULTA QUERY A LA GEODATABASE. COMENZAMOS LA CREACIÓN DE UN SISTEMA
            MIXTO DE CONSULTA A UNA BASE DE DATOS GPKG EN LOCAL O EN UN SERVIDOR. (29/12/23)
        * Se inicia la creación de bypass AUTOMÁTICO que salten los errores de acceso a las URL Query de la GDB a
          consultar sobre un GPKG. Se incluyen la nueva configuración de fichero GPKG los datos.
            - PK_maptool.py Resueltos PkTool.getPointPK y PkBalizaTool.getBalizaPK (21/1/24)
            - Resueltos jccm_bar_config.py (21/1/24)
            - fun.pointToPK altera variable a GPKG si no consigue datos por URL  (29/12/23)
                aparece fun.pointToPK_GPKG (17/01/24)
            - fun.getJCCMMuniProv  altera variable a GPKG si no consigue datos por URL (29/12/23)
                aparece fun.getJCCMMuniProv_GPKG (17/01/24)
            - Se meten en config y jccm_bar_config.py todas las variables de fichero GPKG (23/1/24)
            - Se modifican los exception para que devuelva la linea mediante el fun.PrintException(23/1/24)
            - Se modifica jccm_buscadorGeneral.py goToRoad_clicked mediante fun.getFeaturesCarretera_GPKG (26/1/24)
        * Se resuelven unos problemas de la descarga de PKs en herrCTRAS_descargas.py (11/2/24)
        * Revisado un pequeño error en catálogo cuand se elige un directorio con caracteres no aceptados (ñ,á...) (29/2/24)
    1.33
        * Se arregla jccm_geomGetlista.py para que devuelva coordenadas y superficie de cada anillo multipoligono (17/12/23)
    1.32
        * En el buscador catastral, se introduce la posibilidad de ENTRAR TEXTO con diferentes RRCC, que convierte en listado (4/12/23)
            * Opción con espacios, o separadores como comas u otros
                ej:
                02055A01700038; 02055A0 1700043 0000MY, 02055A0 1700065 0000 MS, 02055A0 1800002 0000 MD;02055A0 1800265 0000 MS, 02055A0 1800345 0000
            * Opción lista de RRCC desde una comunicación normalizada de catastro
                ej:
                02055A0 1700038 0000 MA Polígono 017 Parcela 00038 Paraje MAJADA DE LAS VACAS - NERPIO ( ALBACETE )
                02055A0 1700043 0000 MY Polígono 017 Parcela 00043 Paraje SALTADOR - NERPIO ( ALBACETE )
                02055A0 1700065 0000 MS Polígono 017 Parcela 00065 Paraje CAÑADA DE BOGARRA - NERPIO ( ALBACETE )
                02055A0 1800002 0000 MD Polígono 018 Parcela 00002 Paraje UMBRIA ARROYO BLANCO - NERPIO ( ALBACETE )
                02055A0 1800265 0000 MS Polígono 018 Parcela 00265 Paraje MOLATA DE LA CASILLA - NERPIO ( ALBACETE )
                02055A0 1800345 0000 MT Polígono 018 Parcela 00345 Paraje SOLANA DEL MACALON - NERPIO ( ALBACETE )
        * El menú de buscador permite ahora eliminar la capa PARCELAS CATASTRALES si se desea (30/11/23)
        * Se arreglan los submenús ANADIR del menú 'capas' del config (2/12/23)

    1.31
        * Hacemos una consulta a la GDB de las vías que cortan un buffer de 'bufDist', en functions3.poligToPKINIPKFIN (12/11/23)
        * Se arregla un problema de la identificación de un punto, al dar el listado de coordenadas (11/11/23)
        * Se meten las urls de query de pob. y munis. bien ordenadas en config (11/11/23)
        *****   *****   *****   *****   *****   *****   *****   *****   *****   *****   *****   *****   *****   *****   *****   *****
        * CAMBIAN TODAS LAS URLS DEL SIG DE CARRETERAS, DONDE DICE http://geoservicios, DEBE DECIR https://geoservicios (11/11/23)
        *   Se altera el PROYECTO BÁSICO, config.py, settings.py, jccm_bar_config.py, functions3.py, jccm_bar_configurador.ui
        *****   *****   *****   *****   *****   *****   *****   *****   *****   *****   *****   *****   *****   *****   *****   *****
        * Pequeño arreglo en herrExpro_INFOEXPTES.py faltaba el dato del EX_PROTOCOLO_REGISTRO (innecesario) (22/8/23)
        * En CTRL CALIDAD GDB, se incluye un cálculo de EJES CAKIBRADOS CORRECTOS, ordenando los tramos (17/4/23)
        * Se corrige un error en INVESTIGAR_INVASIONES cuando no están las capas necesarias (17/4/23)
        * Añadido datos DistINI y DistFIN (23/04/07)
            - TODO: SE DETECTA ERROR EN CÁLCULO DistINI y DistFIN CUANDO EL ELEMENTO TIENE VARIOS TRAMOS
            - TODO: TAMBIEN AFECTA AL CÁLCULO DE DIST_A_PLACA
        * Se añade una leyenda al control de calidad (23/04/06)
        * Se revissa el control de SENTIDOS INVERSOS (23/04/04)
        * Reforma de catálogo para seleccionar EXCEL, WEB en la salida. Se modifican los colores de los listados (23/04/04)
    1.30
        * Se resuelve un error en el LISTADO DE CATÁLOGO. (23/03/12)
        * Resuelto error de dominio de idordenctra generico en herrCTRAS_controlCalidadGDB.py (23/01/23)
        * Resuelto error herrDP_informes_invasionDP.py cuando genera fichero con -- DATOS ERRONEOS --   (30/12/22)
            - (functions3.py -creaFICHintercambio-)
        * En control de calidad se mete un color de DENOMINACION igual para todos los tramos de las carreteras troncales (27/12/22)
    1.29
        * Resuelto pequeño error en herrCTRAS_catalogo.py por no aparecer el encabezado de RED (27/12/22)
        * Resuelto pequeño error en PK_info_dialog.py al no encontrar fichero GPKG con tabla datos históricos (12/12/22)
        * Detectado error en descargas, que no funciona con versiones muy modernas (9/12/22)
        * Se añaden campos de la capa PKS a la capa temporal BALIZAS DE CARRETERAS (2/12/22)
    1.28
        * La funcionalidad de CATÁLOGO ofrece la opción de genear un HTML y un EXCEL (25/11/22)
        * Localizado error en functions3.py CtraPktoCoorsAcim. TODO error en caso de problemas de calibración (18/11/22)
        * Se localiza error en cálculo de totales de CATÁLOGO DE CARRETERAS (15/11/22)
            TODO: Revisar listados solo por FUNCIONALIDAD
        * Reestructuración de fichero principal e iconos en jccm_bar3.py (15/11/22)
        * Un error detectado en 'herrDP_informes_invasionDP.py' por campos LEE_ que no tienen BD externas (14/11/12)
            TODO: Se deben analizar todos los campos con entrada LEE_ o en general todos los del posible fichero---
    1.27
        * Se incorpora al CATÁLOGO DE CARRETERAS un RESUMEN por PROVINCIAS y FUNCIONALIDADES (2/11/22)
    1.26
        * Se resuelve un problema en catastro_generaGML.py cuando localid o namespae es NULL (19/10/22)
        * En CATALOGO DE CARRETERAS listados de carreteras por tramos o se unen todos (27/10/22)
    1.25
        * En herrCTRAS_catalogo.py se arreglan distintas cosas (17/10/22)
            Se mejora el redondeo de totales de KM
            Aparece el nombre de la provincia o JCCM en ficheros y capas
            Se estudia la unión de tramos de igual MATRICULA
    1.24
        * Se modifica en config la capa de la que lee la cota Zmdt (29/09/22)
        * Se arregla el config para que resetee las unidades por defecto del fichero CONFIG (29/09/22)
            Se debería leer el config al actualizar el complemento
        * Se arregla un error en BALIZA DE CARRETERAS cuando no responde Zmdt (29/09/22)
        * Se añade un LOG a la creación del GML (13/9/22)
        * Se pone opcional la numeración secuencial {NUM} del LOCALID en la creación del GML (15/9/22)
        * En creación del GML no se generan parcelas con NAMESPACE distinto de 'ES.SDGC.CP' o 'ES.LOCAL.CP'(21/9/22)
    1.23
        * Comprobaciones en la creacionGML. Si namespace ES.SDGC.CP, se comprueba validez RC (24/8/22)
        * Resuelto problema de SRC en creacionGML para que funcione en otros EPSG de España, HUSOS 28,29 y 31 (24/8/22)
        * Resuelto problema de poner arriba el GML generado en catastro_generaGML.py (18/8/22)
        * herrDP_informes_invasionDP.py Resuelto error en calculo de RESTOS en INVASION (8/7/22)
        * Ahora en caso de NO INVASIÓN, da los datos del EXPTE COLINDANTE (29/6/22)
        * En herrDP_informes_invasionDP.py, los geoprocesos se hacen transformando los CRS (29/6/22)
        * Corregido herrDP_informes_invasionDP.py para incorporar dato EX_PROTOCOLO (7/6/22)
            También se permite dato REGISTRO alfanumérico, y se anula el botón al crear GML
        * Creando el config de INVENTARIO, se resuelven conflictos para externos (24/5/22)
        * Resuelto pequeño error en buscadorCATASTRAL cuando no hay conexión a catastro (27/4/22)
        * Solucionado error de PKs en NO INVASIÓN (15/4/22)
        * Arreglado extent en capa PARCELAS CATASTRALES al borrar parcela (15/4/22)
    1.22
        * Resuelto pequeño error en catastroDescPolig.py cuando falla la respuesta (30/3/22)
        * Se añade un botón de DESCARGA EJE en la información de punto pinchado (28/3/22)
        * Resuelto error en Catastro Histórico PK_info_dialog.py (25/3/22)
        * Arreglado pequeño error de datos en herrDP_informes_invasionDP.py (24/3/22)
        * Resuelto pequeño error en caso de INVASIÓN AEE y BIENES INMUEBLES (21/3/22)
        * Resuelto el caso de parcelas de NO INVASIÓN (21/3/22)
    1.21
        * Resuelto error en la carga de municipios, en vez de buscar por 'cmc', tira de 'cpcmc' (16/3/22)
        * Resolución de error function3.buscaTTMMpoligono cuando la superficie es demasiado grande(14/3/22)
        * Reunificados y reagrupados módulos y llamadas de catastro con nombre 'catastro' en jccm_bar3.py (11/3/22)
            Desaparece parcela_catastral.py
            Cambiado plantillacatastro.py a catastroPlantillaGML.py
        * herrEXPRO_generaGML pasa a catastro_generaGML (11/3/22)
        * Resuelto pequeño error de generación de GMLs cuando no estabas en una capa de pol (11/3/22)
        * Se incorpora una nueva función mas general de cargaListRCS (7/3/21))
    1.20
        * Nueva función de INFO de parcela catastral (EN PRUEBAS) con info de colindantes (1/3/22)
        * Corregido un error en la carga de catastro de TTMM completos (3,3/22)
        * Cambiamos cargarCapaParcelaCatastSHP cargarCapaParcelaCatastral para unificar la carga de parcelas (25/2/22)
        * En catastroDescPolig.py se activa el checkbox si la capa tiene elementos seleccionados (25/2/22)
    1.19
        * Resuelto falg NONMODAl en menún que quedaba escondido en herrExpro_BUSCEXPTES.py (24/2/22)
        * Se permite copipega en labels de coordenadas de polígono jccm_geomGetlista.py (23/2/22)
        * Mejoras en datos de campos de Descarga catastral por polígono(22/2/22)
          -Conviene adaptar la carga individual de parcelas para que se añadan/eliminen de una capa cargada por polígono.
        * Resuelto pequeño error de búsqueda de PKs de tramos no calibrados(7/2/22)
        * En la identificación catastral se incorpora un acceso por RC al geoportal registradores (1/2/22)
        * En la identificación catastral se incorpora un acceso a la imagen del inmueble -EN CONSTRUCCIÓN- (1/2/22)
        * Se mejora la herramienta para su uso en el análisis de DP en caminos de AYUNTAMIENTOS (20/1/22)
            VER AYUDA ESPECIAL PARA DOMINIOS PÚBLICOS DE AYUNTAMIENTOS
            TODO: Analizar crear exptes 1 x 1
            TODO: En NO INVASION identificar EXPEDIENTE mas próximo
            TODO: Identificar parcela colindante de DP
            TODO: Unir en GML parte invadida a parcela de DP
            - NOTA: para aparición de las herramientas, modificar variable de usuario
                "JCCM_carreteras/GENERAL/01Ambito" = AYUNTAMIENTO (mayusculas y sin comillas)
    1.18
        * Resuelto error en el BALIZADOR DE CARRETERAS y la identificación del lado pinchado de la carretera (19/1/22)
        * Se resuelve un pequeño error de config en gestorCapas.py (10/1/22)
        * Control de Pks en GDB. Existencia de todos los PKs de cada tramo (6/1/22)
            TODO: Estimar si se quiere meter PK 0
            TODO: Control de atributos de tabla de PKs
            TODO: Control de PKs contra calibración
    1.17
        * Mejora de descargas de capas de TTMM desde catastro, se añade building y addresses (3/1/22)
        * Herramienta de descarga de parcelas catastrales por polígono (29/12/21)
        * Herramienta de borrado de parcelas cargadas (23/12/21)
        * Mejorada herramienta ABOUT y ayuda en index.html (23/12/21)
        * Se reparan iconos de herramientas catastrales y otras (23/12/21)
    1.16
        * Resuelto ZOOM cuando parcela ya existe en PARCELAS CATASTRALES (21/12/21)
        * Se incorpora al buscador catastral la opción de buscar por IDUFIR (14/12/21)
        * En la carga de parcelas catastrales, se añade el campo CAT_NMSPC = 'ES.SDGC.CP' (9/12/21)
        * Resuelto pequeño error de código en functions.pointToPK (2/12/21)
        * Resuelto el problema de margen dcho/izdo en herrExpro_informes_invasionDP.py (27/11/21)
    1.15
        * Se incorpora al menú Pkinfo la infrmaciónde PK+DISTAPLACA (25/11/21)
        * Calculo de point to ctra mucho más simplificado (23/11/21)
        * En carga capas se permite carga de caps JSON (21/11/21)
        * Resuelto error de salida datos Nonetype en PKmaptool (18/11/21)
        * En INVESTIGAR INVASION DOMINIO PÚBLICO se hace el GML directamente (30/10/21)
        * En INVESTIGAR INVASION DOMINIO PÚBLICO se exige la entrada de datos obligatorios (30/10/21)
        * Resuelto problema de margen en herrExpro_informes_invasionDP.py (30/10/21)
        * Info de Datos Historicos en PK_info_dialog (26/10/21)
        * En control de calidad, se crea una plantilla específica para CTRL, diferenciadad de CATÁLOGO (24/10/21)
        * Arreglos en PKinfo para permitir copipegar y colores de matrícula (19/10/21)
    1.14
        * En buscador de parcelas se eliminan espacios en la RC introducida (14/10/21)
        * En buscador de parcelas/carga desde capa, se identifica la capa activa en el combo (14/10/21)
        * Se añade la visulización de un dock con los datos de info de geometría de la carretera (30/9/21)
        * En herrCTRAS_controlCalidadGDB.py metemos ctrl 'Inicios negativos' (14/9/21)
    1.13
        * Se corrige un error en el identificador de carreteras (10/9/21)
    1.12
        * Resuelto pequeño error al crear la capa PARCELAS CATASTRALES, campo VIA pasa a STRING (1/9/21)
        * Ya funciona el botón 'QUITAR' de herrExpro_informes_invasionDP.py (16/8/21)
        * Se resuelve la carga sin CRS de 'PARCELAS CATASTRALES' (16/8/21)
        * Metemos un buscador de CTRA PK contra los datos de Cartociudad (IGN RT) (4/8/21)
        * Se mejoran ciertos errores de herrExpro_informes_invasionDP.py (6/8/21)
        * El calculo de CAPAdesdeCTRAPK ahora mete en LOG todos los campos y atributos de la capa origen (27/7/21)
    1.11
        * Conseguido el borrado de puntos, pero solo para versiones de QGIS 3.16 o superior (8/7/21)
        * IMPORTANTES cambios en CONFIG:
            - Se meten todos los grupos deCONFIG  igual que en SETTINGS
            - Desaparece el grupo de settings /JCCM_EXPRO/ -> pasa a /EXPROPIACION/
        * La URL y datos para Zmdt se mete como variable en config (25/5/21)
    1.10
        * Cuando no funciona la URL del IGN para obtener cota, se avisa de error (20/5/21)
        * Se está creando una herramienta de INVENTARIO (OF, SEVE, SEHO, etc) (19/5/21)
        * Arreglo de categorías de INVASION en 'Investigar Invasión de DP (19/5/21)
        * Arreglo de errores de coincidencia total de CTRA en 'Generar Capa desde Tabla' (18/5/21)
        * Se obtienen datos históricos de carreteras s los hay (10/5/21)
        * Reorganizadas todas las variables en el Config (3/5/21)
            TODO: PONER VARIABLES DE USUARIO EN LUGAR DEL CONFIG
            - Puestas en jccm_bar3/catastrotools/PK_maptool/PK_maptoolFICH
            TODO: REORGANIZAR CIERTAS VARIABLES = MENUS = CONFIG
        * Se cambian las fuentes de librerías, de 'qgis.PyQt. ...' a 'PyQt5. ...' (3/5/21)
        * Se meten VARIABLES en GENERAL: 01Ambito, fich_config_capas (2/5/21)
        * Cambio de todos los self.current_configuration por self.conf (28/4/21)
        * Cambio de variables de 'environment' y 'otras' a 'general' (28/4/21)
        * Resuelto un pequeño problema al modificar el campo LRS (Matrícula o Matricula_Plan) (27/4/21)
    1.09
        * El buscador CTRA / PK permite ahora poner una baliza en el punto (24/4/2021)
        * En el buscador general al dar ENTER se accede a las funciones (18/4/2021)
        * Arreglados errores en GENERAR CAPA DESDE TABLA tipo lineal (15/4/2021)
        * Arreglado un pequeño error en GENERAR CAPA DESDE TABLA, cuando no existe la carretera (18/3/2021)
    1.08
        * Resuelto error de herrCTRAS_CAPAfromCTRAPKS.py en caso CALIBRADA (4/3/21)
        * Corregidos errores del herrCTRAS_CAPAfromXY.py porque ponia mal los datos de atributos geométricos caso de existir el campo(23/2/21)
        * Las funcionalidades que tiran de capas de mapa, ahora ponen en el combo la capa activa(23/2/21)
        * La carga de eventos puntules, ahora carga una leyenda n la que se ve el PK (16/2/21)
        * Se arregla también herrCTRAS_CAPAfromCTRAPKS.py para permitir buscar por distancia a la placa de KM anterior
            (solo eventos puntuales) (16/2/21)
        * El buscador de CTRA,PK ahora permite buscar por distancia a la placa de KM anterior -fun.CtraPktoCoorsAcim- (10/02/21)
        * Arreglos en herrExpro_informes_invasionDP.py por errores de interpretación de NO COLIND.JCCM (12/01/21)
        * Arreglos en herrExpro_informes_invasionDP.py cuando los string son unicode (12/01/21)
        * Cambiados catastrotools.py y function3.py cargaCatastroMuni para la carga desde otras herramientas (03/01/21)
        * Creada herramienta de Creación de exptes de Expropiación (PROVISIONAL) (21/12/27)
        * Corregidos decimales de sup en jccm_geomGetlista.py (21/12/20)
        * Corregido error en herrExpro_informes_invasionDP.py, cuando no existe carretera/camino colindante (21/12/20)
    1.07
        * Corregido el mismo error en buscador de parcela, caso de muchas parcelas con igual pol/par. Detecta David Cantero (16/12/20)
        * Corregido el mismo error en buscador de parcela, cuando es rústica con 'dato sector' = 'C'. Detecta David Cantero (14/12/20)
        * Se altera estructura fecha a 'MM/dd/yyyy' en creaExpte de functions3 por problemas de lectura en Access (14/12/20)
        * Corregido error en identificador de parcela, cuando es rústica con 'dato sector' = 'C'. Detecta David Cantero (11/12/20)
        * En INVASIONES DP, datos de Expte salen de capa LEE (Lista Exptes. Expro.) Debe tener union con Limites de Expropiación (6/12/20)
        * En INVASIONES DP, SOLICITANTE e INTERESADO salen de la lista del config (2/12/20)
        * En INVASIONES DP, pequeño arreglo de la tolerancia en superficie que resulta NO INVADE para SUP<1.00 m. (2/12/20)
    1.06
        * En Config se hacen editables las listas de ficheros y extensiones de la copia de seguridad (23/11/20)
        * Se ha metido un aviso en el análisis de invasiones para casos 'SIN CLASIFICAR' (23/11/20)
        * Traducido la funcionalidad de BORRADO DE MARCAS y CAPAS CARGADAS (4/11/20)
    1.05
        * Se adapta la herramienta de herrCTRAS_CAPAfromCTRAPKS.py en functions3.py al nuevo cálculo de buscar tramos (3/11/20)
        * En el buscador de poblaciones se mete la provincia (2/11/20)
        * Ampliado el buscador que ahora permite buscar tramos y meterlos en una capa (2/11/20)
        * Resuelto un pequeño error de carga de clases de librería Core en el config(27/10/20)
        * Resuelto un error de la función de 'Carga Capas de Catastro por Municipio' para versión 3.16. Solucionado por Ignacio R.de A.(27/10/20)
        * Herramienta De Visualizado de variables de la aplicación en config (20/10/2020)
        * Arreglado el config.py y jccm_bar_config.py para que la lista de capas las coja desde el fichero externo (20/10/2020)
        * Reordenadas algunas variables de catastro sacadas de 'environment' para ponerlas en 'catastro_tool' (20/10/2020)
        * gestorCapas.py y gestorcapas_ini .PY ahora dependeN de un listado en fichero, lo toma de config inicial para user local (17/10/20)
        * Se arregla parcialmente la herramienta de 'herrExpro_cargaEstado()' en herrExpro_cargacapas.py (16/10/20)
            TODO: Parcialmente porque debería cargar la capa desde el CONFIG
    1.04
        * Se crean funciones de infocarreteras desde fichero de datos -no web- (05/10/2020)
        * Se crea en functions herramienta de calculo de PKINI y PKFIN de un poligono (28/9/2020)
        * Se elimina la denoinación BETA del plugin (20/9/20)
        * Resuelto pequeño problema de l copia de seguridad de Exprpiaciones (9/9/20)
        * Terminada la parte de cambiar atributos en INVESTIGAR INVASION DOMINIO PÚBLICO (2/9/20)
        * Se modifica el directorio de transformación al 'TRANS_ED50_ETR89'. Se altera el settings.py (9/9/20)
        * Agregado PKINI/PKFIN provisional en el centro de la INVASIÖN, añadida ctra caso de NO JCCM (INVASION DOMINIO PÚBLICO) (2/9/20)
        * Pequeño arreglo para no repetir en las listas RC14 ya cargadas (31/08/20)
        * Arreglos del config para usuarios externos (31/08/20)
    1.03
        * En INVESTIGAR INVASION DOMINIO PÚBLICO. Se añade un gestor de numero de exptes automático. Añadiendo parcelas no invadidas a fichero resultados 'Zonas Invadidas'.
            Se permite el cambio de atributos de los valores a meter en Informes de Expropiaciones (19/8/2020)
            Desarrollada la herramienta de CREAR EXPEDIENTES desde functions3 (25/8/20)
        * Unificadas funciones comunes de catastroBuscador.py y herrExpro_informes_invasionDP.py en functions3 (25/8/20)
        * En herrExpro_REMISION se enlaza a las funciones de CREAR EXPEDIENTES desde functions3 (25/8/20)
        * Se meter nombre de TM en capa PARCELAS CATASTRALES (19/8/20)
        * La herramienta de listado de polígonos ahora permite el listado de todo tipo de capas de polígono (con M o Z) (10/7/20)
        * Ahora se permite trabajar con capas de expropiaciones desde GPKG, por medio del config (10/7/20)
        * Se incorpora un nuevo config con tab para herramientas expropiaciones (6/7/2020)
        * Resuelto pequeño error en el setting de CRS personalizado (2/7/2020)
    1.02
        * En el buscador de carreteras, cuando se teclea el PK al pulsar enter va a la selección (20/6/2020)
        * Corregido error en catastrotools cuando se pincha una parcela DESCUENTO (16/6/2020)
        * Se corrige alteración de la codificación de la fuente en las capas de expropiaciones (01/06/2020)
        * Creada la funcionalidad de REMISIÓN DE EXPTES DE EXPROPIACIONES (25/5/2020)
        * Mejorado la funcionalidad INFO. Expediente de expropiaciones en modo panel (18/5/2020)
        * Se elimina la opción de intersección solo con seleccionados -herrExpro_informes_invasionDP.py- (9/5/2020)
    1.01
        * Resuelto un error de carga en gestorCapas.py (7/5/20)
        * herrCTRAS_descargas.py prmite ahora bajar ficheros de PKS (11/4/20)
        * En herrCTRAS_descargas.py se pone una opción de bajar o no M. Por errores del JSON con M, los elementos sin valor M no se visualizan en planta (7/4/20)
        * Creación de Sistema de Referencia de Coordenadas CRS User 'ETRS89 ED50  IGN REJILLA' (2/4/20)

    1.00
        * FINAL DE LA TRADUCCIÓN DESDE QGIS 2 A QGIS 3 (30/3/2020)
        * TODO:
        *  -- SE DEBEN ORDENAR LOS GRUPOS VECTORIAL SOBRE RASTER EN LAS CARGAS DE CAPAS

    0.36
        * Traducción 08.3  herrCTRAS_CAPAfromXY.py     (30/3/2020)
        * Arreglado gestorCapas.py (27/3/2020)
        * Arreglado gestorCapas_ini.py (26/3/2020)
        * Traducción 08.3  herrCTRAS_CAPAfromCTRAPKS.py     (25/3/2020)
        * Añadida nueva función de información de Expte de Expropiación (10/3/20)
        * Resuelto pequeño error en la carga de variables de usuario COPYSEG (7/2/29))
        * Cambian los antiguos parametros last en buscador catastroBuscador.py y herrExpro_informes_invasionDP.py a JCCM_carreteras/last/  (26/2/20)
        * Se mejora herrExpro_generaGML.py. Se asignan en los parámetros desde diferentes 'last'. SRC desde current, campo directo a LOCALID (26/2/20)
        * Todas las variables de usuario de Expropiaciones, quedan integradas dentro del grupo de variables de QGIS: JCCM_carreteras/JCCM_EXPRO/ (26/2/20)
            - Se pueden visualizar o alterar  ¡¡¡SI SE CONOCE LA APLICACION!!! en Configuracion > Opciones > Avanzado > Tendreé cuidado lo prometo
    0.35
        * Corregido error en streetview.py, gracias a la aportación de IGNACIO ROMERO DE ÁVILA (24/2/20)
        * Corregido un error en el buscador ctra,pk, fallaba cuando el tramo tenía valores sin M (20/2/20)
        * El nuevo config de variables altera toda la aplicación, se resuelven herrExpro_cargacapas.py (19/02/20)
        * Se añade una herramienta 'Estado de EXPROPIACIONES' en herrExpro_cargacapas.py/herrExpro_cargaEstado()  - FALLA - (13/2/20)
        * Se unifican las variables EXPRO en el subdirectorio espeficico /JCCM_EXPRO/ en las variables personales (13/2/20)
    0.34
        * Resuelto el problema de solapes en restos de invasiones de DP (10/2/20)
        * Se arregla el módulo 'herrExpro_generaGML.py' para mejorar la salida en formato Catastro (9/2/2020)
        * El modulo settings modifica ahora variables de sistema (9/2/2020)
            Qgis/enableMacros',3                      # Activar Macros - Siempre
            Qgis/warnOldProjectVersion', False        # Avisar de Proyecto guardado con version ant.
            Qgis/checkVersion', False                 # Chequear Version QGIS al empezar
            Qgis/askToSaveProjectChanges', False      # Quita el aviso inicial de guardar
        * Se modifica la ubicación de la variable ACCESOEDITOR, que queda como variable de usuario de la app (9/2/2020)
        * Resuelto un error al pinchar en una carretera fuera de la región (5/2/2020)
    0.33
        * Traducción 15.0  about_dialog.py (4/2/2020)
        * Resuelto el guardado de ficheros en distintas funcionalidades herrCTRAS_descargas.py -salida_file_click-    (4/2/2020)
        * Resuelto el guardado de ficheros en distintas funcionalidades herrCTRAS_catalogo.py  -salida_file_click-    (4/2/2020)
        * Resuelto el guardado de ficheros en distintas funcionalidades herrExpro_generaGML.py -gml_salida_file_click-(4/2/2020)
        * Resuelto el guardado de ficheros en distintas funcionalidades PK_info_dialog.py      -botonGuardaCSV-       (4/2/2020)
        * Se crea una herramienta de configuración de la de analiis de invasiones del DP (3/2/2020)
    0.32
        * Se agrupan en una herramienta desplegable distintas herramientas catastrales (28/1/2020)
    0.31
        * Traducción 08.7 herrCTRAS_controlCalidadGDB.py (28/1/2020)
        * Traducción 08.1 herrCTRAS_catalogo.py (26/1/2020)
        * Traducción 09.3 herrExpro_informes_invasionDP.py (19/1/2020)
        * Resuelto el error de códigos de municipios PK_maptool.py (24/1/2020)
        * Resuelto el error de carga de municipios codine != codcat catastrotools.py (24/1/2020)
        * Resuelto un error en PH INFO, faltaba rutina getRoadLmits (20/1/2020)
        * Traducción 09.9 herrExpro_copyfiles.py (19/1/2020)
        * Traducción 09.4 herrExpro_generaGML.py (19/1/2020)
        * Traducción 09.2 herrExpro_BUSCEXPTES.py (18/1/2020)
        * Traducción 09.1 herrExpro_cargacapas.py (18/1/2020)
    0.30
        * Traducción 13.0 Imprimir Vista (17/1/2020)
        * Traducción 12.0 Cargar Capas Inicio (12/1/2020)
        * Traducción 11.0 Borrar Marcadores y capas cargadas  (10/1/2020)
        * Traducción 10.0 Carga Catálogo capas SIG (10/1/2020)
        * Traducción 07.0 Catastro Buscador (10/1/2020)
        * Traducción 06.0 Carga catastro histórico (9/1/2020)
        * Traducción 05.0 Carga capas de catastro por municipio en catastrotools.py (08/01/2020)
        * Carga de parcela y datos de catastrotools.py (07/01/2020)
        * Traducción 04.0 catastrotools.py (23/10/2019)
            - Implica a parcela_catastral.py
        * Traducción 01.5 jccm_geomGetlista.py (22/10/2019)
        * Traducción 03.0 streetview.py (21/10/2019)
        * Resuelto el problema de la herramienta de identificar PK (21/10/2019)
        * Resuelto el problema del icono jccm.jpg
    0.20
        * Traducción 0.1 jccm_bar.py a jccm_bar3.py
        * Traducción 0.2 functions.py a functions3.py
        * Se crea cambios2to3.txt con una relación general de cambios y módulos/clases
        * Traducción 1.1, 1.2 pkmaptool.py, PK_info_dialog.py, balizas_carretera.py a PK_maptool.py, PK_info_dialog.py, PK_balizas_carretera.py
        * Traducción 1.3 jccm_puntoZ.py anulación jccm_Zmdt_dialog.py
        * Traducción 2.0 jccm_buscadorGeneral.py

    0.10
        * Inicio de la traducción de QGIS 2.14 a 3.8.2

nextchangelog=
    TAREAS PENDIENTES TODO
    ----------------------

    (22/01/14) Consultas a registro
        https://geoportal.registradores.org/idtramite/ID02005200002291
        https://geoportal.registradores.org/idufir/02005000756030
        https://geoportal.registradores.org/rfc/7269302WH8876N


homepage=https://github.com/asolabre/JCCM_BAR3
category=Plugins
icon=jccm.jpg
# experimental flag
experimental=False

# deprecated flag (applies to the whole plugin, not just a single version)
deprecated=False

# Since QGIS 3.8, a comma separated list of plugins to be installed
# (or upgraded) can be specified.
# Check the documentation for more information.
# plugin_dependencies=

Category of the plugin: Raster, Vector, Database or Web
# category= Vector

# If the plugin can run on QGIS Server.
server=False

