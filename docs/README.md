# Kukuk DevOps Abschlussprojekt

# CI/CD Abschlussprojekt mit Jenkins & Kubernetes

## Komponenten
- Spring Boot Backend
- Statisches Frontend via BusyBox
- Dockerisierung mit minimalen Images
- Jenkins CI/CD-Pipeline mit Umgebungswahl
- Kubernetes-Deployment (dev & prod getrennt)

## Pipeline-Ablauf
1. Git Checkout
2. Maven Build Backend
3. Docker Build & Push (Backend + Frontend)
4. Dev-Deployment via kubectl
5. Prod-Freigabe manuell
6. Prod-Deployment via kubectl

## Besonderheiten
- Ressourcenoptimiert (Images & Deployments)
- Maven-Profilsteuerung ohne Codeänderung
- Environment via ConfigMap (dev/prod)
- Klar getrennte YAML-Struktur
