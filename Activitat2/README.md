# Desplegament_Aplicacions_Web

## EX_01
He installat Ubuntu.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/6ec3ef62-29b2-4ef4-89da-371e49d8cb72)

He installat apache2, amb la comanda: sudo apt install apache2

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/baabb55c-ff78-44ab-8734-f6c086d67739)

## EX_02
### GET(obtenir)
- Una petició GET s'utilitza per sol·licitar dades d'un servidor.
- És una sol·licitud "segura" en el sentit que només llegeix dades i no les modifica.
- Les dades es passen a través de la URL com a paràmetres de consulta (query parameters), aquests es veuen.

### POST(enviar)
- Una petició POST s'utilitza per enviar dades al servidor per a ser processades.
- S'utilitza freqüentment per enviar formularis o realitzar accions que canvien l'estat del servidor, com ara crear un nou recurs.
- No passa les dades a través de la URL, sinó que les incrusta a la sol·licitud com a cos (body).

### PUT
- Una petició PUT s'utilitza per actualitzar totalment un recurs existent o crear-lo si no existeix.
- Com amb POST, les dades es passen al cos de la sol·licitud.
- Quan es fa una petició PUT, s'espera que el servidor reemplaci els continguts del recurs objectiu amb les dades proporcionades.

### DELETE
- Una petició DELETE s'utilitza per eliminar un recurs existent al servidor.
- Sol·licita al servidor que faci l'acció de suprimir el recurs especificat.
- Com a les anteriors, no passa dades a través de la URL o el cos, simplement sol·licita l'eliminació del recurs.
- És important tenir cura en l'ús d'aquest tipus de petició, ja que pot ser irreversible i suprimir dades de forma permanent.

## EX_03
Primer hem de buscar l'arxiu on s'ha installat apache2
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/35c02bf3-6869-4061-a882-ffb3dfc64624)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/afe7bcae-4866-469c-a3ba-a080cb228efb)

Reiniciem el servidor

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/caf5c675-3169-4804-a973-f9a5468aed14)

Entrem al arxiu ports.conf i cnaviem la linea Listen 80 per 4444. 

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/539cad47-432b-488f-93dd-98807da99fca)

Però no tenim permisos de escritura pertant els hem de canviar amb chmod 777 o chmod 755. Per a canviar els permisos d'un arxiu de manera més segura, pots utilitzar chmod 755. Això establirà permisos de lectura, escriptura i execució per al propietari de l'arxiu i permisos de lectura i execució per al grup i altres usuaris. És una configuració més segura que encara permet al propietari de l'arxiu fer canvis, mentre que restringeix l'escriptura i execució a altres usuaris. Hem d'usar sudo devant de la comanda, per poder tenir permisos per canviar l'arxiu.


![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/9e2d467e-5140-49f1-a0df-3ba7e1c05b3b)

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/96a5970b-7594-4348-afb6-cffa5e6bb9d2)

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/7f8b44b2-9116-4ee2-872e-240c87e783c3)

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/5e909e2b-254a-4ee7-beef-0c508b18977e)

LLavors guardem l'arxiu i tornem a reinicia el servidor amb la comanda sudo service apache2 restart.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/42f3ea06-62ae-4dc3-875c-7a507b08ef2f)

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/d8f76d4c-9f1c-4ba4-8d27-d84b2e8a8d6f)

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/1007a814-9056-4ce2-8f78-5b4596ad9f2d)

Aqui podem veure la IP de la meva maquina.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/7e4cec45-2b50-4956-8d4c-3323574b5ab7)

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/5e9b6cf3-eec3-423a-a25a-a511e5d977b4)

* No ha funcionat obrir-ho al navegador, llavors mirem l'status de apache2.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/f8af18f1-e1a1-47ee-8412-bac4a0030c94)

He resolt el problema i aqui podem veure en el navegador amb http://localhost:4444 o http://127.0.0.1:4444

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/5e0efd8e-d51f-4a09-a0da-8f2d32a6c963)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/3c2aabf4-364b-4321-92a5-8fbbd784d3b3)

## EX_04

Si només tens dos arxius de configuració en /etc/apache2/sites-available, 000-default.conf i default-ssl.conf, això significa que estàs utilitzant la configuració predeterminada d'Apatxe per al lloc web principal i SSL. Aquí et mostro com habilitar SSL i configurar el teu lloc perquè funcioni amb HTTPS en el port 443 utilitzant aquests arxius. Hem canviat el port, que hem canviat en l'exercici anterior a 80, com abans.

PD: He utilitzat el 443 per que m'ho ha dit el profesor encara que en el exercici posa 4444. Tot i això caldria canviar els arxius ServerAdmin, DocumentRoot, ErrorLog, CustomLog, ports.conf i defoult-ssl.conf.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/f844ba81-b5ee-49a2-9bac-f13dc98ecbdf)

Abans de tot hem de canviar els permisos amb sudo chmod 755 /etc/apache2/sites-available/defoult-ssl.conf
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/600132c5-4de7-45db-b913-b3a172770776)

Executa el següent comando per a habilitar el mòdul SSL en Apatxe:
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/bdba50ed-9247-4a16-b8bc-8e08617d9543)

Comprovem que els arxius estan en la ruta /etc/ssl/certs i /etc/ssl/private, en aquesta no puc entrar.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/36c70806-532b-405a-af94-6e3e93fe3a1c)

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/4032be71-5188-4df7-967b-f4089ea3e5aa)

L'arxiu default-ssl.conf ha d'estar amb les rutes correctes, les seguents.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/943dad2a-2ee3-4e56-9821-94c4ec6be14f)

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/ede229b3-60f4-43a6-97d0-9d3df2d62914)

Habilitem el lloc ssl i reiniciem apache2.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/3ca321da-70ce-400d-9cf9-f1e9b73472ac)

Entrem al port amb https i el port 443. Es conecta encara que posa que és de risc, ho acceptem i seguim.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/d021b32c-1f8a-4cef-ad76-9ac0602e4682)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/92323b7f-c229-4542-b9b9-9b022302a64d)

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/d3b560f0-44c3-4572-b5ff-d26ce8aec27d)


