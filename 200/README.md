# 200 - Requirements

Based on "Harbor Installation Prerequisites" at https://goharbor.io/docs/2.5.0/install-config/installation-prereqs/

Harbor is deployed as several Docker containers. You can therefore deploy it on any Linux distribution that supports Docker. The target host requires Docker, and Docker Compose to be installed.

## 100 - Hardware

The following table lists the minimum and recommended hardware configurations for deploying Harbor.

| Resource | Minimum | Recommended |
| --- | --- | --- |
| CPU | 2 CPU | 4 CPU |
| Memory | 4 GB | 8 GB |
| Disk | 40 GB | 160 GB |

## 200 - Software

The following table lists the software versions that must be installed on the target host.

| Software | Version | Description |
| --- | --- | --- |
| Docker Engine | Version 17.06.0-ce+ or higher | For installation instructions, see [Docker Engine documentation](https://docs.docker.com/engine/installation/) |
| Docker Compose | Version 1.18.0 or higher | For installation instructions, see [Docker Compose documentation](https://docs.docker.com/compose/install/) |
| Openssl | Latest is preferred | Used to generate certificate and keys for Harbor |

## 300 - Network Ports

Harbor requires that the following ports be open on the target host.

| Port | Protocol | Description |
| --- | --- | --- |
| 443 | HTTPS | Harbor portal and core API accept HTTPS requests on this port. You can change this port in the configuration file. |
| 4443 | HTTPS | Connections to the Docker Content Trust service for Harbor. Only required if Notary is enabled. You can change this port in the configuration file. |
| 80 | HTTP | Harbor portal and core API accept HTTP requests on this port. You can change this port in the configuration file. |
