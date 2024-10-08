# Zabbix com Docker Compose

Este projeto oferece uma configuração Docker Compose para o Zabbix, simplificando sua implantação em contêineres Docker e permitindo monitorar e gerenciar a infraestrutura de TI de forma eficiente.

## Visão Geral

Ele inclui os componentes essenciais, como servidor, banco de dados e interface web. Assim, é possível implantar o Zabbix rapidamente e começar a monitorar sua infraestrutura sem complicações.

## Requisitos

* Docker Compose

## Instruções

1. [Clone este repositório](#clone-este-repositório)
2. [Navegue até o diretório do projeto](#navegue-até-o-diretório-do-projeto)
3. [Inicie os contêineres](#inicie-os-contêineres)
4. [Acesse o Zabbix](#acesse-o-zabbix)
5. [Faça login](#faça-login)
6. [Para parar os contêineres](#para-parar-os-contêineres)
7. [Conclusão](#conclusão)

## Clone o repositório

```
git clone https://github.com/rafaelmotadasilva/zabbix-docker-compose.git
sudo docker-compose up -d
```

## Execute os contêineres

```
sudo docker-compose up -d
```

## Acesse o Zabbix

Abra seu navegador e acesse http://host. Você será redirecionado para a página padrão para a interface do usuário do Zabbix.

## Faça login:

- **Usuário:** Admin
- **Senha:** zabbix

## Para parar os contêineres

```bash
docker-compose down
```

## Conclusão

Este projeto simplifica a implantação do Zabbix em contêineres Docker, permitindo monitorar e gerenciar sua infraestrutura de TI de forma eficiente.

## Contribuição

Se você tiver sugestões de melhorias ou correções para este guia, sinta-se à vontade para enviar uma pull request.

## Referências

* [Documentação oficial do Zabbix - Instalação em Contêineres](https://www.zabbix.com/documentation/current/pt/manual/installation/containers)
* [Repositório oficial do Zabbix Docker](https://github.com/zabbix/zabbix-docker/)

## Licença

Este projeto está licenciado sob a [Licença MIT](LICENSE).