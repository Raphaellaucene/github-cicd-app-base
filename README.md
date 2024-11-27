# Projeto de Deployment de Aplicação Node.js
Este projeto demonstra um pipeline de deploy para uma aplicação Node.js em duas branchs chamadas Docker e Kubernetes.. A aplicação será implantada em um container Docker e em um cluster Kubernetes na nuvem, simulando o uso do Google Cloud Platform (GCP).

## Estrutura do Projeto
O projeto está estruturado em duas branches principais:

`docker`: Contém a configuração necessária para criar e executar a aplicação em um container Docker em máquina local, com propósito de um ambiente dev..

`kubernetes`: Contém a configuração para implantar a aplicação em um cluster Kubernetes utilizando o GCP.

## Funcionalidades
Pipeline de CI/CD: Automatiza o processo de build, teste e deploy da aplicação nas duas branches mencionadas.

branch docker: Inclui um Dockerfile para criar uma imagem da aplicação Node.js.

branch kubernetes: Inclui os manifests do Kubernetes (Deployments, Services, etc.) para a implantação no GCP.

Google Cloud Platform: Integração com o GCP para criar e gerenciar o cluster Kubernetes na nuvem.

## Requisitos:

*Docker*

*Kubernetes e kubectl*

*Conta no Google Cloud Platform*

*Node.js*

## Instruções de Uso

### Docker

1. Clone o repositório e navegue até a branch `docker`:
    ```sh
    git clone <URL do repositório>
    cd <nome do repositório>
    git checkout docker
    ```

2. Construa a imagem Docker:
    ```sh
    docker build -t minha-aplicacao-node .
    ```

3. Execute o container:
    ```sh
    docker run -p 3000:3000 minha-aplicacao-node
    ```

### Kubernetes

1. Clone o repositório e navegue até a branch `kubernetes`:
    ```sh
    git clone <URL do repositório>
    cd <nome do repositório>
    git checkout kubernetes
    ```

2. Configure seu ambiente GCP e crie um cluster Kubernetes:
    ```sh
    gcloud container clusters create meu-cluster
    ```

3. Aplique os manifests do Kubernetes:
    ```sh
    kubectl apply -f k8s/
    ```

4. Verifique os pods em execução:
    ```sh
    kubectl get pods
    ```

