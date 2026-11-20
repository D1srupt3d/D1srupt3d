```text
██████╗  ██╗███████╗██████╗ ██╗   ██╗██████╗ ████████╗██████╗ ██████╗ 
██╔══██╗███║██╔════╝██╔══██╗██║   ██║██╔══██╗╚══██╔══╝╚════██╗██╔══██╗
██║  ██║╚██║███████╗██████╔╝██║   ██║██████╔╝   ██║    █████╔╝██║  ██║
██║  ██║ ██║╚════██║██╔══██╗██║   ██║██╔═══╝    ██║    ╚═══██╗██║  ██║
██████╔╝ ██║███████║██║  ██║╚██████╔╝██║        ██║   ██████╔╝██████╔╝
╚═════╝  ╚═╝╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚═╝        ╚═╝   ╚═════╝ ╚═════╝ 
```
  
  *The Great Disk Druid, Server Sentinel, Professional Light Blinker Observer*

Infrastructure engineer building Go and Python tooling, with everything I run defined in code.

![Profile Views](https://komarev.com/ghpvc/?username=D1srupt3d&color=blue&style=for-the-badge)

## Skills & Technologies

### Programming Languages

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Shell Script](https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white)

### Infrastructure & DevOps

![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=for-the-badge&logo=ansible&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)

### Tools & Platforms

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![VSCode](https://img.shields.io/badge/VSCode-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)

## Currently Working On

- Moving new homelab apps onto `lyra`, a five-node Talos cluster that Omni builds and repairs on its own
- Restore drills: K3s etcd snapshots, and wiping and restoring the management cluster while workloads keep running
- TypeScript for my personal site ([d1srupt3d.dev](https://d1srupt3d.dev))
- Learning Rust

## Featured Projects

| Project | Description | Stack |
|---------|-------------|-------|
| [strata](https://github.com/D1srupt3d/strata) | Layered dotfiles manager for macOS, Linux and Windows that never overwrites your local edits. CI, tagged releases and a Homebrew tap. | Go |
| [skyledger](https://github.com/D1srupt3d/skyledger) | A ledger of everything your ADS-B receiver has heard: live ingest plus history backfill into TimescaleDB, with Grafana dashboards. Runs on Docker Compose or a Helm chart. | Go, TimescaleDB, Grafana, Docker, Helm |
| [dotfiles-arch](https://github.com/D1srupt3d/dotfiles-arch) | My Arch Linux desktop and shell configs | Shell |

## Homelab 🔒

Self-hosted infrastructure on Proxmox and OPNsense, with three Kubernetes clusters (K3s, plus Talos managed by Omni) deployed by Argo CD. Private repo, so here's how it works and what it runs.

- **Nothing changes unless I signed it.** Merging deploys nothing. Argo CD and Semaphore only act on a `deploy` branch whose tip is a GPG-signed approval commit, and refuse anything else.
- **Secrets live only in 1Password.** External Secrets Operator delivers them at runtime, and gitleaks scans every commit and CI run.
- **Default-deny networking.** App namespaces block all traffic unless a per-app Cilium policy allows it.
- **Backups as code.** OpenTofu sets each guest's tier tag, and the tag decides its backup schedule and retention.
- **Checked before it lands.** CI runs tflint, Checkov, ansible-lint and the tests for the Python tooling; Renovate keeps dependencies current.

**Infra & IaC**

![Proxmox](https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white)
![OPNsense](https://img.shields.io/badge/OPNsense-D94F00?style=for-the-badge&logo=opnsense&logoColor=white)
![TrueNAS](https://img.shields.io/badge/TrueNAS-0095D5?style=for-the-badge&logo=truenas&logoColor=white)
![Packer](https://img.shields.io/badge/Packer-02A8EF?style=for-the-badge&logo=packer&logoColor=white)
![OpenTofu](https://img.shields.io/badge/OpenTofu-FFDA18?style=for-the-badge&logo=opentofu&logoColor=black)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=for-the-badge&logo=ansible&logoColor=white)
![Semaphore](https://img.shields.io/badge/Semaphore-2E7D32?style=for-the-badge)

**Kubernetes & GitOps**

![K3s](https://img.shields.io/badge/K3s-FFC61C?style=for-the-badge&logo=k3s&logoColor=black)
![Talos](https://img.shields.io/badge/Talos-FF7300?style=for-the-badge)
![Omni](https://img.shields.io/badge/Omni-1E1E1E?style=for-the-badge)
![Argo CD](https://img.shields.io/badge/Argo_CD-EF7B4D?style=for-the-badge&logo=argo&logoColor=white)
![Cilium](https://img.shields.io/badge/Cilium-F8C517?style=for-the-badge&logo=cilium&logoColor=black)
![Traefik](https://img.shields.io/badge/Traefik-24A1C1?style=for-the-badge&logo=traefikproxy&logoColor=white)
![cert-manager](https://img.shields.io/badge/cert--manager-326CE5?style=for-the-badge)
![External Secrets](https://img.shields.io/badge/External_Secrets-4B32C3?style=for-the-badge)
![1Password](https://img.shields.io/badge/1Password-3B66BC?style=for-the-badge&logo=1password&logoColor=white)
![CloudNativePG](https://img.shields.io/badge/CloudNativePG-336791?style=for-the-badge&logo=postgresql&logoColor=white)

**Observability**

![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Loki](https://img.shields.io/badge/Loki-F9A825?style=for-the-badge&logo=grafana&logoColor=white)
![Alloy](https://img.shields.io/badge/Alloy-F46800?style=for-the-badge&logo=grafana&logoColor=white)

**Running on top**

- Pocket ID (passkey SSO) · Immich · Paperless-ngx · Dawarich · Home Assistant · Scrypted · Garage (S3) · Step-CA · Proxmox Backup Server · Gatus · Homepage · it-tools · Malcolm · and a Minecraft server or two.

## Activity

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/D1srupt3d/D1srupt3d/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/D1srupt3d/D1srupt3d/output/github-contribution-grid-snake.svg">
  <img alt="Snake eating my contribution graph" src="https://raw.githubusercontent.com/D1srupt3d/D1srupt3d/output/github-contribution-grid-snake.svg">
</picture>

## Contact

Reach me through my site or LinkedIn.

[![Website](https://img.shields.io/badge/d1srupt3d.dev-000000?style=for-the-badge&logo=About.me&logoColor=white)](https://d1srupt3d.dev)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/liamgamache)
