---
name: Corrección ejercicio
about: Rúbrica de corrección
title: Corrección
labels: ''
assignees: ''

---

Parte 1 - (2,5 puntos) debe contener:

- [ ] Dashboard de Elastic Beanstalk
- [ ] Resultados de realizar una solicitud
- [ ]  Conexión de New Relic y métricas obtenidas
- [ ] Prueba de carga seleccionada y justificacion. Como no se dan datos sobre la cantidad de usuarios concurrentes, la prueba debería ser de estrés para determinar la carga media.
- [ ]  Logs de cloudwatch y opcionalmente mejoras

Parte 2
(2,5 puntos) Propuesta de nueva arquitectura. La opción más razonable parece ser la escalabilidad horizontal (la mejor) o vertical (solo dimensionando bien la carga). La alternativa de usar un worker no es la ideal porque se responde al request sin que la contraseña se haya cambiado. Se podría utilizar un hook para consultar si la misma se cambió, pero la seguridad se puede ver comprometida.

- [ ]  escalabilidad horizontal
- [ ]  escalabilidad vertical
