# Projeto kube-news

### Objetivo
O projeto Kube-news é uma aplicação escrita em NodeJS e tem como objetivo ser uma aplicação de exemplo pra trabalhar com o uso de containers.

### Configuração
Pra configurar a aplicação, é preciso ter um banco de dados Postgre e pra definir o acesso ao banco, configure as variáveis de ambiente abaixo:

DB_DATABASE => Nome do banco de dados que vai ser usado.

DB_USERNAME => Usuário do banco de dados.

DB_PASSWORD => Senha do usuário do banco de dados.

DB_HOST => Endereço do banco de dados.

## Executar no Kind

```bash
kind create cluster --config kind-config.yaml
kind delete cluster
```

## Deploy da aplicação no Kind
```bash
kubectl apply -f deployment.yaml

# listar todos os recursos
kubectl get all

# listar services
kubectl get services

# listar pods
kubectl get pods

# rollback
kubectl rollout undo deployment kubenews

# deletar 
kubectl delete -f deployment.yaml
```

