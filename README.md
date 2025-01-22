# Jenkins Setup Guide

## Steps to Set Up Jenkins on an Instance

### 1. SSH to the Instance
```bash
ssh ubuntu@54.210.84.67
```

### 2. Install JDK
```bash
sudo apt update
sudo apt install openjdk-17-jre
```

### 3. Validate the Installation
```bash
java -version
```

### 4. Import the Jenkins Key
```bash
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
```

### 5. Add the Jenkins Repository to the Sources List
```bash
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian binary/" | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
```

### 6. Update the Package List
```bash
sudo apt-get update
```

### 7. Install Jenkins
```bash
sudo apt-get install jenkins
```

### 8. Check if Jenkins is Running
```bash
ps -ef | grep jenkins
```

### 9. Access Jenkins
- Open your browser and navigate to:  
  [http://54.210.84.67:8080/](http://54.210.84.67:8080/)

### 10. Get the Jenkins Unlock Password
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

### 11. Create a Pipeline
- Log in to Jenkins using the password from Step 10.
- Click **New Item** and select **Pipeline**.
- Configure your pipeline as needed.
