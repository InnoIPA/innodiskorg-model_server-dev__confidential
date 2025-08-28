# AccelBrain Model Server Docker (Based on Ollama)

This project is forked from [ollama/ollama](https://github.com/ollama/ollama),  
and is customized to build a Dockerized model server for use in the AccelBrain system.

---

## 🛠️ Build Workflow

1. **Prepare two self-hosted GitHub runners**:
   - One with **x86_64 (amd64)** architecture and GPU support
   - One with **ARM64 (arm)** architecture and GPU support

2. **Update versioning information**:
   - Edit `CHANGELOG.md`
   - Modify `version/version.json` with the new version info

3. **Trigger the GitHub Actions `build-release` workflow**:
   - Push a tag (e.g., `v1.2.3`) to start the workflow
   - Multi-architecture Docker images will be built and published automatically

---

## 📦 Docker Images

- Once built, images will be published to [Docker Hub](https://hub.docker.com/r/innodiskorg/ollama):
  ```bash
  docker pull innodiskorg/ollama:<version>
