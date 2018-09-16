Debate App
----------

TODO Poner nombre!!!
Un torneo son muchas cosas!!

Propósito
=========

Crear una App para la gestión de torneos de debate {académico español}. Deberá incluir:

* Automatización de los cruces
	- Qué equipos debaten con qué equipos (pueden tener incompatibilidades - equipos que no deberían debatir entre sí, a menos que sea la final)
	- Horarios y espacios (en cada ronda hay un número de salas)
	- Qué jueces juzgan qué debates (incompatibilidades con equipos)
	- Qué staff está en cada sala
* Automatizar el proceso de puntuación de equipos/oradores
	- Los jueces puntuan a los equipos en cada debate (items)
	- Los jueces deciden qué equipo gana cada debate
	- Los jueces obtienen un informe con estadísticas sobre cada equipo y cada orador
	- Los jueces votan al mejor orador (opcional)
* Automatiza las calificaciones de los jueces (opcional)
	- Los jueces se evalúan entre sí
	- Los oradores evalúan a los jueces
* Red social para debate {futuro}
	- Calendario de torneos
	- Amigos
	- Debates online
	- Chats
	- Recursos didácticos/organización
		- Registro de los informes



Roles de un torneo de debate
============================

### Personas físicas (usuarios)
* Coordinación del torneo
	- Coordinador del torneo (1 por torneo, máxima autoridad)
	- Adjudicador (X por torneo - típicamente 3, contratados/invitados por el coordinador)
	- Tabuladores (X por torneo, pueden ser muchos - típicamente 1 por cada 10 equipos)
	- Equity (opcional) {prescindimos en la primera versión}
	- Coordinador de staff (duplicado)
* Staff
	- Coordinador de staff (1 por torneo, puede cambiar temas logísticos de forma manual)
	- Asistente de sala (1 por sala - siempre en la misma sala, para todos los debates que haya en la misma)
	- Corredores (depende de lo grande que sea el torneo, prescindibles si su función se automatiza)
	- Otros
		- Distintos tipos de staff (fotógrafo, etc.) definidos por el coordinador de staff
* Equipos (2 equipos por debate, entre 2 y 6 personas por equipo, dependiendo de cómo esté definido en el reglamento)
	- Oradores (1 orador pertenece únicamente a un equipo; un usuario con este rol no puede tener otros roles en el torneo)
		- Capitán del equipo (1 por equipo, opcional - dependiendo del torneo)
		- Distintos tipos de oradores (introductor, refutador, etc.) definidos por el reglamento {cadena de caracteres}; cada orador será de un tipo, elegido por el equipo para cada debate {para el futuro}; el capitán tiene uno de estos subtipos también.
	- Formador (opcional, 1 formador puede tener asociados varios equipos; puede tener otros roles en el torneo) {futuro}
* Jueces (X jueces por sala, que pueden tener alguno de los siguientes roles, típicamente 2 o 3) 
	- Juez principal (1 por sala)
	- Panelista (opcional, muy típico, típicamente 2)
	- Trainee (opcional)


### Recursos
* Torneo
	- Pregunta
	- Localización(es) - Mapa
	- Fechas - Calendario
	- Equipos', Adjudicadores', etc.
	- Reglamento
		- Info del torneo (Localización, fechas, pregunta, etc.)
		- Definición Items
		- Faltas
			- Penalización sobre la puntuación total de los items
* Acta (pueden ser emitida por los jueces individuales o por el conjunto de ellos - el juez principal firma)
	* Items (sirven para puntuar el equipo y al orador) {empezaremos por tener una variable numérica, simplemente; luego, descripción del item+puntuación}
		- Ejemplos: Se utiliza bien los espacios, buen control de los exordios, citas de autoridad, etc.
	* Votación al mejor orador (opcional)
	* Información del debate:
		- Pregunta
		- Cruce (equipo a favor y equipo en contra)
		- Nombre del equipo y miembros
		- Anexo de criterios de juzgar
* Salas (una sala puede alojar un debate a la vez)         ]
* Time-slot (un time-slot puede alojar un debate a la vez) ] -> 1 Debate requiere 1 sala + 1 time-slot
* Debate (el elemento central, que tiene tiene asociadas una serie de recursos y personal)
	- Sala + time-slot (1)
		- Staff
		- Mobiliario (opcional)
	- Equipos (2) - según cruces
	- Jueces (X)  - según cruces
	- Acta (1)
	- Fungibles (opcional)



Casos de uso
============

### Usuario (sin rol)
* Solicita formar parte de un torneo, con un rol determinado (pueden asignársele varios roles)
* Genera un torneo (pasando a ser automáticamente coordinador del mismo)

### Juez
* Firma una hoja de acta donde pone quién gana (incluyendo puntuaciones, items)
* Emite un feedback sobre un debate concreto (a veces escrito) En la App: texto o audio. Idealmente, feedback para cada equipo y para cada orador.
* Los jueces se evalúan entre ellos (opcional, dependiendo del torneo).
* Pone faltas de reglamento (llegar tarde a un debate, etc.)

### Formador
* Ver resultados de sus equipos (si ganan o pierden) y feedback. Al mismo tiempo que sus equipos.

### Orador
* Participa en los debates que tiene asignados, como parte de un equipo
* Recibe feedback de los jueces.
* Recibe puntuaciones de los debates: saber si has ganado o perdido - los items son siempre privados (solo disponibles para staff) (opcional).
* Decir su rol concreto al juez (roles concretos de orador definidos por el reglamento)

### Adjudicadores
* Ponen la pregunta del torneo
* Ponen las características del torneo
* Ponen los criterios de los items, del paso de fase, de las votaciones (en caso de que haya votaciones entre los jueces y de los oradores a los jueces)
* Ponen orden cuando hay conflicto entre jueces (dos jueces que no se pongan de acuerdo, un juez que denuncie a otro juez....)
* Ponen orden en caso de que haya conflicto a nivel académico o de criterios (si un equipo se queja de que un juez ha juzgado mal)
* Define el anexo del acta, que contiene criterios para juzgar
* Controla las faltas de reglamento, puestas por los jueces (normalmente es función de Tabuladores)
* Toman medidas sobre las faltas de reglamento
	- Expusión de un equipo
	- Posibilidad de excluir del paso de fase
	- 
* Define los roles concretos de los jueces (asociados a cada debate), pudiendo cambiarlo de una ronda a otra

### Coordinador del torneo
* Puede modificar cualquier cosa: roles, horarios, etc.
* Acepta las solicitudes de los participantes, asignándoles un rol (juez, orador, etc.)


### Tabuladores
* Elegir las incompatibilidades (entre equipos, entre jueces y equipos, etc)
* Definen manualmente los cruces
* Introducen manualmente quién ha ganado los cruces, quién tiene los items, quién ha ganado mejor orador... (gestión de las actas)
* Hacen un informe final del torneo (estadística)
	- A favor ha ganado más que en contra
	- Equipos con más chicas han ganado más
	- Equipos novatos han ganado X% veces
* Controla las faltas de reglamento, puestas por los jueces
	- En caso de que un equipo u orador acumule muchas faltas (o faltas graves), se toman acciones:
		- Avisar a Equity
		- Avisar a Adjudicación


### Coordinador de staff
* Puede cambiar en qué sala debate un equipo
* Decide dónde va cada persona del staff y qué función tiene
* Escribe la guía del staff del torneo
* Gestiona los recursos físicos (agua, atriles, fotocopias) {en principio no se automatiza}


### Equity
* Define su apartado en el reglamento
* Media en conflictos de equity
	- Puede penalizar, de forma independiente a Adjudicación
	- Puede amonestar a los jueces
* Hace informes del torneo/debates
* Revisa la/s pregunta/s {en BP}
* Recibe quejas de equity



* Los usuarios podrán escribirse mensajes privados, que podrán tener forma de audio. Unidireccional: juez al equipo o juez al orador. El feedback podrá ser puntuado por el orador (no se permite una respuesta elaborada).
