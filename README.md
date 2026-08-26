<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:2496ED&height=170&section=header&text=Docker%20e%20Kubernetes&fontColor=ffffff&fontSize=44&fontAlignY=36&desc=Reposit%C3%B3rio%20de%20estudos%20e%20laborat%C3%B3rios&descSize=17&descAlignY=58" width="100%" alt="banner" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />
<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/YAML-CB171E?style=for-the-badge&logo=yaml&logoColor=white" />

<br />

<img src="https://img.shields.io/badge/status-em%20andamento-2563EB?style=flat-square" />
<img src="https://img.shields.io/github/last-commit/Iago-Vargas/docker-kubernetes?style=flat-square&color=475569" />
<img src="https://img.shields.io/github/languages/top/Iago-Vargas/docker-kubernetes?style=flat-square&color=475569" />

</div>

---

## 📌 Sobre este repositório

Este repositório concentra **todos os meus estudos, anotações e laboratórios sobre containers e orquestração**, feitos ao longo de um curso de Docker e Kubernetes.

A ideia não é guardar só o código das aulas, mas construir um material que eu (ou qualquer pessoa) consiga reabrir daqui a seis meses e entender **o que foi feito, por que foi feito e o que deu errado no caminho**.

---

## 🗂️ Como o repositório é organizado

Cada aula tem uma **branch própria** e uma **pasta própria**, seguindo um padrão fixo:

| Item | Padrão | Exemplo |
|:--|:--|:--|
| Branch | `aula/NN-slug-do-tema` | `aula/07-docker-compose` |
| Pasta | `aulas/NN-slug-do-tema/` | `aulas/07-docker-compose/` |
| Commit | `aula(NN): descrição curta` | `aula(07): sobe stack com app e mysql` |

```text
.
├── aulas/
│   ├── 01-introducao-containers/
│   │   ├── README.md          <- anotações da aula
│   │   └── comandos.sh
│   ├── 02-primeira-imagem/
│   │   ├── README.md
│   │   ├── Dockerfile
│   │   └── app/
│   └── ...
├── cheatsheet/                <- comandos que eu sempre esqueço
├── labs/                      <- exercícios livres, fora do roteiro do curso
└── README.md
```

Cada pasta de aula tem seu **próprio `README.md`** com:
- o conceito trabalhado, escrito com minhas palavras
- os comandos executados
- prints ou saídas relevantes do terminal
- 🧠 **o que travou** e como resolvi

---

## 📚 Progresso

### 🐳 Docker

- [x] Fundamentos de containers e diferença para VMs
- [x] Imagens, camadas e `Dockerfile`
- [ ] Volumes e persistência de dados
- [ ] Redes e comunicação entre containers
- [ ] Docker Compose
- [ ] Registry e publicação de imagens
- [ ] Boas práticas: multi-stage build, imagens enxutas, segurança

### ☸️ Kubernetes

- [ ] Arquitetura do cluster (control plane e nodes)
- [ ] Pods, ReplicaSets e Deployments
- [ ] Services e descoberta de serviços
- [ ] ConfigMaps e Secrets
- [ ] Volumes, PV e PVC
- [ ] Ingress e roteamento externo
- [ ] Escalonamento e health checks
- [ ] Helm
- [ ] Observabilidade e troubleshooting

---

## 🚀 Rodando os exemplos

**Pré-requisitos:**

```bash
docker --version      # Docker Engine 24+
docker compose version
kubectl version --client
minikube version      # ou kind, k3d
```

**Clonando e navegando até uma aula:**

```bash
git clone https://github.com/Iago-Vargas/docker-kubernetes.git
cd docker-kubernetes

# ver todas as aulas disponíveis
git branch -a

# entrar em uma aula específica
git switch aula/07-docker-compose
cd aulas/07-docker-compose
```

Cada pasta traz no seu README as instruções exatas de execução daquele exemplo.


---

## 🎯 Por que estou estudando isso

Trabalho com **Laravel sobre infraestrutura Proxmox e Ceph**, e containers são a peça que conecta os dois mundos: padronizar o ambiente de desenvolvimento, isolar dependências em pipelines de CI/CD e, mais adiante, orquestrar cargas de trabalho de forma reproduzível.

Este repositório é o registro dessa transição de "sei usar Docker" para "entendo o que acontece por baixo".


---

<div align="center">

<sub>Repositório de estudo pessoal ·</sub>

</div>
