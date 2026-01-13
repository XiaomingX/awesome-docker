# Awesome Docker (更新版)

🐳 精心整理的 Docker 资源、项目与工具列表。

# 什么是 Docker

> Docker 是一个供开发人员和系统管理员构建、发布和运行分布式应用程序的开放平台。它包含 Docker Engine（轻量级运行时和打包工具）和 Docker Hub（用于分享应用和自动化工作流的云服务）。Docker 使应用能够通过组件快速组装，消除了开发、QA 和生产环境之间的摩擦。因此，IT 部门可以更快地发布应用，并在笔记本电脑、数据中心虚拟机或任何云端运行完全相同的应用。

# 入门指南 (Where to start)

* [Docker 官方文档](https://docs.docker.com/): **永远是起点的最佳选择**。
* [Docker 课程 (Docker Curriculum)](https://github.com/prakhar1989/docker-curriculum): 一份非常全面的 Docker 入门教程。
* [Play With Docker](https://training.play-with-docker.com/): 一个基于浏览器的 Docker 游乐场，无需安装即可从入门学到精通。
* [从程序员到 Docker 专家](https://github.com/jesseduffield/lazydocker) (虽是工具介绍，但很多概念值得学习): 推荐配合实战使用。
* [Docker 动手实验 (LabEx)](https://labex.io/skilltrees/docker): 包含 100 多个初学者友好的动手实验，结构化的技能树。

**速查表 (Cheatsheets)**

* [Docker 官方速查表](https://docs.docker.com/get-started/docker_cheatsheet.pdf) (PDF): 官方出品，命令权威。
* [@wsargent 的 Docker 速查表](https://github.com/wsargent/docker-cheat-sheet): 社区最流行、最全的速查表之一。

# 桌面端与安装 (Desktop)

*注：现在的 Docker Desktop 在 Windows 上使用 WSL 2，在 Mac 上使用虚拟化框架，性能已大幅提升。*

* [Docker Desktop](https://www.docker.com/products/docker-desktop/): Windows 和 Mac 上运行 Docker 的标准方式（部分企业使用需付费）。
* [OrbStack](https://orbstack.dev/): **(强烈推荐 - macOS)** 快速、轻量且简单的 Docker Desktop 替代品，资源占用极低。
* [Rancher Desktop](https://rancherdesktop.io/): 开源的桌面容器管理工具，支持 Docker (Moby) 和 Kubernetes，完全免费。
* [Podman Desktop](https://podman-desktop.io/): 一个开源的图形化容器管理工具，同时支持 Docker 和 Podman 引擎。

---

# 核心项目 (Projects)

* [Moby](https://github.com/moby/moby): Docker 构建的基础开源项目。
* [Docker Compose](https://github.com/docker/compose/): 定义和运行多容器 Docker 应用程序的工具（现已用 Go 重写为 V2 版本）。
* [Docker Hub](https://hub.docker.com): 全球最大的容器镜像库和社区。

## 容器管理与运维 (Container Operations)

### 可视化管理界面 (UI / Management)

* [Portainer](https://github.com/portainer/portainer): **(必备)** 一个轻量级的管理 UI，可轻松管理 Docker 主机或 Swarm 集群。
* [Dockge](https://github.com/louislam/dockge): 一个界面现代、反应灵敏的 Docker Compose 堆栈管理器（由 Uptime Kuma 作者开发）。
* [Yacht](https://www.google.com/search?q=https://github.com/SelfhostedPro/Yacht): 一个专注于模板和易用性的 Docker Web 管理界面。
* [LazyDocker](https://github.com/jesseduffield/lazydocker): **(终端神器)** 一个基于终端的 UI (TUI)，让你在命令行里也能像用图形界面一样管理 Docker，支持鼠标操作。

### 监控与日志 (Monitoring & Logging)

* [cAdvisor](https://github.com/google/cadvisor): Google 出品，用于分析运行中容器的资源使用和性能特征。
* [Dozzle](https://github.com/amir20/dozzle): 实时查看 Docker 容器日志的轻量级 Web 界面，无需配置，开箱即用。
* [Glances](https://github.com/nicolargo/glances): 跨平台的系统监控工具，支持 Docker 监控。
* [Prometheus](https://prometheus.io/): 云原生应用监控的事实标准。
* [Grafana](https://grafana.com/): 开源的可观察性平台，通常与 Prometheus 配合，用于展示精美的仪表盘。
* [Loki](https://grafana.com/oss/loki/): 受到 Prometheus 启发的水平可扩展、高可用、多租户日志聚合系统。

### 网络与反向代理 (Networking / Reverse Proxy)

* [Traefik](https://github.com/traefik/traefik): 云原生应用代理。能自动发现 Docker 容器并自动配置路由和 SSL，非常适合微服务。
* [Nginx Proxy Manager](https://github.com/jc21/nginx-proxy-manager): 基于 Docker 的 Nginx 反向代理管理工具，拥有漂亮易用的 Web 界面，自动申请 SSL 证书。
* [Caddy](https://caddyserver.com/): 强大的企业级开源 Web 服务器，默认自动启用 HTTPS（常作为反向代理使用）。
* [Socket Proxy](https://github.com/Tecnativa/docker-socket-proxy): 一个安全性增强的 Docker Socket 代理，用于防止容器获取过高的 Docker 守护进程权限。

### 部署与自动化 (Deployment & Automation)

* [Watchtower](https://github.com/containrrr/watchtower): 自动检测并更新正在运行的 Docker 容器的基础镜像。
* [Diun](https://github.com/crazy-max/diun): 当 Docker 注册表上的镜像更新时，接收通知（支持 Telegram, Slack, Discord 等）。
* [CapRover](https://caprover.com/): 极其简单的应用/数据库部署平台，相当于你自己的私有 Heroku。
* [Coolify](https://coolify.io/): 一个开源且可自托管的 Heroku / Netlify / Vercel 替代方案。

### 安全 (Security)

* [Trivy](https://github.com/aquasecurity/trivy): **(强烈推荐)** 简单而全面的容器及文件系统漏洞扫描工具，CI/CD 必备。
* [Grype](https://github.com/anchore/grype): 针对容器镜像和文件系统的漏洞扫描器。
* [Syft](https://github.com/anchore/syft): 用于从容器镜像生成软件物料清单 (SBOM) 的 CLI 工具。
* [Hadolint](https://github.com/hadolint/hadolint): Dockerfile 语法检查器，帮助你编写符合最佳实践的 Dockerfile。
* [Dockle](https://github.com/goodwithtech/dockle): 容器镜像安全合规性检查工具，专注于构建“最佳实践”镜像。

### 终端工具 (Terminal / CLI Tools)

* [Dive](https://github.com/wagoodman/dive): 一个用于探索 Docker 镜像层内容、分析每一层大小并发现缩减镜像体积方法的工具。
* [ctop](https://github.com/bcicen/ctop): 类似于 Linux `top` 命令的界面，但用于显示容器的实时指标。
* [Dry](https://github.com/moncho/dry): 一个交互式的 Docker 容器管理器终端应用。

## 镜像与构建 (Images & Building)

### 基础镜像 (Base Images)

* [Alpine Linux](https://hub.docker.com/_/alpine): 面向安全的轻量级 Linux 发行版，镜像体积极小（约 5MB）。
* [Distroless](https://github.com/GoogleContainerTools/distroless): Google 推出的"无发行版"镜像，仅包含应用及其运行时依赖，不包含 Shell 或包管理器，安全性更高。
* [Wolfi](https://github.com/wolfi-dev): 专为容器时代设计的 Linux 操作系统（由 Chainguard 维护），专注于供应链安全。

### 构建工具 (Builders)

* [BuildKit](https://github.com/moby/buildkit): 支持并发、缓存高效且与 Dockerfile 无关的构建工具包（现已成为 Docker 默认构建后端）。
* [Kaniko](https://github.com/GoogleContainerTools/kaniko): 在 Kubernetes 中构建容器镜像的工具，无需特权模式。
* [Buildah](https://github.com/containers/buildah): 专注于构建 OCI 镜像的工具，不需要运行守护进程。
* [Slim (原 DockerSlim)](https://github.com/slimtoolkit/slim): 自动分析并压缩 Docker 镜像，最高可将体积减少 30 倍。

### 镜像仓库 (Registries)

* [Harbor](https://goharbor.io/): 一个开源的可信云原生镜像仓库，支持存储、签名和扫描内容。
* [Gitea / Forgejo](https://about.gitea.com/): 轻量级自托管 Git 服务，内置了容器镜像仓库功能。
* [Zot](https://zotregistry.io/): 一个 OCI 原生的容器镜像仓库，适合分发容器镜像和制品。

## 开发环境 (Development Environment)

* [Dev Containers (VS Code)](https://code.visualstudio.com/docs/devcontainers/containers): 直接在 VS Code 中使用容器作为全功能的开发环境。
* [DevPod](https://devpod.sh/): 类似 GitHub Codespaces 但开源、仅客户端且无特定厂商绑定的工具。
* [Gitpod](https://www.gitpod.io/): 云端开发环境平台。

# 其他资源

## 最佳实践与列表

* [Dockerfile 最佳实践](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/): 官方指南，必读。
* [Awesome Kubernetes](https://github.com/ramitsurana/awesome-kubernetes): 既然用了 Docker，迟早会用到 Kubernetes。
* [Awesome Compose](https://github.com/docker/awesome-compose): Docker 官方提供的 Docker Compose 示例集合，包含各种常见技术栈（如 Nginx+Flask, React+Java 等）。
* [Awesome Selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted): **(强烈推荐)** 适合寻找可以在 Docker 中运行的自托管应用。
