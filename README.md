# CleanStart Container for Glibc

The GNU C Library (glibc) container provides essential standard C libraries and utilities required for Linux applications. This container includes the complete GNU C Library implementation, featuring POSIX threading support, locale data, and core system libraries. It serves as a fundamental runtime dependency for applications requiring glibc compatibility, offering standardized C library functions, system calls, and internationalization support. The container is security-hardened and optimized for enterprise deployments, featuring minimal attack surface and FIPS-compliant cryptographic functions.

**📌 CleanStart Foundation:** Security-hardened, minimal base OS designed for enterprise containerized environments.

---

## Key Features

Complete GNU C Library implementation with POSIX support:

- Complete GNU C Library implementation with POSIX support
- Internationalization and locale data included
- Thread-safe library functions and utilities
- FIPS 140-2 compliant cryptographic functions
- Security-hardened for enterprise deployments
- Minimal attack surface design

---

## Common Use Cases

Typical scenarios where this container excels:

- Base container for C/C++ applications requiring glibc
- Runtime environment for compiled applications
- Multi-language application support requiring standard C libraries
- Enterprise applications requiring POSIX compliance
- Foundation for containerized Linux applications

---

## Quick Start

### Pull Latest Image

Download the container image from the registry:
```bash
docker pull ghcr.io/cleanstart-containers/glibc:latest
```
```bash
docker pull ghcr.io/cleanstart-containers/glibc:latest-dev
```

### Basic Run

Run the container with basic configuration:
```bash
docker run -it --name glibc-test ghcr.io/cleanstart-containers/glibc:latest-dev /bin/bash
```

### Production Deployment

Deploy with production security settings:
```bash
docker run -d --name glibc-prod \
  --read-only \
  --security-opt=no-new-privileges \
  --user 1000:1000 \
  ghcr.io/cleanstart-containers/glibc:latest \
  tail -f /dev/null
```

---

## Architecture Support

### Multi-Platform Images
```bash
docker pull --platform linux/amd64 ghcr.io/cleanstart-containers/glibc:latest
```
```bash
docker pull --platform linux/arm64 ghcr.io/cleanstart-containers/glibc:latest
```

---

## Resources

- **Official Documentation:** https://www.gnu.org/software/libc/manual/
- **Provenance / SBOM / Signature:** https://images.cleanstart.com/images/glibc
- **Docker Hub:** https://hub.docker.com/r/cleanstart/glibc
- **CleanStart All Images:** https://images.cleanstart.com
- **CleanStart Community Images:** https://hub.docker.com/u/cleanstart

---

## Vulnerability Disclaimer

CleanStart offers Docker images that include third-party open-source libraries and packages maintained by independent contributors. While CleanStart maintains these images and applies industry-standard security practices, it cannot guarantee the security or integrity of upstream components beyond its control.

Users acknowledge and agree that open-source software may contain undiscovered vulnerabilities or introduce new risks through updates. CleanStart shall not be liable for security issues originating from third-party libraries, including but not limited to zero-day exploits, supply chain attacks, or contributor-introduced risks.

**Security remains a shared responsibility:** CleanStart provides updated images and guidance where possible, while users are responsible for evaluating deployments and implementing appropriate controls.
