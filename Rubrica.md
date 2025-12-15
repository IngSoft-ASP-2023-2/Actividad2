# Rúbrica de corrección
## Parte 1
Esta sección (3,5 puntos) debe contener:
- [ ] Dashboard the Elastic Beanstalk
- [ ] Resultados de realizar una solicitud
- [ ] Conexion de new relic y metricas obtenidas
- [ ] Prueba de carga seleccionada y justificacion. como no se dan datos sobre la cantidad de usario concurrentes la prueba debería ser de estrés para determinar la carga media
- [ ] Logs de cloudwatch y opcionalmente mejoras

## Parte 2 
(1,5 puntos) Propuesta de nueva arquitectura. La opción mas razonable parece ser la escalabilidad horizontal (la mejor) o vertical (solo dimensionando bien la carga). La alternativa de usar un worker no es la ideal porque se responde al request sin que la 
contraseña se haya cambiado. Se podria utilizar un hook para consultar si la misma se cambió pero la seguridad se puede ver comprometida.
- [ ] escalabilidad horizontal
- [ ] escalabilidad vertical

