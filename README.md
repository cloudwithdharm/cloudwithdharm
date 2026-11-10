<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0B1F3A,50:0078D4,100:5E2CA5&height=260&section=header&text=DHARMENDRA%20PRASAD&fontSize=54&fontColor=ffffff&fontAlignY=40&animation=fadeIn&desc=Senior%20DevSecOps%20Engineer%20%C2%B7%20Azure%20Platform%20%26%20Governance%20%C2%B7%20Terraform%20Landing%20Zones&descAlignY=62&descSize=17" width="100%" alt="Dharmendra Prasad"/>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&pause=1400&color=4DA3FF&center=true&vCenter=true&width=820&height=40&lines=I+design+secure%2C+governed+Azure+platforms+at+enterprise+scale;Everything+as+code.+Security+shifted+left.+Governance+by+default.;9%2B+years+%E2%80%A2+Telecom+%E2%86%92+Cloud+%E2%86%92+DevSecOps+%E2%86%92+Platform+Leadership)](https://github.com/cloudwithdharm)

<br/>

![Experience](https://img.shields.io/badge/EXPERIENCE-9%2B_YEARS-0B1F3A?style=for-the-badge&labelColor=0078D4)
![Cloud](https://img.shields.io/badge/CLOUD_%26_DEVSECOPS-6%2B_YEARS-0B1F3A?style=for-the-badge&labelColor=5E2CA5)
![Provisioning](https://img.shields.io/badge/PROVISIONING_TIME-%E2%88%9280%25-0B1F3A?style=for-the-badge&labelColor=107C10)
![Focus](https://img.shields.io/badge/FOCUS-AZURE_%C2%B7_TERRAFORM_%C2%B7_SECURITY-0B1F3A?style=for-the-badge&labelColor=CA5010)

<a href="https://www.linkedin.com/in/dharmendra-prasad92"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/></a>
<a href="mailto:dharmendraprasad708@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-EA4335?style=flat-square&logo=gmail&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Hyderabad-India-2ea44f?style=flat-square&logo=googlemaps&logoColor=white"/>
<img src="https://komarev.com/ghpvc/?username=cloudwithdharm&label=Views&color=0078D4&style=flat-square"/>

</div>

<br/>

## 🧭 Who I Am

I'm a **Senior DevSecOps Engineer at AmeriCloud** who builds the **foundation other teams build on**: governed Azure tenants, hub-and-spoke networks, Terraform landing zones and secure delivery pipelines.

My career started in **telecom and network engineering** (Ericsson, Nokia), so I think about cloud the way a network engineer does: **connectivity, segmentation, inspection and resilience first**. That is why my platforms are secure and predictable in production.

> **I don't just deploy resources. I design operating models:** how subscriptions are organised, how access is granted, how code reaches production, and how cost, security and recovery are controlled.

<br/>

## ⚡ Impact at a Glance

| 🚀 Delivery | 🔐 Security | 🏛️ Governance | 🤝 Leadership |
|:---:|:---:|:---:|:---:|
| **80% faster** infrastructure provisioning with Terraform | Security scanning built into every pipeline | Management groups, Policy and RBAC by design | Vendor management, KT and team upskilling |
| Consistent **Dev → UAT → Prod** | **RBAC** and least-privilege access | Policy exemptions with justification | SOW, RFP/RFI and deliverable sign-off |

<br/>

## 🛠️ Tech Arsenal

<div align="center">

<a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=azure,terraform,azurepipelines,githubactions,jenkins,kubernetes,docker,helm,prometheus,grafana,linux,ubuntu,bash,powershell,python,git,github,bitbucket,jira&perline=10" alt="skills"/></a>

</div>

<table>
<tr>
<td width="50%" valign="top">

**☁️ Cloud Platform**
`Azure` `Entra ID` `VNet` `Load Balancer` `Application Gateway` `Azure Firewall` `Key Vault` `Storage` `ACR` `AKS`

**🏗️ Infrastructure as Code**
`Terraform` `ARM Templates` `Reusable Modules` `Remote State`

**🔁 CI/CD**
`Azure DevOps` `Azure Pipelines` `GitHub Actions` `Jenkins`

</td>
<td width="50%" valign="top">

**🔐 DevSecOps**
`SonarQube` `Trivy` `TFLint` `OWASP` `RBAC` `Defender` `Azure Policy` `Vulnerability Mgmt`

**📦 Containers**
`Docker` `Kubernetes (AKS)` `Helm`

**📊 Observability**
`Azure Monitor` `Log Analytics` `Prometheus` `Grafana`

**💻 Systems & Scripting**
`Linux` `Windows Server` `Bash` `PowerShell` `Python`

</td>
</tr>
</table>

<br/>

## 🏛️ Enterprise Azure Platform Engineering

*Expand any area to see how I approach it.*

<details open>
<summary><b>🧱 1 · Tenant, Management Groups & Governance</b></summary>
<br/>

A clean hierarchy is the backbone of governance: policy and access flow **down**, and exceptions are explicit.

```mermaid
graph TD
    R["Tenant Root Group<br/>Microsoft Entra ID"] --> P["Platform MG"]
    R --> L["Landing Zones MG"]
    R --> S["Sandbox MG"]
    R --> D["Decommissioned MG"]
    P --> P1["Identity"]
    P --> P2["Connectivity"]
    P --> P3["Management"]
    L --> L1["App Sub · Prod"]
    L --> L2["App Sub · Non-Prod"]
    style R fill:#0B1F3A,color:#fff
    style P fill:#0078D4,color:#fff
    style L fill:#107C10,color:#fff
    style S fill:#CA5010,color:#fff
    style D fill:#605E5C,color:#fff
```

- Subscription boundaries: **platform** vs **application** subscription design
- **Azure Policy & initiatives** assigned at management group scope
- **RBAC group model**: access via groups, never individuals
- **Subscription onboarding / offboarding** runbooks
- **Policy exemptions** with written justification and expiry
- **Defender for Cloud**, user and group lifecycle in Entra ID

</details>

<details>
<summary><b>🌐 2 · Hub-and-Spoke Networking</b></summary>
<br/>

**Centralized inspection · Shared connectivity · Controlled egress**

```mermaid
graph LR
    OP["On-Premises<br/>VPN / ExpressRoute"] --> GW
    subgraph HUB["Hub VNet"]
        GW["VPN / ER Gateway"]
        FW["Azure Firewall"]
        DNS["Private DNS Zones"]
    end
    HUB <-->|Peering| S1["Spoke · Prod"]
    HUB <-->|Peering| S2["Spoke · Non-Prod"]
    HUB <-->|Peering| S3["Spoke · Shared Services"]
    S1 -->|"UDR 0.0.0.0/0"| FW
    S2 -->|"UDR 0.0.0.0/0"| FW
    S3 -->|"UDR 0.0.0.0/0"| FW
    FW --> NET(("Internet<br/>Controlled Egress"))
```

- **IPAM & CIDR planning**, including on-premises CIDR assessment to prevent overlap
- **UDRs**, firewall rule design, **Private Endpoints** and **Private DNS**
- **VPN Gateway & ExpressRoute** for hybrid connectivity

</details>

<details>
<summary><b>🛡️ 3 · Defense in Depth</b></summary>
<br/>

| Layer | What I enforce |
|---|---|
| 🪪 **Identity** | Entra ID, group-based RBAC, least privilege |
| 🌐 **Network** | Hub firewall, NSGs, UDRs, Private Endpoints |
| 📜 **Governance** | Management groups, Azure Policy, initiatives |
| 🖥️ **Compute** | Hardening, Defender, patching, vulnerability management |

</details>

<details>
<summary><b>🏗️ 4 · Terraform Landing Zone Automation</b></summary>
<br/>

- **Remote state** with least-privilege access and **encryption at rest**
- **Versioned, reusable modules**
- Quality gates: **linting · secret scanning · security scanning · testing · cost estimation**
- **Manual approvals** before apply
- **Drift detection** via scheduled pipelines

```hcl
# Pattern: remote state, locked down and encrypted
terraform {
  backend "azurerm" {
    resource_group_name  = "rg-tfstate-platform"
    storage_account_name = "sttfstateplatform"
    container_name       = "tfstate"
    key                  = "landingzone/prod.tfstate"
    use_azuread_auth     = true   # RBAC, not access keys
  }
}
```

</details>

<details>
<summary><b>🔁 5 · Secure Pipelines & Branching Strategy</b></summary>
<br/>

```mermaid
flowchart LR
    A["Short-lived<br/>feature branch"] --> B["Pull Request<br/>(mandatory)"]
    B --> C["Validate & Test<br/>fmt · TFLint · Sonar · Trivy"]
    C --> D["Plan + Cost"]
    D --> E{"Manual<br/>Approval"}
    E -->|Approved| F["Apply / Deploy"]
    E -->|Rejected| A
    F --> G["Monitor +<br/>Drift Detection"]
    F -.->|Failure| H["Rollback"]
```

- **Trunk-based** development, branch policies, **no delete on `main`**, **CODEOWNERS**, minimum reviewers
- Reusable templates: **Validate & Test → Build → Deploy → Apply → Rollback**
- **Parallel jobs** for fast feedback

</details>

<details>
<summary><b>🚚 6 · Cloud Migration</b></summary>
<br/>

**Assess → Discover → Readiness → Pre-checklist → Cutover → Post-checklist → Hypercare**

Clear migration strategy per workload, with checklists *before, during and after* cutover so nothing is left to memory.

</details>

<details>
<summary><b>💰 7 · FinOps & Cost Optimization</b></summary>
<br/>

Idle resources · Unattached disks · Oversized VMs · Unnecessary log ingestion · VM auto-shutdown/start · Reserved capacity · Right-sized backup retention

</details>

<details>
<summary><b>♻️ 8 · Backup, DR & High Availability</b></summary>
<br/>

**LRS / ZRS / GRS** · **VMSS** · Primary and secondary regions · Designs driven by explicit **RTO / RPO** targets

</details>

<details>
<summary><b>📈 9 · Monitoring & Observability</b></summary>
<br/>

**Azure Monitor** · **Log Analytics** · Alerting · **Prometheus & Grafana** for Kubernetes workloads

</details>

<details>
<summary><b>🤝 10 · Technical Leadership & Vendor Management</b></summary>
<br/>

| Area | Scope |
|---|---|
| **Vendor lifecycle** | RFI / RFP, technical evaluation matrix, commercial proposals, SOW |
| **Delivery control** | Deliverables, acceptance criteria, sprints, dependencies, risks, payment milestones |
| **Cadence** | Weekly reviews, retro calls, sign-off, escalation matrix |
| **Transitions** | Knowledge transfer, documentation handover, RACI |
| **People** | Team management, upskilling strategy, senior-level interviews |

</details>

<br/>

## 💼 Career Journey

```mermaid
timeline
    title From Telecom Networks to Cloud Platform Leadership
    2017 : Network Engineer · Teleysia / Nokia
    2018 : Network & IT Support · Ericsson
    2021 : Cloud & Automation Engineer · Ericsson
    2022 : DevOps & Security Engineer · CEMtics
    2024 : Senior DevSecOps Engineer · AmeriCloud
```

| Period | Role | Company |
|---|---|---|
| **May 2024 – Present** | **Senior DevSecOps Engineer** | **AmeriCloud**, Hyderabad |
| Mar 2022 – May 2024 | DevOps & Security Engineer | CEMtics Solution, Gurgaon |
| Apr 2021 – Feb 2022 | Cloud & Automation Engineer | Ericsson Global India |
| 2017 – 2021 | Network & IT Support Engineer | Ericsson · Nokia · Teleysia |

<br/>

## 📌 Featured Work

| Project | Stack | Outcome |
|---|---|---|
| **Azure Infrastructure Automation** | Terraform · Azure · Linux · Git | Modular IaC for VNets, NSGs, storage and VMs with remote state and CI/CD |
| **Secure CI/CD Pipeline** | Azure DevOps · GitHub · Terraform · SonarQube | Automated delivery with quality and security gates |
| **Kubernetes Deployment on AKS** | Docker · AKS · ACR | Scalable, monitored containerized applications |

<br/>

## 📊 GitHub Analytics

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=cloudwithdharm&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true" />
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=cloudwithdharm&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" />

<img src="https://streak-stats.demolab.com?user=cloudwithdharm&theme=tokyonight&hide_border=true" />

</div>

<br/>

## 🎓 Education & Certification

- 🎓 **B.Tech** · Electronics & Communication Engineering
- ☁️ **AWS Cloud** · Ethans Tech (ISO Certified) · Jan 2021

<br/>

## 🌱 Currently

- 🔨 Building reusable Terraform modules and Azure landing zone patterns
- 📚 Deepening DevSecOps automation and platform governance
- 💬 Open to conversations on Azure architecture, Terraform and DevSecOps

<br/>

<div align="center">

### 📫 Let's Build Something Reliable

[![LinkedIn](https://img.shields.io/badge/LinkedIn-dharmendra--prasad92-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/dharmendra-prasad92)
[![Email](https://img.shields.io/badge/Email-dharmendraprasad708%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:dharmendraprasad708@gmail.com)

*"Automate everything. Secure by default. Govern at scale."*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:5E2CA5,50:0078D4,100:0B1F3A&height=130&section=footer" width="100%" alt="footer"/>

</div>
