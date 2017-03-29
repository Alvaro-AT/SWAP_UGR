# Ejercicio 5. Probar las diferentes maneras de redirección HTTP. ¿Cuál es adecuada y cuál no lo es para hacer balanceo de carga global? ¿Por qué?
Para indicar redireccionamiento, se pueden usar varios **códigos de estado HTTP**: 301, 302, 303, 307 y 308.  
  
Los dos primeros corresponden la la versión 1.0 de HTTP en adelante. El primero indica que la redirección es permanente y se puede guardar en caché. El segundo, que la redirección es temporal y no se puede guardar en caché por defecto. Esta es la recomendada si queremos tener varios servidores o páginas para mostrar en función de la localización del cliente, ya que la web principal no se vería afectada. Además ofrece mayor compatibilidad que 303 y 307.  
Los otros tres corresponden a la versión 1.1 de HTTP. Tanto 303 como 307 indican que la redirección es temporal. La diferencia entre ambos es que 303 nunca se puede guardar en caché, mientras que 307 no se guarda por defecto.  
Por último, 308 se utiliza para indicar redirecciones permanentes y se guarda en caché por defecto.  

Por otro lado, la redirección se puede realizar en varios lenguajes, como HTML, JavaScript o PHP.  
En **HTML** sería algo tal que así: `<meta http-equiv="Refresh" content="0; url=http://www.urlnueva.com/" />`  
La forma para hacerlo en **JavaScript** es mediante `window.location.replace('http://www.urlnueva.com/')`  
Desde el lado del servidor, se utiliza **PHP** con la función *header( )*:  
`header('HTTP/1.1 301 Moved Permanently');`  
`header('Location: http://www.urlnueva.com/');`  
`exit();`