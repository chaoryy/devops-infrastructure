# DevOps Infrastructure Repository

Учебный проект: инфраструктурный репозиторий с полным набором DevOps-инструментов — от контейнеризации до мониторинга.

# DevOps Infrastructure Repository

> Status: infrastructure ready, deployment in progress

## 🚀 Как развернуть

### 1. Сборка Docker-образа
```bash
docker build -t app:latest ./docker
docker run -p 3000:3000 app:latest
```

### 2. Развёртывание инфраструктуры (Terraform)
```bash
cd terraform
terraform init
terraform plan
terraform apply
```

### 3. Настройка серверов (Ansible)
```bash
ansible-playbook -i inventory ansible/playbook.yml
```

### 4. Деплой в Kubernetes
```bash
kubectl apply -f kubernetes/deployment.yaml
kubectl apply -f kubernetes/service.yaml
```

### 5. Мониторинг
Конфигурация Prometheus находится в `monitoring/prometheus.yml`. Запуск:
```bash
prometheus --config.file=monitoring/prometheus.yml
```
