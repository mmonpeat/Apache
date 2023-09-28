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


