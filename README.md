# GitHub-Actions-Project
# CI/CD DevSecOps Pipeline avec GitHub Actions

Ce projet Java Maven est accompagné d'un pipeline CI/CD complet basé sur GitHub Actions.
Lien projet: 
```bash
https://www.youtube.com/watch?v=icZUzgtz_d8
```
## Fonctionnalités

- Compilation avec Maven
- Analyse de vulnérabilités (Trivy)
- Scan de secrets (Gitleaks)
- Tests unitaires
- Analyse SonarQube
- Build et push Docker

## Pipeline GitHub Actions

```yaml
jobs:
  - compile
  - security-check (Trivy + Gitleaks)
  - test (mvn test)
  - build_project_and_sonar_scan
  - buils_docker_image_and_push
