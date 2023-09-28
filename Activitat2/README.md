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
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/5e9b6cf3-eec3-423a-a25a-a511e5d977b4)

PD: No ha funcionat obrir-ho al navegador, llavors mirem l'status de apache2.

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

## EX_05
1. L'arxiu principal de configuració de Apache2 es troba en la següent ubicació:
/etc/apache2/apache2.conf
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/05ccb84f-1d88-4529-b5a7-2726d49bf95b)

2. Aquest arxiu conté configuracions globals per al servidor Apache2 i pot incloure configuracions generals que s'apliquen a tots els llocs allotjats en el servidor.
Codi principal:
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/b3f1250a-d453-4ffe-9ff1-a8c206130171)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/742209ee-e7c1-42e9-a463-ebdffb41b874)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/6104066c-512b-483d-b603-5abea87346f4)


3. Directoris sites-available i sites-enabled: Aquests directoris s'utilitzen per a gestionar la configuració dels llocs web virtuals en Apache2.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/78653b53-5118-4dd2-a7c7-3e6d9f00b955)

* /etc/apache2/sites-available/: En aquest directori, es troben els arxius de configuració dels llocs web virtuals disponibles. Cada arxiu representa una configuració de lloc web. Aquests arxius estan disponibles però no activats per defecte.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/4358e2b2-7070-4bb3-bf9a-086992a32c20)

* /etc/apache2/sites-enabled/: En aquest directori, es creen enllaços simbòlics (symlinks) als arxius de configuració dels llocs web virtuals que desitges habilitar. Quan habilites un lloc, Apache2 llegeix la seva configuració des de sites-available a través dels enllaços en sites-enabled.
  ![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/f5082e0b-3e0f-4cb8-98af-9cdff320ed48)

4.  Directoris mods-available i mods-enabled: Aquests directoris s'utilitzen per a gestionar els mòduls de Apache2.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/9fe6b89c-986f-4e68-a437-702a0739b15a)

* /etc/apache2/mods-available/: En aquest directori, es troben els arxius de configuració dels mòduls disponibles per a Apache2. Cada arxiu representa la configuració d'un mòdul específic.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/5a7cbb75-2e7b-463f-95f2-d429be39fe3a)

* /etc/apache2/mods-enabled/: Igual que en el cas de sites-enabled, aquest directori conté enllaços simbòlics als arxius de configuració dels mòduls que desitges habilitar. Habilitar un mòdul significa crear un enllaç simbòlic des de mods-available a mods-enabled.![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/fbb65c2b-8bfb-4cbb-b232-18688b740ece)

En resum, sites-available i sites-enabled s'utilitzen per a administrar la configuració de llocs web virtuals, mentre que mods-available i mods-enabled s'utilitzen per a administrar els mòduls de Apache2. L'arxiu apache2.conf conté configuracions globals per al servidor. Aquests components permeten una administració flexible i modular de la configuració de Apache2.

## EX_06
Anem al directori /usr/bin, per això cal tirar directoris enrrera fins /
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/0849fdfd-5337-4126-bb48-45714e47f633)

### Control de servei
Per a controlar el servei Apache2 en la majoria de les distribucions de Linux, pots utilitzar el comando systemctl, que és part del sistema d'inici systemd. A continuació, es descriuen els comandos comuns per a controlar Apache2:

Iniciar Apache2:
sudo systemctl start apache2
Aquest comando inicia el servei Apache2. El servidor web començarà a escoltar i processar sol·licituds.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/f7861d3b-7033-4366-ab13-e65206e23996)

Detenir Apache2:
sudo systemctl stop apache2
Aquest comando deté el servei Apache2. El servidor web deixarà d'escoltar i processar sol·licituds.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/7dff377d-1b98-4afd-ae23-8d7fe7181532)

Recarregar la configuració de Apache2:
sudo systemctl reload apache2
Aquest comando recarrega la configuració de Apache2 sense detenir el servidor. És útil després de fer canvis en la configuració per a aplicar-los sense reiniciar el servidor.
Cal fer start per fer reload.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/37c0e7ee-fa99-49f5-a908-cc159bee4755)

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/13b8c271-19ae-4186-a61f-fecb63ace64a)

Reiniciar Apache2:
sudo systemctl restart apache2
Aquest comando deté i després reinicia el servei Apache2. S'utilitza per a aplicar canvis importants en la configuració o reiniciar el servidor després d'actualitzar Apatxe o els seus mòduls.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/d89c02ba-8448-42e1-94a9-35af49c94774)

### Comprovació de sintaxi de configuració:

Per a verificar la sintaxi de la configuració de Apache2 abans de reiniciar el servidor, pots usar el comando apache2ctl. El següent comando verificarà la sintaxi de la configuració:
sudo apache2ctl configtest
Aquest comando revisarà la configuració i t'informarà si hi ha errors en la sintaxi. Si la configuració és vàlida, veuràs un missatge que indica "Syntax OK". Això és útil per a detectar problemes de configuració abans de reiniciar Apache2, evitant que el servidor es detingui a causa d'errors de configuració.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/85289c5a-5945-4411-9bd7-da219b6d7fb3)

## EX_07

### Ubicació principal dels arxius de monitoratge:
Els arxius de registre (logs) principals de Apache2 es troben en el directori /var/log/apache2/. Els arxius de registre més importants són error.log i access.log.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/fbde4858-3800-4e8c-8bb9-59b435524304)

error.log: Aquest arxiu registra errors i problemes trobats pel servidor Apache2. Això pot incloure errors en la configuració, errors de *scripts *CGI, problemes amb sol·licituds de clients i més.

access.log: Aquest arxiu registra totes les sol·licituds entrants al servidor Apache2, incloent-hi informació sobre les adreces IP dels clients, les pàgines sol·licitades, el codi de resposta HTTP i altres detalls d'accés.

### Rotació de logs en Apache2:

La rotació de logs és important per a evitar que els arxius de registre ocupin massa espai en disc i per a mantenir un historial ordenat d'esdeveniments. En sistemes Linux, generalment s'utilitza el programa logrotate per a la rotació de logs. Aquest programa permet comprimir i arxivar registres antics, a més de configurar quan i com s'han de girar els logs.

En Apache2, la configuració de rotació de logs es troba en arxius específics dins del directori /etc/logrotate.d/. Pots trobar un arxiu de configuració per a Apache2, generalment dit apache2, que defineix com s'han de girar els logs de Apache2. El contingut de l'arxiu sol ser similar al següent:
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/e24ead3a-5731-4b2a-b0ce-926b44a72f8a)

Aquesta configuració diu que els arxius de registre en /var/log/apache2/ es giraran setmanalment (weekly) i es conservaran 52 còpies anteriors (rotate 52). Els *logs es comprimiran (compress) i el servidor Apache2 es recarregarà després de la rotació perquè comenci a escriure en nous arxius de registre.

### Monitoratge en temps real:

Pots utilitzar l'eina tail -f per a monitorar en temps real els accessos i errors en els arxius de registre de Apache2. Per exemple:

tail -f /var/log/apache2/access.log
tail -f /var/log/apache2/error.log

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/e78c5804-d704-403e-8ed1-eed706aa9cb6)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/32ce1b88-15ba-4180-8200-c6a1d0862d81)

Això mostrarà les últimes entrades en els arxius i continuarà mostrant noves entrades a mesura que es generin.

### Anàlisi de logs:

Per a analitzar i obtenir estadístiques visuals a partir dels logs de Apache2, pots utilitzar eines com GoAccess. Per a instal·lar GoAccess, pots utilitzar el gestor de paquets del teu sistema (per exemple, apt-get, yum, brew, etc.). Una vegada instal·lat, pots executar-ho en l'arxiu de registre d'accés de Apache2 de la següent manera:

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/0f03c9c5-29f1-4091-a36d-b81aa3bfbc53)

He clicat d per tenir el format d'hora.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/01e0ca4b-d9f6-4bde-9ff4-cc11f7561d21)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/7b926102-4b9b-438e-9f0c-4d30257fdea3)

Aquí es poden veure estadistiques.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/767145a7-4544-49fe-8297-300032bb70ae)
