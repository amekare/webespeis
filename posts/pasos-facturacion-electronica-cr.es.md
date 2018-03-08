# Pasos para facturación electrónica

Para quienes deseen usar la plataforma gratuita de facturación electrónica, hice una guía en este hilo que espero les ayude a aprender en menos tiempo que lo que me tomó a mí entenderlo #FacturaciónElectrónica

Cualquier persona puede voluntariamente facturar electrónicamente pero hay un calendario de obligaciones por sector productivos o giro comercial según su código de inscripción en Tributación. Véanlo [aquí](http://www.hacienda.go.cr/docs/59cebb7657f59_Aviso%20Comunicacion%20uso%20de%20comprobantes%20electronico.pdf)

Si no recuerdan en cuál actividad están inscritos, pueden confirmarlo y saber su código de actividad con su número de cédula (física o jurídica) [aquí](https://www.hacienda.go.cr/ATV/frmConsultaSituTributaria.aspx)

Si desean saber más sobre el fundamento legal del cambio, el documento [factura electrónica](http://www.hacienda.go.cr/contenido/14350-factura-electronica) y los [requisitos](http://www.hacienda.go.cr/contenido/13383-requisitos-de-las-facturas-o-comprobantes-de-ingresos), dan referencia a las resoluciones.

El primero paso es en la Adminstración [Tributaria Virtual](https://www.hacienda.go.cr/ATV/Login.aspx), igresando con su usuario y clave

![Imagen de login](https://github.com/ignacioalmar/webespeis/blob/guia-hacienda/posts/img/pasos-facturacion-electronica-cr/login.png)

Si perdieron alguno de estos datos pueden recuperarlo al correo con el que se registraron o por sms al teléfono indicando fecha de nacimiento y de vencimiento (de la cédula), no vencimiento de ustedes.

Si no saben ninguno, vayan personalmente a una Administración Tributaria y aprovechan la filota para meditar en cómo ser más ordenados.

Al ingresar a la ATV, digitan los códigos de la tarjeta virtual. Si no la tiene, generan otra que se las manda al correo. Si no recuerdan el correo o no pueden acceder, vayan personalmente a arreglar eso a alguna administración tributaria: http://www.hacienda.go.cr/contenido/13786-quioscos-tributarios

Si van a llamar, pues paciencia.. mucha paciencia... http://www.hacienda.go.cr/docs/552ea3e3554e5_TELEFONOS%20Y%20DIRECCION%20AATT.pdf

Si tienen su tarjeta virtual, digitan los códigos requeridos

![Imagen de login](https://github.com/ignacioalmar/webespeis/blob/guia-hacienda/posts/img/pasos-facturacion-electronica-cr/confirmar-tarjeta.png)


Una vez ingresados en la ATV, seleccionan si facturarán como personas físicas el perfil de obligado tributario. Si es como personas jurídicas (una sociedad anónima, por ejemplo), el perfil de representante legal. 

![Imagen de login](https://github.com/ignacioalmar/webespeis/blob/guia-hacienda/posts/img/pasos-facturacion-electronica-cr/seleccion-perfil.png)


Listo. Ojo que solo en el muñequito verde se activa el enlace.

![Imagen de login](https://github.com/ignacioalmar/webespeis/blob/guia-hacienda/posts/img/pasos-facturacion-electronica-cr/seleccion-perfil2.png)


Ingresados, seleccionan generar llave criptográfica.Eso se almacena en su equipo. Si van a compartir su computadora con varias, cada uno con su sesión y usuario, seleccionan este usuario, sino todos los usuarios.

![Imagen de login](https://github.com/ignacioalmar/webespeis/blob/guia-hacienda/posts/img/pasos-facturacion-electronica-cr/generar-llave-privada.png)

Luego de generar la llave, deben hacer un usuario y clave para envío de facturas, en ese mismo menú. Genera en pantalla un usuario y una clave. RE IMPORTANTE GUARDARLAS porque será necesaria para el último paso de la facturación (Enviar xml firmado)

![Imagen de login](https://github.com/ignacioalmar/webespeis/blob/guia-hacienda/posts/img/pasos-facturacion-electronica-cr/generar-contrasena.png)

Hay un video sobre cómo se genera y revoca la llave criptográfica y la clave y usuario https://www.youtube.com/watch?v=elhHdEUechs

El tercer paso, luego de la llave y del usuario y clave para envío de facturas es el firmador. ese es un programa adicional que hay que instalar MHFirma_Electrónica en http://www.hacienda.go.cr/contenido/14350-factura-electronica. Lo usual, aceptar, aceptar, aceptar y ya.


Con la llave, el usuario y clave y el firmador se puede ya pasar a facturar en el menú de Comprobantes Electrónicos (no se han salido del ATV, ¿cierto?) 

![Imagen de login](https://github.com/ignacioalmar/webespeis/blob/guia-hacienda/posts/img/pasos-facturacion-electronica-cr/facturar.png)


Ahora sí, a facturar: sus datos como emisor (sucursal sin descripción, sucursal 1 y caja 1 si no tienen realmente varias sucursales y cajas registradoras..), los de la persona que recibirá la factura o receptor  (cédula)...

Es de suma importancia que coloquen en la factura electrónica la información del receptor, con su nombre o cédula. No cometan el error de generarla sin esos datos ya que NO SE PUEDEN ELIMINAR FACTURAS HECHAS. NO SE PUEDEN ELIMINAR. NO SE PUEDE.

En el encabezado si es factura electrónica (o notas) y si es de contado y la moneda. Al guardar encabezado se abre el detalle de la factura que llenarán línea por línea.

Para la factura electrónica pueden usar códigos o solamente rellenar la descripción del servicio en “Descripción de la línea”, más la unidad de medida (SP), la cantidad y el precio y guardan la línea. Si son servicios será uno, claro, salvo que sean con precio por unidad.

![Imagen de login](https://github.com/ignacioalmar/webespeis/blob/guia-hacienda/posts/img/pasos-facturacion-electronica-cr/guardar-linea.png)
 
Una vez hecha la factura electrónica, deben solicitar validarla (aceptar)

![Imagen de login](https://github.com/ignacioalmar/webespeis/blob/guia-hacienda/posts/img/pasos-facturacion-electronica-cr/uno-dos.png)


Con la factura electrónica validada se genera una clave del documento (HASH) que hay que pegar en el firmador (ya vamos a eso) copiándola

![Imagen de login](https://github.com/ignacioalmar/webespeis/blob/guia-hacienda/posts/img/pasos-facturacion-electronica-cr/copiar-hash.png)

Con ese HASH copiado, abrimos el firmador (MHFirma_Electrónica) que ya debieron de haber instalado, pegar HASH y firmar, sea con firma digital o llave crIptográfica

![Imagen de login](https://github.com/ignacioalmar/webespeis/blob/guia-hacienda/posts/img/pasos-facturacion-electronica-cr/uno-dos-o-otrodos.png)

Una vez firmada, se envía el XML firmado y eso genera una factura electrónica lista en pdf para ser enviada al cliente

![Imagen de login](https://github.com/ignacioalmar/webespeis/blob/guia-hacienda/posts/img/pasos-facturacion-electronica-cr/enviar-xml-firmado.png)


Si están obligados a emitir este tipo de comprobantes y no lo hacen, la sanción es de dos Salarios Base (Salario Base cambia año a año; en 2018 es C. 431.000) Ver http://www.hacienda.go.cr/docs/58b8330a02620_Infraccionesysanciones.pdf

Si el sistema falla y no pueden emitir comprobantes pueden darle otro o factura pre-impresa (las de antes, advirtiendo que es temporal. http://www.hacienda.go.cr/docs/5a6f9e6a95922_Paso%20a%20Paso%20Comprobantes%20Electronicos.pdf

![Imagen de login](https://github.com/ignacioalmar/webespeis/blob/guia-hacienda/posts/img/pasos-facturacion-electronica-cr/cuando-utilice.png)

Si desean leer la historia larga de la facturación electrónica está en un manual de Tributación en este enlace http://www.hacienda.go.cr/docs/5a550c170342c_Manual%20de%20uso%20de%20la%20Herramienta%20Gratuita%20de%20Facturacion.pdf

Hay un resumen de los pasos para hacer facturación electrónica aquí http://www.hacienda.go.cr/docs/5a6f9e6ac664a_ABC%20para%20uso%20del%20Facturador%20Electronico%20del%20Ministerio%20de%20Hacienda.pdf

Es importante hacer notar que además de estas evidentes complicaciones y dificultades que hacen que pueda ser una experiencia de usuario frustrante, hay varias limitaciones técnicas en cuanto a sistemas operativos y otros.

Hecho por Ignacio Alfaro Marín
Publicado en https://twitter.com/instantepasado/status/971777192819679232

Sígueme en [![alt text][1.1]][1] [![alt text][2.1]][2]

[1.1]: http://i.imgur.com/tXSoThF.png
[2.1]: http://i.imgur.com/0o48UoR.png

[1]: http://www.twitter.com/instantepasado
[2]: http://www.github.com/ignacioalmar
