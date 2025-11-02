# 🧩 Introduction to Kubernetes

> * Repositório de estudos pessoais sobre Kubernetes

---

## 📘 Sobre o Projeto

Este repositório tem como objetivo armazenar **manifests YAML** e exemplos práticos de uso do **Kubernetes (K8s)**.  
A ideia é servir como **material de estudo pessoal**, facilitando o aprendizado de conceitos fundamentais de containers, pods, deployments, services, volumes e outros recursos do K8s.

---

## 📂 Estrutura do Repositório

| Arquivo / Diretório         | Descrição |
|-----------------------------|-----------|
| `cluster.yml`               | Configuração de cluster / exemplo base |
| `deploy-configmap.yml`      | Exemplo de Deployment com uso de ConfigMap |
| `deployment.yml`            | Deployment básico de aplicação |
| `index.html`                | Página simples usada em algum pod ou serviço |
| `mybd-secret.yml`           | Exemplo de Secret (credenciais) |
| `mybd.yml`, `mybd2.yml`     | Exemplos de banco de dados (Pods ou Deployments) |
| `myweb.yml`                 | Aplicação web e respectivo serviço |
| `pod.yml`                   | Definição direta de um Pod |
| `service.yml`               | Serviço para expor aplicação |
| `serviceconfigmap.yml`      | Serviço que utiliza ConfigMap |
| `statefulset.yml`           | StatefulSet para aplicações com estado |
| `volume.yml`                | Configuração de volumes persistentes |
| `volumeintroduction.yml`    | Introdução prática ao uso de volumes |

---

## ⚙️ Pré-requisitos

Antes de aplicar os manifests, é importante ter:

- Um **cluster Kubernetes** (local ou remoto). Pode usar:
  - [Minikube](https://minikube.sigs.k8s.io/docs/start/)
  - [Kind](https://kind.sigs.k8s.io/)
  - [K3s](https://k3s.io/)
  - Docker Desktop (com Kubernetes habilitado)
- **Kubectl** instalado e configurado corretamente.  
  [Guia de instalação do kubectl](https://kubernetes.io/docs/tasks/tools/)

---

## 🚀 Como Usar

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/Sc4rlxrd/Introduction-to-K8s.git
   cd Introduction-to-K8s
   ```

2. **Aplique os manifests no seu cluster:**
   ```bash
   kubectl apply -f .
   ```

3. **Verifique os recursos criados:**
   ```bash
   kubectl get pods
   kubectl get svc
   kubectl get deployments
   kubectl get statefulsets
   ```

4. **Acesse a aplicação (se aplicável):**
   - Caso use `NodePort`, descubra a porta com:
     ```bash
     kubectl get svc
     ```
   - Acesse via `http://localhost:<porta>`

---

## 📄 Licença

Distribuído sob a licença **MIT**.  
Consulte o arquivo `LICENSE` para mais detalhes.

---

## 👨‍💻 Autor

**Guilherme dos Santos**  

> “Aprender Kubernetes é dominar a base da orquestração moderna de containers.”
