# Task 4: Setup and Use a Firewall on Windows/Linux

## Author  
**Kush Thaker**  
📧 kthaker442@gmail.com  

---

## Steps Followed

### Step 0: Identifying Operating System  
For this task, I used my Primary PC running **Windows 11 (Phoenix)**.

---

### Step 1: Open Firewall Configuration Tool  
To open Windows Firewall configuration tool:  
- Pressed **Win + R**  
- Typed: `wf.msc`  
- Pressed **Enter**  
- Navigated to **Inbound Rules** and located the option to add a **New Rule**.

---

### Step 2: List Current Firewall Rules  
- Inside the Firewall Manager, I navigated to **Inbound Rules**.  
- This section displayed a list of pre-configured rules managing traffic for different applications and services.  
- Reviewed these existing rules before applying new custom rules.

---

### Step 3: Add a Rule to Block Inbound Traffic on a Specific Port  
To block **Telnet (Port 23)**:  
- Clicked **New Rule…** → Selected **Port** → Clicked **Next**  
- Chose **TCP**  
- Entered **23** in “Specific local ports”  
- Selected **Block the connection**  
- Applied the rule to **Domain, Private, Public** profiles  
- Named the rule: **Block Telnet (Port 23)**  
- Clicked **Finish**  

The rule appeared in the inbound rules list.

---

### Step 4: Testing the Rule  
To test the block rule:  
- Enabled **Telnet Client** (via Control Panel → Programs and Features → Turn Windows features on or off → Checked *Telnet Client*)  
- Tested with the command:  
  ```bash
  telnet localhost 23
  ```  
- The connection failed, proving the firewall successfully blocked inbound Telnet traffic.

---

### Step 5: Remove the Test Block Rule  
After testing:  
- Navigated to **Inbound Rules**  
- Located **Block Telnet (Port 23)**  
- Right-clicked → **Delete**  

This restored the firewall to its original state.

---

## Summary  
- **Open Firewall Manager**: `Win + R` → `wf.msc`  
- **Create Rule**: Inbound Rules → New Rule… → Port → TCP → 23 → Block  
- **Enable Telnet Client**: Control Panel → Programs and Features → Turn Windows features on or off  
- **Test Connection**: `telnet localhost 23`  
- **Remove Rule**: Right-click → Delete  

A firewall filters traffic based on rules:  
- If a packet matches a block rule, it is **denied**.  
- If a packet matches an allow rule, it is **permitted**.  

This task demonstrated blocking Telnet (port 23) and later restoring original settings.  

---

## 📂 Additional Resources  
- For the **detailed report**, check the file **Task4Report.pdf** in the main branch of this repository.  
- All **screenshots of every step** are uploaded in the **images** folder of the main branch.

---

**Regards,**  
*Kush Thaker*  
