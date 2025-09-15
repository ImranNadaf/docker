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

2. **Ran my first Docker container**  
   - Noticed that it did not show in `docker ps`, but appeared in `docker ps -a` because the container exited after running.

3. **Worked with Docker Images**  
   - Cleaned up old images using:  
     ```bash
     docker system prune -a
     ```

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

---

## 🚧 Blockers
- **Permission Denied** error while using `docker stop`.  
- Resolved after guidance from **Vaibhav Sir** ✅

---

📌 *This marks the completion of my Day 1 progress with Docker.* 🚀
