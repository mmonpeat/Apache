# Desplegament_Aplicacions_Web

##EX_01
He installat Ubuntu.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/6ec3ef62-29b2-4ef4-89da-371e49d8cb72)

He installat apache2, amb la comanda: sudo apt install apache2

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/baabb55c-ff78-44ab-8734-f6c086d67739)

##EX_02
###GET(obtenir)
- Una petició GET s'utilitza per sol·licitar dades d'un servidor.
- És una sol·licitud "segura" en el sentit que només llegeix dades i no les modifica.
- Les dades es passen a través de la URL com a paràmetres de consulta (query parameters), aquests es veuen.

###POST(enviar)
- Una petició POST s'utilitza per enviar dades al servidor per a ser processades.
- S'utilitza freqüentment per enviar formularis o realitzar accions que canvien l'estat del servidor, com ara crear un nou recurs.
- No passa les dades a través de la URL, sinó que les incrusta a la sol·licitud com a cos (body).

###PUT
- Una petició PUT s'utilitza per actualitzar totalment un recurs existent o crear-lo si no existeix.
- Com amb POST, les dades es passen al cos de la sol·licitud.
- Quan es fa una petició PUT, s'espera que el servidor reemplaci els continguts del recurs objectiu amb les dades proporcionades.

###DELETE
- Una petició DELETE s'utilitza per eliminar un recurs existent al servidor.
- Sol·licita al servidor que faci l'acció de suprimir el recurs especificat.
- Com a les anteriors, no passa dades a través de la URL o el cos, simplement sol·licita l'eliminació del recurs.
- És important tenir cura en l'ús d'aquest tipus de petició, ja que pot ser irreversible i suprimir dades de forma permanent.

##EX_03
Primer hem de buscar l'arxiu on s'ha installat apache2
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/35c02bf3-6869-4061-a882-ffb3dfc64624)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/afe7bcae-4866-469c-a3ba-a080cb228efb)
Reiniciem el servidor 
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/caf5c675-3169-4804-a973-f9a5468aed14)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/539cad47-432b-488f-93dd-98807da99fca)

