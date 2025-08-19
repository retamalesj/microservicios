# INF326 T1 Arquitectura de Software
- Pablo Retamales Jara ROL: 202173650-6

## Link al video
[Ver video: INF326: Tarea 1 Microservicios](https://www.youtube.com/watch?v=GYvWnsVu_Lg)

## Instrucciones

    1. Antes de todo, crear una red 'demo_01' en la terminal para habilitar la network de Docker que se usa en el proyecto:
        1.1 docker network create demo_01
    
    2. Para ejecutar logging (Loki, Promtail y Grafana):
        2.1 cd logging
        2.2 docker compose up

    3. Para ejecutar service_01 (Jugadores)
        3.1 cd service_01
        3.2 docker compose up
    
    4. Para ejecutar service_02 (Equipos)
        4.1 cd service_02
        4.2 docker compose up

    5. Luego, para entrar en la UI de Grafana:
        5.1 Ir a Connections y agregar Loki como Data Source, definir la URL de Loki, en este caso: http://loki:3100

        5.2 Crear una Dashboard usando Loki y correr una query filtrando un 'job' o un 'filename', idealmente { job = docker-logs } que sigue la configuración de etiqueta definida en 'promtail-config.yml'
    
## Muchas gracias!