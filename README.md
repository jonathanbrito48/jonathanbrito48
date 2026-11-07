<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=0:09090b,50:0f172a,100:09090b&height=160&section=header&text=Jonathan%20Brito&fontSize=38&fontColor=ffffff&fontAlignY=42&desc=Google%20Cloud%20Certified%20%7C%20Cloud%20Architect%20%26%20Data%20Engineer&descFontSize=15&descColor=38bdf8&descAlignY=68&stroke=1e293b&strokeWidth=1" width="100%" alt="Header" />
</div>

<div align="center">

[![Google Cloud PCA](https://img.shields.io/badge/Google%20Cloud-Certified%20Professional%20Cloud%20Architect-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)](https://www.credly.com/badges/251634f5-7ee6-4c1a-8322-dfdbfac9b3e4/public_url)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jonathan-loiola-brito/)
[![Portfolio](https://img.shields.io/badge/Live%20Portfolio-jbrito.cloud-10b981?style=for-the-badge&logo=vercel&logoColor=white)](https://portfolio-eight-pink-54.vercel.app/)

</div>

<br />

```bash
jonathan@gcp-cloud-shell:~$ gcloud profile describe --format="yaml"
```
```yaml
identity:
  name: "Jonathan Loiola Brito"
  role: "Cloud Architect & Data Engineer"
  certification: "Google Cloud Certified - Professional Cloud Architect"
  focus:
    - "Cloud-Native Infrastructure & Serverless (GCP)"
    - "Infrastructure as Code (Terraform) & Zero-Trust Security"
    - "Resilient Data Pipelines (Python, Pub/Sub, BigQuery)"
  status: "Available for Architecture & Engineering Consulting"
```

---

### 🌐 Overview & Engineering Background

Atuo no desenho e sustentação de **infraestruturas de nuvem resilientes e esteiras de dados de missão crítica**, com ênfase no ecossistema **Google Cloud Platform (GCP)**, automação declarativa com **Terraform** e engenharia de backend com **Python**.

> 💡 **Nota sobre os repositórios corporativos:**  
> Meus projetos em escala de produção enterprise (migrações multi-cloud, clusters GKE gerenciados, arquiteturas de mensageria com DLQ e data warehouses analíticos) estão hospedados em **organizações privadas sob NDA**. Este espaço pessoal abriga utilitários, estudos e PoCs.  
> 
> 🔗 Para inspecionar métricas de produção, diagramas e os cases de sucesso reais, acesse meu **[Portfólio Web](https://portfolio-eight-pink-54.vercel.app/)**.

---

### 🛠️ Core Stack & Tooling

<div align="center">

| Domínio | Tecnologias Principais |
| :--- | :--- |
| **Cloud & Serverless** | ![GCP](https://img.shields.io/badge/Google_Cloud-4285F4?style=flat-square&logo=google-cloud&logoColor=white) ![Cloud Run](https://img.shields.io/badge/Cloud_Run-4285F4?style=flat-square&logo=google-cloud&logoColor=white) ![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?style=flat-square&logo=google-cloud&logoColor=white) ![GCS](https://img.shields.io/badge/Cloud_Storage-4285F4?style=flat-square&logo=google-cloud&logoColor=white) ![Pub/Sub](https://img.shields.io/badge/Cloud_Pub%2FSub-4285F4?style=flat-square&logo=google-cloud&logoColor=white) |
| **Infra & DevOps** | ![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/GKE-326CE5?style=flat-square&logo=kubernetes&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white) ![Argo CD](https://img.shields.io/badge/Argo_CD-EF7B4D?style=flat-square&logo=argo&logoColor=white) |
| **Backend & Python** | ![Python](https://img.shields.io/badge/Python_3.12-3776AB?style=flat-square&logo=python&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white) ![Clean Arch](https://img.shields.io/badge/Clean_Architecture-zinc?style=flat-square) ![Ruff](https://img.shields.io/badge/Ruff_&_Mypy-black?style=flat-square) |
| **Data & Storage** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![Cloud SQL](https://img.shields.io/badge/Cloud_SQL-4285F4?style=flat-square&logo=google-cloud&logoColor=white) ![Redis](https://img.shields.io/badge/Redis_Memorystore-DC382D?style=flat-square&logo=redis&logoColor=white) ![Document AI](https://img.shields.io/badge/Document_AI-EA4335?style=flat-square&logo=google-cloud&logoColor=white) |

</div>

<br />

<div align="center">
  <img src="https://skillicons.dev/icons?i=gcp,terraform,docker,kubernetes,githubactions,python,fastapi,postgres,redis,linux&theme=dark" alt="Tech Stack Icons" />
</div>

---

### 🏛️ Arquiteturas & Padrões de Engenharia

<details open>
<summary><b>📐 01. IaC & Governança de Infraestrutura (Terraform & GKE)</b></summary>
<br />

- **Zero Cliques em Console:** Infraestrutura 100% declarativa e versionada.
- **Segurança Zero-Trust:** Eliminação integral de credenciais estáticas (chaves JSON de contas de serviço) substituídas por **Workload Identity Federation** nas esteiras de CI/CD.
- **Topologia de Rede:** Ambientes segmentados por VPCs dedicadas, Private Google Access, Cloud NAT e clusters GKE em modo privado.

```
GitHub Actions ➔ OIDC Workload Identity ➔ Terraform ➔ GCP (VPC / GKE / Cloud SQL / IAM)
```
</details>

<details>
<summary><b>⚡ 02. Ingestão & Pipelines de Dados Analíticos (Serverless & Pub/Sub)</b></summary>
<br />

- **Desacoplamento Assíncrono:** Arquiteturas orientadas a eventos utilizando Cloud Pub/Sub com políticas de retry exponencial e Dead Letter Queues (DLQ) para contenção de falhas.
- **Arquitetura Medallion:** Organização lógica em camadas nativas na nuvem:
  - **Bronze:** Dados brutos em Cloud Storage (GCS) com retenção e versionamento.
  - **Silver:** Ingestão estruturada e deduplicada (Upsert) no BigQuery / PostgreSQL.
  - **Gold:** Modelagem dimensional e views otimizadas para consumo de BI e IA.

```
Fontes de Dados ➔ Cloud Run / Functions ➔ Cloud Pub/Sub (DLQ) ➔ BigQuery Warehouse
```
</details>

<details>
<summary><b>🛡️ 03. Engenharia de Backend & Software Craftsmanship</b></summary>
<br />

- **Clean Architecture & SOLID:** Domínio desacoplado de frameworks e drivers de banco.
- **Tipagem Estrita & Qualidade:** Código Python validado via **Mypy** (modo estrito) e linters de alta performance com **Ruff**.
- **Contêineres Eficientes:** Dockerfiles multi-stage visando imagens mínimas, sem root e imunes a vulnerabilidades comuns de runtime.
</details>

---

### 🚀 Production Cases & Validação Técnica

<div align="center">
  <table>
    <tr>
      <td width="50%">
        <h4 align="center">🌐 Casos Reais em Produção</h4>
        <p align="center">
          Detalhamento técnico de migrações de missão crítica (AWS ➔ GCP), esteiras de IA com Document AI, automações serverless e topologias Zero-Trust com métricas de impacto e topologias de arquitetura.
        </p>
        <p align="center">
          <a href="https://portfolio-eight-pink-54.vercel.app/"><b>Acessar Portfólio ➔</b></a>
        </p>
      </td>
      <td width="50%">
        <h4 align="center">🏆 Certificação Oficial</h4>
        <p align="center">
          <b>Google Cloud Certified</b><br />
          Professional Cloud Architect (PCA)<br />
          Credencial pública e auditável emitida pelo Google.
        </p>
        <p align="center">
          <a href="https://www.credly.com/badges/251634f5-7ee6-4c1a-8322-dfdbfac9b3e4/public_url"><b>Verificar no Credly ↗</b></a>
        </p>
      </td>
    </tr>
  </table>
</div>

---

### 📬 Conexão & Contato

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Jonathan_Brito-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jonathan-loiola-brito/)
[![Portfolio](https://img.shields.io/badge/Web-jbrito.cloud-10b981?style=flat-square&logo=google-chrome&logoColor=white)](https://portfolio-eight-pink-54.vercel.app/)
[![Email](https://img.shields.io/badge/Email-jonathan.brito48@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:jonathan.brito48@gmail.com)

<sub>Baseado em São Paulo, Brasil • Atuação Remota Global • Disponível para desafios de alta escala</sub>

</div>
