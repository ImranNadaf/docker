# Docker - Day 1

## 📘 EOD Updates

### What I Learnt (Theory)
- What is Docker and why we use it  
- Difference between **Containers vs VMs**  
- Docker architecture  
- Docker images  
- Dockerfiles and best practices  

### Practical Tasks Performed
1. **Verified Docker Installation**
   ```bash
   docker --version
   docker run hello-world
   ```
   ✅ Docker installed and working successfully  

   ![Docker Install](screenshots/screenshot_1.png)

2. **Ran my first Docker container**  
   - Noticed that it did not show in `docker ps`, but appeared in `docker ps -a` because the container exited after running.  

   ![First Container](screenshots/screenshot_2.png)

3. **Worked with Docker Images**  
   - Cleaned up old images using:  
     ```bash
     docker system prune -a
     ```  

   ![Docker Images](screenshots/screenshot_3.png)

4. **Explored Docker Commands**
   - Faced `permission denied` error while using `docker stop`.  
   - Fixed it with reference: [Forum Link](https://forum.storj.io/t/cant-stop-container-permission-denied/25596/2)  
   - Also used:
     ```bash
     docker ps
     docker start <container_id>
     docker rm <container_id>
     docker rmi <image_id>
     ```  

   ![Docker Commands](screenshots/screenshot_4.png)
   ![Error Fix](screenshots/screenshot_5.png)

5. **Built my first Docker Image**
   - Created a Dockerfile (`testdockerfile`)  
   - Faced issue where Docker could not detect it by default  
   - Solved using:  
     ```bash
     docker build -f testdockerfile -t myimage .
     ```
   - Ran the container using:  
     ```bash
     docker run --name mycontainer myimage
     ```  

   ![Docker Build](screenshots/screenshot_6.png)
   ![Docker Run](screenshots/screenshot_7.png)

---

## 🚧 Blockers
- **Permission Denied** error while using `docker stop`.  
- Resolved after guidance from **Vaibhav Sir** ✅  

---

📌 *This marks the completion of my Day 1 progress with Docker.* 🚀
