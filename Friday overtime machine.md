Lo primero que realizamos es ingresar en la maquina virtual con los datos y la contraseña que nos brindan al inicio.

En el ejemplo se da el caso como si estuviésemos a punto de salir del trabajo un viernes sin embargo nos llega un ticket de un colaborador de una empresa el cual creemos que se trata de un malware por lo que seguimos los siguientes pasos

1. Descargamos los ejemplos del malware que nos brindaron en el ticket, asegurándonos de que sea en un ambiente controlado
2. Luego ejecutamos el malware en un analizador de malware automatizado y que nos brinde un rápido análisis del malware.
3. Luego procedemos con un análisis manual que nos ayudara a entender el comportamiento del malware e identificando sus patrones de comunicación 
4. correlacionamos los hallazgos con bases de datos de inteligencia de amenazas globales para identificar firmas o comportamientos conocidos 
5. Por ultimo la compilación de un informe amplio con medidas de mitigación y recuperación, asegurándonos de que swiftspend pueda abordar rápidamente las amenazas potenciales  

En el correo que recibimos en nuestro buzón podemos notar que las muestras del malware son compartidas por el compañero *Oliver Bennett

Luego de eso nos vamos a la terminal de donde procedemos a abrir el archivo que descargamos para el analisis con los siguientes comandos 
 1. ls
 2. cd Downloads 
 3. unzip samples.zip
 4. ingresamos la contraseña
 5. sha1sum pRsm.dll 
 6. 9d1ecbbe8637fed0d89fca1af35ea821277ad2e8 

Para conseguir la respuesta de la siguiente pregunta tendríamos que dirigirnos a nuestro buscador de internet en el cual nos dirigimos a virustotal donde buscamos el hash que logramos conseguir antes y nos arroja los siguientes resultados:
Popular threat label [](https://www.virustotal.com/gui/search/engines:trojan AND engines:mgbot AND engines:fragtor AND engines:hgdbj) [trojan.mgbot/fragtor]

Luego seguimos buscando en nuestro buscador de internet y buscamos noticias o información de pRsm.dll encontramos una pagina que se llama We live Security que si lo leemos podemos encontrar la siguiente respuesta:
|[T1123](https://attack.mitre.org/versions/v12/techniques/T1123)|Audio Capture|MgBot’s plugin module pRsm.dll captures input and output audio streams.|

en dicha pagina al inicio podemos seguir con la siguiente respuesta ya que se muestra el URL sin embargo la pregunta es cual es la url defanged por lo que utilizamos la url que encontramos en la pagina web anterior y nos vamos a defang url ingresamos dicha url y el resultado es: hxxp[://]update[.]browser[.]qq[.]com/qmbs/QQ/QQUrlMgr_QQ88_4296.exe

Ahora lo mismo con la dirección IP solo buscamos la que sea con fecha 2020-09-14 y procedemos con el defang ip addresses: 122[.]10[.]90[.]12

Luego buscar la IP anterior del servidor C2 en el virustotal donde podemos encontrar las relaciones de esta IP en la sesión de relaciones y hacer clic en el enlace de nombre de Android y obtener el hash SHA1 de spyware en Detalles sesión: 1c1fe906e822012f6235fcc53f601d006d15d7be



Maquina concluida 



