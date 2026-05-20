# Zabbix com Docker Compose

Stack completa do Zabbix 6.4 com Docker Compose — servidor, banco de dados, Java Gateway, interface web e agente, prontos para subir com um único comando.

## Stack

- **Zabbix Server** — core de coleta e processamento
- **Zabbix Web (nginx)** — interface de gerenciamento
- **Zabbix Agent** — monitoramento do host local
- **Zabbix Java Gateway** — monitoramento de aplicações JMX
- **MySQL 8.0** — banco de dados com volume persistente

Todas as imagens Zabbix utilizam a variante `alpine-6.4-latest`.

## Pré-requisitos

- Docker
- Docker Compose

## Como usar

```bash
git clone https://github.com/rafaelmotadasilva/zabbix-docker-compose.git
cd zabbix-docker-compose

docker compose up -d
```

Acesse a interface web:

```
http://localhost
```

Login padrão: `Admin` / `zabbix`

## Portas expostas

| Serviço | Porta |
|---|---|
| Interface Web | 80 |
| Zabbix Server (trapper) | 10051 |

## Volumes persistentes

| Volume | Conteúdo |
|---|---|
| `mysql-data` | Dados do banco |
| `alertscripts` | Scripts de alerta customizados |
| `externalscripts` | Scripts externos |
| `modules` | Módulos do Zabbix |
| `ssh_keys` | Chaves SSH para checks remotos |
| `snmptraps` | Traps SNMP recebidos |

## Configuração padrão

| Variável | Valor |
|---|---|
| Banco de dados | zabbix |
| Usuário DB | zabbix |
| Senha DB | zabbix_pwd |

> Altere as credenciais no `docker-compose.yml` antes de usar em produção.

## Parar os containers

```bash
docker compose down
```
