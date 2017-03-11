# Ejercicio 1. Calcular la disponibilidad del sistema si tenemos dos réplicas de cada elemento (en total 3 elementos en cada subsistema).
- **Web** = 97.75% + ( ( 1 - 97.75% ) * 85% ) = **99.6625%**
- **Aplicación** = 99% + ( ( 1 - 99% ) * 90% ) = **99.9%**
- **Base de datos** = 99.9999% + ( ( 1 - 99.9999% ) * 99.9% ) = **99.9999999%**
- **DNS** = 99.96% + ( ( 1 - 99.96% ) * 98% ) = **99.9992%**
- **Firewall** = 97.75% + ( ( 1 - 97.75% ) * 85% ) = **99.6625%**
- **Switch** = 99.99% + ( ( 1 - 99.99% ) * 99% ) = **99.9999%**
- **Data Center** = 99.99% + ( ( 1 - 99.99% ) * 99.99% ) = **99.999999%**
- **ISP** = 99.75% + ( ( 1 - 99.75% ) * 95% ) = **99.9875%**