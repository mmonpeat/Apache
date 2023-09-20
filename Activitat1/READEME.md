
## ex 03
## Analiza los headers de las peticiones cuando inicias sesión en el Moodle y comprende cómo se obtiene el token. Para ello, necesitamos saber de dónde salen TODOS los datos sensibles que se envían.
Podem veure el logintoken que és el Token per a ingrés (Login token) és una característica relacionada amb seguretat introduïda en les versions de Moodle 3.1.15, 3.3.9, 3.4.6, 3.5.3 i 3.6.0. 
Ajuda a protegir en contra d'un rang de vulnerabilitats, com ara el robatori de la sessió d'un altre usuari, via el format per a ingressar al lloc.
A partir de les versions esmentades, tots els formats (formularis) per a ingrés al lloc han d'incloure un nou camp de token per a ingrés i enviar-ho juntament amb el nom_de_usuari i la contrasenya. 
El valor per al camp ha de ser obtingut via l'anomenada a \core\*session\*manager::get_*login_*token(). Tots els intents d'ingressar al lloc sense el token proporcionat per a ingrés seran rebutjats.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/f9aead7c-396c-4935-9117-68b23ff7bdfd)

## ex 04
## ¿A qué puerto se reciben normalmente las peticiones del protocolo HTTP?
Al port 80.

## ¿A qué capa del modelo TCP/IP se encuentra el protocolo HTTP? 
Capa 4 o d'aplicació En aquesta capa és on trobem alguns protocols molt famosos com són l'HTTP de les pàgines web, el FTP per a la transferència d'arxius, DHCP com a protocol 
de configuració dinàmica de host o l'SMTP per a la transferència de correus.

![Suite_de_Protocolos_TCPIP](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/a6de451c-52cb-408b-8de1-90f7ce00107c)

## ¿Y los protocolos TCP, UDP, e IP?
El TCP i UDP a la capa de transport. El IP en la de internet.

## ex 05
## ¿Cuál es el significado de la siguiente respuesta de un servidor? 
###HTTP/1.1 302 Found 
###Location: http://www.example.com/test/index2.php
Indica que una URL específica ha estat traslladada temporalment a una nova ubicació. Cada vegada que els visitants, els robots de Google o altres motors de cerca accedeixen a la URL original, 
la redirecció 302 ofereix una resposta automàtica que indica una nova direcció.

## ex 06
## Utilizando el filtro de captura para la interfaz de red de Wireshark, analiza la petición al host: www.google.com. Mostrando la cabecera IP, la dirección IP de tu ordenador y la del servidor. Comprueba que, poniendo esa IP en el navegador, accedas a Google.
Posant aquesta IP 142.250.184.14 s'obre google.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/6739ef35-61d8-4ccb-bda3-bc071ab5d6c6)

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/1bd259ad-368e-4c5f-8d38-4e24d9c62423)

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/fe375747-d39f-4a3c-a72d-81276d236ce4)

