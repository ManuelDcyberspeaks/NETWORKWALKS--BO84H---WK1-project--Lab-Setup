<div align="center">

# 🛡️ CYBERSECURITY LAB DEPLOYMENT

**Developing a secure virtual environment for ethical hacking and cybersecurity training**
</div>


<img width="1007" height="831" alt="Copilot_20261027_105204" src="https://github.com/user-attachments/assets/b2c4ae05-abb6-4cbe-94e3-65bbfaa1a0fd" />


<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-C00000?style=for-the-badge&labelColor=404040" />
  <img src="https://img.shields.io/badge/VirtualBox-v6-0070C0?style=for-the-badge&labelColor=000000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=for-the-badge&labelColor=000000&logo=kalilinux&logoColor=white" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Linux-Skill-C00000?style=for-the-badge&labelColor=404040" />
  <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-238F89?style=for-the-badge&labelColor=000000" />
  <img src="https://img.shields.io/badge/Penetration%20Testing-C00000?style=for-the-badge&labelColor=000000&logo=kalilinux&logoColor=white" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Virtualization-Skill-C00000?style=for-the-badge&labelColor=404040" />
  <img src="https://img.shields.io/badge/GitHub-0070C0?style=for-the-badge&labelColor=404040&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=for-the-badge&labelColor=000000&logo=kalilinux&logoColor=white" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/NetworkWalks-C00000?style=for-the-badge&labelColor=404040" />
  <img src="https://img.shields.io/badge/ManueldCyberspeaks-404040?style=for-the-badge&labelColor=0070C0" />
</p>
---

## 🛡️ PROJECT OUTLINE

This project is arranged to establishing a virtual cybersecurity lab for penetration testing and ethical hacking using VirtualBox and Kali Linux.

The lab provides a safe, controlled environment where security tools can be deployed to perform tasks such as network scanning, reconnaissance, vulnerability analysis, and exploit testing in a repeatable manner.

Configured on a private virtual network, the setup allows for the addition of multiple machines that can serve as target systems for authorized security experiments and training.

---




## 🛡️ METHODOLOGIES

The main goals of this project are to:

- Set up and configure VirtualBox as the virtualization platform.
- Deploy Kali Linux as a guest operating system within the VM.
- Establish a dedicated NAT-based virtual network for the lab environment.
- Enable and verify network connectivity for the Kali Linux instance.
- Assign a static IP address to the Kali VM for consistency.
- Confirm proper DNS resolution and internet access from the VM.
- Capture a baseline snapshot of the virtual machine for quick recovery.
- Record and document the entire installation and configuration process.
- Prepare the lab as a foundation for advanced cybersecurity experiments.


  ----

## 🛡️ SCOPE OF THE LAB ENVIRONMENT

This virtual lab is designed to provide a safe and controlled environment for exploring cybersecurity concepts and practicing authorized security assessments.

It serves as a platform for:

- Conducting reconnaissance on networks
- Performing port and service discovery
- Identifying and analyzing vulnerabilities
- Inspecting and interpreting packet traffic
- Testing web application defenses
- Practicing exploitation techniques
- Experimenting with security tools in a repeatable setup

⚠️ **Note:** This environment is strictly for educational and authorized use. Activities must only target systems you own or have explicit permission to test. Unauthorized use against external systems is prohibited.

----

## 🛡️ LAB BLUEPRINT



<img width="1109" height="494" alt="Screenshot 2026-08-10 234811" src="https://github.com/user-attachments/assets/8ce0edd8-f3e6-4e20-9e2e-83567f1a8c08" />

This environment is scalable, enabling new virtual hosts to be introduced for advanced experiments..

----

## 🛡️ LAB CONFIGURATION

| 🧩 Component       | ⚙️ Configuration   |
| ------------------ | ------------------  |
| 🖥️ Host OS         | Windows 11PRO         |
| 🧠 Host RAM        | 16 GB               |
| ⚡ Processor       | Intel Core i7      |
| 🧰 Hypervisor      | VirtualBox 7.2  |
| 🐉 Security OS     | Kali Linux 2026.2  |
| 🧠 Kali RAM        | 2048 MB            |
| 🌐 Virtual Network | NAT Network        |
| 📡 Network Address | 10.0.2.0/24        |
| 🐧 Kali IP Address | 10.0.0.3/24        |
| 🚪 Default Gateway | 10.0.2.1           |
| 🌍 DNS Server      | 8.8.8.8            |

  
-----

# 🛡️LAB DEPLOYMENT

## Step 1. Install 7-Zip

7-Zip was installed to extract the Kali Linux virtual-machine package, which may be distributed as a `.7z` archive.

**Tool:** 7-Zip

---

## Step 2. INSTALL VIRTUALBOX

VirtualBox was installed as the hypervisor.

---

## Step 3. CREATE NATNETWORK
A controlled NAT networking setup was deployed inside VirtualBox.

Configuration:
Network Name: NatNetwork
IPv4 Prefix:  10.0.2.0/24
IPv6:        Disabled
DHCP:         Enabled


<img width="1280" height="690" alt="image" src="https://github.com/user-attachments/assets/c0a2b242-5d9d-453f-8dd0-7ae45edc21d7" />



A NAT-based network was chosen because it enables multiple virtual machines to communicate internally while still maintaining outbound connectivity to external resources. This design ensures that future attacker and target VMs can interact within the lab environment without exposing them directly to the wider internet.

---

## Step 4. IMPORT KALI LINUX

The Kali Linux virtual machine was downloaded from the official Kali Linux website and imported into VirtualBox.

The VM network adapter was configured as follows:

```text
Adapter 1
Attached to: NAT Network
Network:     NatNetwork
Adapter Type: Intel PRO/1000 MT Desktop(82540EM)
```

ALLOCATED VirtualMachine:

```text
RAM: 2048 MB
```
<img width="2560" height="1252" alt="image" src="https://github.com/user-attachments/assets/a876ef58-6c26-484a-b9ba-76bdb02a084a" />

To simplify file management, a shared folder was created for seamless transfer between the host and Kali VM.



---

## Step 5. KALI LINUX NETWORK CONFIGURATION

The Kali Linux network configuration was checked and configured with a consistent IPv4 address.

my BLUEPRINT:

```text
IP Address: 10.0.0.3
Subnet Mask: 255.255.255.0
Gateway: 10.0.2.1
DNS: 8.8.8.8
```


## Step 6. SAVE A RECOVERY SNAPSHOT

Once the setup was finalized, a snapshot of the Kali VM was taken in VirtualBox.

Snapshot view name:

```text
Baseline Kali – Network Configured
...

This snapshot captures the clean starting point of the laboratory. Any future misconfigurations or issues can be resolved by restoring to this saved state.


# 🛡️ LAB VERIFICATION 

| ✅ Test                        | 🧾 Command                      | 🎯 Expected Result              |
| ----------------------------- | ------------------------------- | ------------------------------    |
| 🌐 Check IP address           | `ip a`                          | Exact Kali IP displayed           |
| 📡 Gateway testing            | `ping 10.0.2.1`                 | Successful response              |
| 🌍 Internet connectivity      | `ping 8.8.8.8`                  | Successful response           |
| 🔎 Test DNS resolution        | `nslookup networkwalks.com`     | Domain responds              |
| 🧰 Verify Nmap                | `nmap --version`                | Nmap version displayed          |
| 🔄 Snapshot verification      | Restore snapshot and run `ip a` | Snapshot configuration recovered |

### Evidence Results

```text
IP Address:
10.0.0.3/24

Gateway:
10.0.0.1

DNS:
8.8.8.8
...


<img width="2560" height="1252" alt="image" src="https://github.com/user-attachments/assets/121004ee-2d0e-4e32-9b3d-045d3556b5d8" />
<img width="2560" height="1252" alt="image" src="https://github.com/user-attachments/assets/2a49dcc0-d06f-4db4-9fbd-dedcba06fd3f" />
<img width="2560" height="1252" alt="image" src="https://github.com/user-attachments/assets/4535ee06-2c64-4e72-a984-00a7fe6b7ec0" />

----






# 🔑 KEY TAKEAWAYS FROM LAB DEPLOYMENT


### 1. Snapshots as Recovery Points


Creating snapshots in VirtualBox provides a reliable way to preserve the lab’s baseline state. This means that after completing the initial setup, you can always COME back to a clean configuration if experiments break the system. Snapshots save time, prevent repetitive reinstallation, and allow safe exploration of advanced tools without fear of permanent damage.


### 2. NAT Network vs. Other Networking Modes

Choosing a NAT network offers a balance between isolation and connectivity. Unlike Bridged Mode, which exposes VMs directly to the host’s physical network, NAT keeps them contained while still allowing outbound internet access. Compared to Host‑Only Mode, NAT enables communication between VMs and external resources, making it ideal for attacker–target simulations while maintaining security boundaries.


### 3. Static IP Addressing for Consistency

I learned how to assign a static IP to the Kali VM ensures predictable connectivity. Without it, DHCP could assign different addresses on each boot, breaking scripts, tools, or configurations that rely on a fixed target. Static IPs make penetration testing exercises repeatable and simplify multi‑VM setups where attacker and victim machines need consistent communication paths.

### 4. Documentation as a Learning Asset

I also make sure i recorded every step of the setup process which will serve a valuable reference guide. Documentation not only helps you troubleshoot issues later but also serves as a teaching resource for others. It transforms the lab from a personal experiment into a reusable framework for future projects, ensuring that knowledge is saved and shared.

### 5. Scalability for Future Projects

By designing the lab with modularity in mind, additional VMs can be added seamlessly. This scalability allows you to simulate real‑world attack scenarios with multiple targets, practice lateral movement, and expand into advanced topics like intrusion detection or web application testing. The initial deployment lays the foundation for a growing cybersecurity playground.


----

### Security and Ethical Use of the Lab

Making sure the lab is treated as a training ground for responsible cybersecurity practice. The skills developed here should be applied to strengthen defenses, not to exploit vulnerabilities for malicious purposes.

----




# 🛡️ RESOURCES AND TOOLS USED

- **7-Zip:** [https://7-zip.org/download.html](https://7-zip.org/download.html)
- **VirtualBox:** [https://virtualbox.org/wiki/Downloads](https://virtualbox.org/wiki/Downloads)
- **Kali Linux:** [https://kali.org/get-kali](https://kali.org/get-kali)


---


# 👤 AUTHOR
**POPOOLA EMMANUEL BABALOLA(Manueldcyberspeaks)**\
Cybersecurity Intern at NETWORKWALKS


---


