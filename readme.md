# Kubernetes WordPress Deployment

Este projeto configura um ambiente Kubernetes para hospedar um site WordPress com MySQL como banco de dados e phpMyAdmin para administração do banco. 
O objetivo é demonstrar uma implantação completa utilizando melhores práticas em um ambiente containerizado.

---

## Arquitetura

- **WordPress**: Serviço principal do site.
- **MySQL**: Banco de dados para o WordPress, configurado como um StatefulSet.
- **phpMyAdmin**: Interface gráfica para gerenciamento do banco de dados.
- **Persistent Volumes**: Garantem a persistência de dados tanto para o MySQL quanto para o WordPress.
- **Ingress**: Garante o acesso externos das aplicações.

---

## Estrutura do Projeto

- **`wordpress.yaml`**:
  - Configuração do Deployment, Service e PersistentVolumeClaim para o WordPress.
- **`mysql.yaml`**:
  - Configuração do StatefulSet, Service e PersistentVolumeClaim para o MySQL.
- **`phpmyadmin.yaml`**:
  - Configuração do Deployment e Service para o phpMyAdmin.
- **`ingress.yaml`**:
  - Configuração ingress para acesso externo da aplicação e do phpmyadmin
- **`namespace.yaml`**:
  - Configuração da namespace para que abrigará os recursos
- **`secrets.yaml`**:
  - Configuração dos secrets utilizados pelo projeto