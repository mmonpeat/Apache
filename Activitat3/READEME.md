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

Quan obres localhost, entra a index.html per defecte, llavors he canviat la pàgina que surt d'Ubuntu per aquesta.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/eadddaf4-d483-4faf-ae70-5c09885beed2)

Hemposat l'arxiu index.html en la carpeta inc, llavors al fer http://localhost es veu aquesta imatge. Es pot veure que a baix surt Apache Server at localhost Port 80.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/10b80c90-29ac-41f3-97d7-6d62fa97cb1e)

Entrem a security.conf i canviem les lineas ServerTokens i ServerSignature. Per acabar reiniciem Apache.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/22638131-5f66-4f17-8101-27d2d5448954)

Per aconseguir que no es vegi el comentari canviem l'arxiu d'aquesta manera.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/ab824ed0-7fe8-4de8-97ff-8c8c36756560)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/8d070471-8e73-49ce-abfe-dfa95bff248a)

Per que és vegi la versió completa de Apache, inclossos detalls com el número de la versió i el sistema operatiu en las respostas HTTP, posem:

ServerTokens Full

ServerSignature On

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/f673d286-72a8-4032-93d8-bc1d782053b9)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/55539f48-9f17-4ab5-af13-03e614b7944b)


ServerTokens Min

ServerSignature On

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/2f4f4c33-4f63-42b3-b16f-6d80199474d7)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/3cf258c4-9423-456b-8333-a974f4a648f8)

## EX 3

Creem les carpetes en l'arrel del path, amb sudo mkdir. (en /var/www/html) no en /
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/bca81598-cd25-4fdd-9678-15df613565c5)

Per tenir permisos d'escritura(AllowOverrite) anem a /etc/apache2 entrem en l'arxiu apache2.conf i canviem el None per un All.
Després amb l'arxiu .htaccess canviatem les Options.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/305b850b-237a-4bc7-bf92-0ef90937da4f)

No posem res en el directori public

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/ee6ae80b-ac8b-4a43-a9a9-dfa508ffc1b0)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/30e547b0-89d8-4213-a4d6-2f86b2b0c374)

Encanvi en el directori private creem l'arxiu ocult htaccess.

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/366228b3-c35e-4bf0-b65c-9174a7b29c3c)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/48f1985a-a9e2-47a4-afd5-4fcf8f6b95fc)

## EX 4

So si funciona, crec que es per que a l'activitat anterior encontes d'usat htacces vaig usar un mòdul.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/ee6c22c6-1538-4cbf-a085-d9bb337df408)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/c9f7bfda-7386-4b03-b6b4-d85e8aab3254)

## EX 5

Utilitzarem el tema que ens donen, encata que podriem fer-nos la nostra plantilla personalitzada.
LLavors ens decaregem el repositori i movem el 'directory-listing' al directori root d'Apache, es a dir a /etc/apache2.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/8c9713c8-ebd7-4de7-87c4-238c5e26e266)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/6eeaeaec-89d9-429b-92f1-71f049c542da)

Copiem htaccess.txt al directori root del server, anomentant'l-ho .htaccess.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/7dbb77df-c4ee-4e94-bdd0-2045a4c54d6c)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/f4ec1a1d-728d-4247-84d5-07540f244a87)

Ha d'estar a la ruta /var/www/html. M'havia equivocat i ho he canviat.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/efe1d19e-b42a-465b-a37f-47db0aeb6819)


Canviem {LISTING_DIRECTORY} per la localització(ruta) del directori directory-listing.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/6f77bdb0-6bd6-4fc0-b13f-cba69f2ed40e)

Canviem {LISTING_STYLE} per algún estil d'aquest: grid, table, grid-darkmode, table-darkmode, grid-automode, or table-automode.
grid-automode i table-automode canviaran automàticament entre els temes clars i foscos segons els paràmetres del SO o del navegador de l'usuari.
Ho he canviat tot a mà per qué no he pogut amb el sed :(
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/f10c36fc-ce85-406d-8dcc-58a63677985f)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/0133226e-beed-4c8b-9a8c-ee5e6fffb027)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/c550ec52-6060-4e59-9d77-fdb522ab0409)


És canvia el estil, amb table-automode però no queda bonic, i el table-darkmode hem fa el mateix.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/dd9bc236-0ee2-424f-a6fb-465b21dd7821)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/ae27179c-3372-4349-aae5-b987631c14e8)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/54a96a8b-d31a-48ac-80e2-56f3a252dd09)

## EX 6
He creat una carpeta que es diu mi-tema-apache, dins he creat un arxiu html i he posat aquest codi.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/e1767adb-92ac-414b-b0ec-c3c65ed6b577)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/0ab41fb2-cfff-455a-86ac-fa2f3bdaaeed)

Aquest arxi, la part del codi senyalat ha d'estar així.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/75aef9bc-6275-47f3-8910-983b39170120)

Si anem al directori mi-tema-apache podem veure que s'ha fet la pagina correctament.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/5d6a7905-ef07-4df7-9d3e-d6e8fcf3d244)
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/102a4656-d768-4d31-b7cc-9f3f7a4fcdf3)

També funciona amb www.localhost.
![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/6002de5d-7d03-4149-91a1-25149f65307b)



