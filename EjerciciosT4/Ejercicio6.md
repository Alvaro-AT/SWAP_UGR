# Ejercicio 6. Buscar información sobre los bloques de IP para los distintos países o continentes. Implementar en JavaScript o PHP la detección de la zona desde donde se conecta un usuario.
En la web de **IPDeny** ([Enlace](http://www.ipdeny.com/ipblocks/)) podemos encontrar los bloques de IP correspondientes a cada país.  
  
Podemos usar una **API** que nos devuelva la información en formato **JSON**. Esta es la mejor que he encontrado, ofreciendo un máximo de 150 consultas al minuto:  

`$.getJSON('//ip-api.com/json?callback=?', function(data) {`  
	`console.log(JSON.stringify(data, null, 2));`  
`});`  
  
Nos devuelve lo siguiente:  
  
`{`  
  `"as": "AS198096 Junta de Andalucia",`  
  `"city": "Granada",`  
  `"country": "Spain",`  
  `"countryCode": "ES",`  
  `"isp": "Junta de Andalucia",`  
  `"lat": 37.1784,`  
  `"lon": -3.5992,`  
  `"org": "Universidad de Granada",`  
  `"query": "150.214.205.69",`  
  `"region": "AN",`  
  `"regionName": "Andalusia",`  
  `"status": "success",`  
  `"timezone": "Europe/Madrid",`  
  `"zip": "18001"`  
`}`