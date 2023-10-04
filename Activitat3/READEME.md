## Ex 1
El modul mod_info s'utilitza per obtenir informació detallada de la configuració i l'estat del servidor Apache. Aquí et deixo els passos per a seguir per instalar-lo.
Accedeix a la teva màquina virtual i acedeix a superusuari (root) o permisos de sudo per a fer canvis en la configuració del servidor Apatxe.

Verifica l'existència del mòdul: Abans d'habilitar el mòdul, verifica si ja està instal·lat en el teu servidor Apatxe. Pots fer-ho executant el següent comando:
apache2ctl -M | grep info_module

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/a1560adf-23dd-470f-95b2-386228e421a1)

Si veus una línia que conté "info_moduli (shared)", això significa que el mòdul mod_info ja està instal·lat.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/c8c939bf-6972-472f-a3fd-8334942406d5)

No existeix el modul.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/9ac5be44-c2dd-4583-b1f0-21784363607f)

Reiniciem Apache

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/5d554f77-c075-474a-b80e-96820722e3b7)

Accedeix a la informació del servidor: Una vegada que hagis habilitat el mòdul, pots accedir a la informació del servidor
en el teu navegador web utilitzant la URL http://direccioIP/server-info. Reemplaça "direcció IP" amb l'adreça IP o el nom de domini de la teva màquina virtual.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/5b1dfb99-9e87-45c6-a2db-3076b05b75db)

## EX 2

Quan obres localhost, entra a index.html per defecte.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/eadddaf4-d483-4faf-ae70-5c09885beed2)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/10b80c90-29ac-41f3-97d7-6d62fa97cb1e)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/ab824ed0-7fe8-4de8-97ff-8c8c36756560)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/22638131-5f66-4f17-8101-27d2d5448954)

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/8d070471-8e73-49ce-abfe-dfa95bff248a)

