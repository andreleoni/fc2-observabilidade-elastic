Antes de executar o docker-compose up, crie a rede observability com o comando

`docker network create observability`

Também é necessário criar a pasta elasticsearch_data no fc2-observabilidade-elastic na máquina local manualmente para evitar erro de permissionamento

`mkdir elasticsearch_data`

Execute os seguintes comandos:

`sudo chown root beats/metric/metricbeat.yml`
`sudo chown root apm/apm-server.yml`

Caso ocorra o erro

`bootstrap check failure [1] of [1]: max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]`

Execute o comando

`sysctl -w vm.max_map_count=262144`
