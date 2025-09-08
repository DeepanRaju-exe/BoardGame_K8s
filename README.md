## Features

- Full-Stack Application
- UI components created with Thymeleaf and styled with Twitter Bootstrap
- Authentication and authorization using Spring Security
  - Authentication by allowing the users to authenticate with a username and password
  - Authorization by granting different permissions based on the roles (non-members, users, and managers)
- Different roles (non-members, users, and managers) with varying levels of permissions
  - Non-members only can see the boardgame lists and reviews
  - Users can add board games and write reviews
  - Managers can edit and delete the reviews
- Deployed the application on AWS EC2
- JUnit test framework for unit testing
- Spring MVC best practices to segregate views, controllers, and database packages
- JDBC for database connectivity and interaction
- CRUD (Create, Read, Update, Delete) operations for managing data in the database
- Schema.sql file to customize the schema and input initial data
- Thymeleaf Fragments to reduce redundancy of repeating HTML elements (head, footer, navigation)
# DevOps Ultimate Kubernetes Pipeline

**One-liner summary:**  
A Kubernetes cluster deployed on three VMs (1 master, 2 workers), featuring Jenkins, SonarQube, and Nexus integrated for  CI/CD pipeline.


##  Architecture

The project architecture includes:

- **Three Virtual Machines (VMs)**:
  - **Master Node**: Controls the Kubernetes cluster
  - **Worker Node 1 & 2**: Runs workloads and Services

- **Key Services deployed**:
  - **Jenkins**: For automated pipelines and builds
  - **SonarQube**: For code quality checks and static analysis
  - **Nexus**: Artifact repository for versioned binaries and Docker images

---

##  Infrastructure Setup

1. Provision three Virtual Machines (using AWS EC2):
   - VM-1: Kubernetes Master
   - VM-2 / VM-3: Kubernetes Worker Nodes

2. Install and configure **Kubernetes** on all:
   - Initialize the cluster on master
   - Join workers to the cluster

3. Verify cluster health:
   ```bash
   kubectl get nodes
   kubectl get pods --all-namespaces

