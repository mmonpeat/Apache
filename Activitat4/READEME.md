## Configuració del Servidor Web:

Utilitzem el servidor web d'Apache. Creem dos bolcs de configuració vitual (Virtual Hosts) en l'arxiu de configuració  del servidor. Un domini "daw.gimbernat.eug.es" i un altre "mmonpeat.gimbernat.eug.es".

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/0f1d104c-105c-49bb-932f-f834c3e7563a)

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/4b37dceb-49fd-41d8-a4fa-46b00eb80c2a)

## Configuració de DNS

Entrem a /etc/hosts

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/d0a5e91e-27e9-44c7-a464-649fce7839d5)

### daw

#### 000-default.conf

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/f17b23d0-72b7-4bcd-833f-ecddaf62b766)


#### index.html

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/f8af8892-ec3f-4dff-9ab9-fbb9c1d27d91)


#### estil.css

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/d3a1f388-68e8-4703-9b13-9128ca07e973)

sudo systemctl reload apache2

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/797f1b36-a556-417a-9cb7-3a09c5104b2d)


![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/ed2ec895-3dad-417c-a88f-00f47f825152)

### mmonpeat

#### 000-default.conf

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/b951a1eb-2568-45c9-aab1-27af177eb37d)


#### index.html

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/b88cfc36-b099-4214-90d2-2295e7e28fce)


#### estil.css

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/32195460-35e0-4d72-a67f-45b9ae7951ae)

sudo systemctl reload apache2

![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/797f1b36-a556-417a-9cb7-3a09c5104b2d)


![imatge](https://github.com/mmonpeat/Desplegament_Aplicacions_Web/assets/115364869/47166a40-2ebb-4177-b3fa-a2aeec087f5f)
