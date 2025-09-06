# SWA Lab 10 – Spring Cloud Config Repository
This repository contains YAML configuration files for use with a Spring Cloud Config Server.
### Overview
- Config files are structured for ServiceA and ServiceB.
- The Config Server fetches these files from this GitHub repository, enabling centralized configuration management.
- Supports dynamic property updates for services without redeployment.

### Usage
1. Clone or fork this repository.
2. Configure your Spring Cloud Config Server to point to this repository:
```yaml
spring:
  cloud:
    config:
      server:
        git:
          uri: https://github.com/<your-username>/swalab10.git
          default-label: main
```
3. Start the Config Server; services will fetch configuration automatically.

### Notes
Ensure that application.yml files for each service exist in the repository root or in service-specific subfolders.
