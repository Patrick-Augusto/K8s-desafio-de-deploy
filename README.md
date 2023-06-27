# K8s-desafio-de-deploy


## Descrição

O K8s-desafio-de-deploy é um repositório que contém um desafio de implantação usando o Kubernetes (K8s). O objetivo deste projeto é demonstrar a implementação e implantação de uma aplicação em um cluster do Kubernetes. Ele abrange várias etapas, incluindo configuração do ambiente, definição dos recursos do Kubernetes, criação e implantação da aplicação.

A aplicação é um formulário de feedback simples que permite aos usuários enviar seus nomes, endereços de e-mail e comentários. Os dados do formulário são salvos em um banco de dados MySQL.

## Pré-requisitos

Antes de começar, verifique se você atende aos seguintes requisitos:

- Kubernetes (K8s) cluster configurado e acessível.
- Ferramentas de linha de comando do Kubernetes (kubectl) instaladas e configuradas corretamente.
- Servidor MySQL configurado e acessível.

## Instalação

Siga as etapas abaixo para instalar e executar o projeto em seu ambiente local:

1. Clone o repositório em sua máquina local:

   ```bash
   git clone https://github.com/Patrick-Augusto/K8s-desafio-de-deploy.git
   ```

2. Certifique-se de ter acesso ao cluster do Kubernetes e que o comando `kubectl` esteja configurado corretamente para se conectar ao cluster.

3. Configure o servidor MySQL com as credenciais corretas e crie o banco de dados necessário.

4. Atualize o arquivo `BackEnd/Conexao.php` com as informações de conexão corretas para o seu servidor MySQL.

5. Navegue até o diretório do projeto:

   ```bash
   cd K8s-desafio-de-deploy
   ```

6. Aplique a configuração do Kubernetes executando o seguinte comando:

   ```bash
   kubectl apply -f config/
   ```

7. Verifique se os recursos do Kubernetes foram criados corretamente:

   ```bash
   kubectl get deployments
   kubectl get services
   ```

8. Acesse a aplicação no navegador usando o endereço fornecido pelo serviço.

## Estrutura do Projeto

A estrutura do projeto é a seguinte:

```
K8s-desafio-de-deploy
├── BackEnd
│   ├── Conexao.php
│   └── index.php
├── FrontEnd
│   ├── css.css
│   ├── index.html
│   └── js.js
├── config
│   ├── deployment.yaml
│   └── service.yaml
└── app
    └── index.html
```

- `BackEnd`: Contém os arquivos do backend da aplicação, responsável por lidar com a persistência de dados no banco de dados MySQL.
- `FrontEnd`: Contém os arquivos do frontend da aplicação, incluindo CSS, HTML e JavaScript.
- `config`: Contém os arquivos de configuração do Kubernetes.
  - `deployment.yaml`: Define o Deployment da aplicação.
  - `service.yaml`: Define o Service da aplicação.
- `app`: Contém os ar

quivos do aplicativo, incluindo uma versão estática do formulário HTML para referência.



## Licença

Este projeto é licenciado sob a [MIT License](LICENSE).
