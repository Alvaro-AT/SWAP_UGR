# Ejercicio 1. Aplicar con iptables una política de denegar todo el tráfico en una de las máquinas de prácticas. Comprobar el funcionamiento. Aplicar con iptables una política de permitir todo el tráfico en una de las máquinas de prácticas. Comprobar el funcionamiento.
Para bloquear todo el tráfico, introducimos las siguientes reglas:  
`iptables -F`  
`iptables -X`  
`iptables -P INPUT DROP`  
`iptables -P OUTPUT DROP`  
`iptables -P FORWARD DROP`  
Para aceptar todo el tráfico, cambiamos las tres últimas reglas anteriores por las siguientes:  
`iptables -P INPUT ACCEPT`  
`iptables -P OUTPUT ACCEPT`  
`iptables -P FORWARD ACCEPT`  

Cuando bloqueamos el tráfico, perdemos el acceso a la máquina virtual. Si borramos las reglas y/o aceptamos el tráfico, volvemos a tener acceso. 