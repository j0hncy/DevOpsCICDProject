# DevOpsCICDProject

A comprehensive CI/CD pipeline implementation using Jenkins, Maven, SonarQube, and ArgoCD for automated build, test, analysis, and deployment workflows.

## Overview

This project demonstrates a complete DevOps CI/CD workflow that automates the build, test, code analysis, and deployment processes. It integrates industry-standard tools to ensure code quality, security, and reliable deployments.

## Architecture & Tools

### Core Technologies

- **Jenkins**: Orchestration and automation of the CI/CD pipeline
- **Maven**: Build automation and dependency management
- **SonarQube**: Code quality analysis and static code analysis
- **ArgoCD**: GitOps-based continuous delivery and deployment
- **Docker**: Containerization of applications (Dockerfile included)

## Project Structure

- **Python** (67.1%): Main application logic and scripts
- **HTML** (23.3%): Web interface components
- **Java** (4.6%): Backend services and utilities
- **Dockerfile** (2.8%): Container configuration
- **CSS** (1.9%): Styling for web components
- **Groovy** (0.3%): Jenkins pipeline scripts

## Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- Java JDK 8 or higher
- Maven 3.6+
- Docker and Docker Compose
- Git
- Jenkins (for CI/CD orchestration)
- SonarQube (for code analysis)
- ArgoCD (for GitOps deployments)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/j0hncy/DevOpsCICDProject.git
   cd DevOpsCICDProject
   ```

2. **Build the project with Maven**
   ```bash
   mvn clean install
   ```

3. **Run tests**
   ```bash
   mvn test
   ```

4. **Build Docker image**
   ```bash
   docker build -t devopscicdproject:latest .
   ```

## CI/CD Pipeline

The pipeline includes the following stages:

1. **Source Control**: Code pushed to Git repository
2. **Build**: Maven compiles and packages the application
3. **Test**: Automated unit and integration tests
4. **Code Analysis**: SonarQube performs static code analysis
5. **Quality Gate**: Ensures code meets quality standards
6. **Docker Build & Push**: Containerizes and pushes to registry
7. **Deploy**: ArgoCD manages GitOps-based deployments

### Jenkins Configuration

- **Pipeline Type**: Declarative/Scripted Pipeline
- **Triggers**: Webhook on push, scheduled builds
- **Notifications**: Build status notifications

### SonarQube Integration

SonarQube analyzes code for:
- Code smells
- Bugs and vulnerabilities
- Test coverage
- Code duplications

Configure SonarQube properties in `sonar-project.properties` (if applicable).

### ArgoCD Deployment

ArgoCD automatically syncs deployed applications with the Git repository, ensuring:
- GitOps-based infrastructure
- Declarative configuration management
- Automated rollback capabilities

## Configuration

### Maven Configuration

Update `pom.xml` with your project-specific dependencies and build configurations.

### Jenkins Configuration

Configure the following in Jenkins:

1. Git repository URL
2. SonarQube server connection
3. Docker registry credentials
4. ArgoCD webhook URL

### SonarQube Configuration

1. Set up SonarQube project token
2. Configure quality gates
3. Add to build pipeline

## Usage

### Running Locally

```bash
# Build the project
mvn clean package

# Run the application
java -jar target/app.jar

# Or use Docker
docker run -d -p 8080:8080 devopscicdproject:latest
```

### Triggering the Pipeline

Push changes to trigger the Jenkins pipeline automatically, or manually trigger via Jenkins console.

## Project Workflow

```
Git Push → Jenkins Trigger → Build → Test → Code Analysis → 
Quality Gate Check → Docker Build → Push to Registry → 
ArgoCD Sync → Deployment
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Quality Standards

This project maintains high-quality standards enforced through:

- SonarQube code analysis
- Automated unit tests
- Code coverage requirements
- Quality gates before deployment

## Troubleshooting

### Common Issues

**Build Failures**: Check Maven dependencies and Java version compatibility

**SonarQube Connection**: Verify server URL and authentication tokens

**Docker Build Issues**: Ensure Docker daemon is running and sufficient disk space

**ArgoCD Sync Problems**: Verify Git repository credentials and ArgoCD configuration

## Documentation

For detailed documentation on each tool:

- [Jenkins Documentation](https://www.jenkins.io/doc/)
- [Maven Documentation](https://maven.apache.org/guides/)
- [SonarQube Documentation](https://docs.sonarqube.org/)
- [ArgoCD Documentation](https://argo-cd.readthedocs.io/)

## Additional Resources

This repository contains several example implementations:

- **java-maven-sonar-argocd-helm-k8s/**: Jenkins pipeline for Java applications with Maven, SonarQube, ArgoCD, Helm, and Kubernetes
- **multi-stage-multi-agent/**: Multi-stage pipeline with multiple agents for diverse application architectures

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact & Support

For questions or issues, please open a GitHub issue in this repository.

---

**Last Updated**: May 27, 2026
