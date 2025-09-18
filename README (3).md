# 📅 Day 03 – Docker Networking  

Today’s focus was on exploring different Docker networking modes through 4 practical tasks.  

---

## ✅ Tasks Completed  

### Task 1 – Explore the Default Bridge Network  
- Ran one **nginx** container and one **alpine** container (default bridge).  
- Installed `curl` inside alpine.  
- Tried accessing nginx using container name → ❌ failed.  
- Access worked only with container **IP address**.  

👉 **Lesson:** Default bridge uses IP-based communication, not container names.  

---

### Task 2 – Run a Container With No Network  
- Started an alpine container with `--network none`.  
- Verified it only had the loopback interface (`lo`).  
- No internet access, no communication with other containers.  

👉 **Lesson:** `--network none` provides total isolation.  

---

### Task 3 – Use a Custom Bridge Network  
- Created a user-defined bridge network (`mynet`).  
- Ran **MySQL** and **WordPress** containers inside this network.  
- WordPress connected to MySQL using the hostname **`db`**, not an IP.  

👉 **Lesson:** Custom bridge allows DNS-based service discovery (containers can talk by name).  

---

### Task 4 – Attach a Container to Multiple Networks  
- Created two networks (`mynet`, `mynet2`).  
- Ran one alpine container in `mynet`.  
- Connected the same container to `mynet2`.  
- Inspected container → saw **two IP addresses** (one for each network).  

👉 **Lesson:** A container can join multiple networks, making it multi-homed.  

---

## 📖 Learnings  
- Default bridge = IP-based communication only.  
- Custom bridge = DNS-based discovery (name resolution).  
- `--network none` = full isolation.  
- Containers can attach to multiple networks simultaneously.  

---
