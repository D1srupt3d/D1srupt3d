<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/banner-dark.svg">
  <img alt="D1srupt3d: Infrastructure, written like software." src="assets/banner-light.svg" width="100%">
</picture>

Hey, I'm D1srupt3d 👋

I build infrastructure the way good software is built: versioned, tested, and shipped through a pipeline that refuses anything unsigned. Mostly Go and Python, on Kubernetes, with OpenTofu and Ansible underneath.

Off the clock I'm usually still at it, just at home: logging every plane my antenna can hear, keeping a Minecraft server or two alive, and watching a rack of blinking lights the way other people watch a fireplace.

<sub><i>The Great Disk Druid, Server Sentinel, Professional Light Blinker Observer.</i></sub>

[d1srupt3d.dev](https://d1srupt3d.dev) &nbsp;·&nbsp; [LinkedIn](https://linkedin.com/in/liamgamache)

### Selected work

<table>
<tr>
<td width="50%" valign="top">

#### [strata](https://github.com/D1srupt3d/strata)

Layered dotfiles manager for macOS, Linux and Windows.

I wanted my dotfiles repo to look like my home directory, not a template language. So strata stacks plain folders (`work/` on top of `base/`), remembers what it last wrote so it never overwrites your local edits, and is tested on all three operating systems with the race detector and govulncheck. Releases are SSH-signed, and the installer checks before anything lands.

<sub>Go · GoReleaser · Homebrew tap</sub>

</td>
<td width="50%" valign="top">

#### [skyledger](https://github.com/D1srupt3d/skyledger)

Long-term memory for an ADS-B aircraft receiver.

My receiver hears every plane in range, then forgets most of it. skyledger decodes its binary history and live feed into TimescaleDB with exactly-once imports, and turns it into flights, range and signal health. CI runs integration tests against a real database with an 80% coverage gate and installs the Helm chart into a throwaway kind cluster.

<sub>Go · TimescaleDB · Grafana · Helm · amd64 + arm64</sub>

</td>
</tr>
</table>

### Homelab

A private, production-style platform: Proxmox and OPNsense underneath, three Kubernetes clusters on top, all of it in one repository. Is it overkill for my photos and a Minecraft server? Absolutely. It's also where I learn things properly, by running them for real.

| Practice | How it works |
|---|---|
| **Change control** | Merging deploys nothing. Argo CD and Semaphore act only on a GPG-signed approval commit, and fail closed otherwise. |
| **Secrets** | 1Password is the only source. External Secrets delivers them at runtime; gitleaks guards every commit. |
| **Network** | Default deny. Every app gets an explicit Cilium policy. |
| **Recovery** | Each guest's backup tier is a tag in OpenTofu. Restore drills for etcd and the management cluster are in progress. |
| **Clusters** | `cygnus` K3s for apps · `lyra` five self-healing Talos nodes built by Omni · `vega` management, running Omni and Argo CD |

<sub>Proxmox · OPNsense · TrueNAS · OpenTofu · Ansible · Packer · K3s · Talos · Omni · Argo CD · Cilium · External Secrets · CloudNativePG · Prometheus · Grafana · Loki</sub>

**Now:** moving workloads onto `lyra`, breaking things on purpose in restore drills before they break on their own, and learning Rust, slowly.

---

If you made it this far, say hi. I'm always up for talking homelabs, Go, or why that one LED just turned amber.
