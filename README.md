# JPetStore CI/CD Pipeline

## Project Description

This project implements a **CI/CD pipeline** for the **JPetStore Java Web Application** using DevOps tools. The application is deployed as a **Docker container** and runs on port **8081**.

## Tools Used

- **Git/GitHub** → Clone the source code.
- **Maven** → Build and test the application.
- **Docker** → Containerize the application.
- **Jenkins** → Automate the CI/CD pipeline.
- **Ansible** → Deploy the application.

## CI/CD Pipeline Flow

### **Continuous Integration (CI)**

1. Clone the repository.
2. Build the code using Maven.
3. Run unit tests.
4. Build a Docker image.
5. Push the image to **Docker Hub**.

### **Continuous Deployment (CD)**

1. Use **Ansible** to pull the Docker image from Docker Hub.
2. Deploy and run the application as a **Docker container**.
3. Expose the application on **port 8081**.

## Project Structure

```
├── src/                 # Source code of the application
├── .mvn/                # Maven wrapper files
├── Dockerfile           # Instructions to build Docker image
├── Jenkinsfile          # CI/CD pipeline script for Jenkins
├── ansible/             # Ansible playbook for deployment
│   ├── inventory        # Server inventory file
│   ├── playbook.yml     # Deployment playbook
├── README.md            # Project documentation
```

## How to Run the Application

### **Clone the Repository**

```sh
git clone https://github.com/muhamedusama92/JpetstoreApp.git
cd JpetstoreApp
```

### **Build and Test the Application**

```sh
mvn clean package
```

### **Build and Run the Docker Container**

```sh
docker build -t my-jpetstore-app .
docker run -d -p 8081:8080 my-jpetstore-app
```

### **Deploy Using Ansible**

```sh
ansible-playbook -i ansible/inventory ansible/playbook.yml
```

## Access the Application

After deployment, visit:\
[**http://localhost:8081/jpetstore**](http://localhost:8081/jpetstore)

## Future Enhancements

- Add **automated tests** with Selenium.
- Implement **Kubernetes** for scalable deployment.
- Set up **GitHub Actions** for an alternative CI/CD approach.

---

**Author**: Muhamed Usama\
**Last Updated**: February 2025\


