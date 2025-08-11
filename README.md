# CST8316 Final Exam Companion – Scenario-Based Study Guide

> A holistic troubleshooting study guide for PC hardware, software, and user-related issues.
> Built from Jeopardy review questions and CST8316 course content, but organized around the
> real-world lifecycle of building and maintaining a computer environment.

---

## 1. Planning & Design

Before you touch a screwdriver or install an OS, planning ensures the system is compatible, reliable, and future-proof.  
This stage addresses **component selection**, **compatibility checks**, **initial risk management**, and **design for maintainability**.

### 1.1 Component Compatibility

**Example Checkpoint Question**  
> *SAS cards can also support drives of this interface type.*  
**Answer:** SATA.

**Why This Matters:**  
SAS controllers are backward compatible with SATA drives, giving flexibility in storage planning. This means you can mix high-performance SAS drives with cost-effective SATA drives in the same server. Knowing compatibility upfront avoids wasted purchases and integration delays.

**Broader Exam Connection:**  
Questions about **interface compatibility** could appear for:
- USB versions and backward compatibility.
- RAM generations (DDR3 vs DDR4).
- PCIe lane requirements for GPUs.

**Course Reference:** *Troubleshooting Storage Drives*, p.1–2.

---

### 1.2 Maintenance Scheduling

**Example Checkpoint Question**  
> *This is a computer systems maintenance item usually only performed once or twice a year.*  
**Answer:** Physical cleaning of the inside of the computer.

**Why This Matters:**  
Dust buildup reduces cooling efficiency, increases fan wear, and causes overheating. In an enterprise, dust can also void warranties if service contracts require preventive maintenance logs.

**Broader Exam Connection:**  
Any question about:
- Preventive maintenance schedules.
- Environmental controls (humidity, air filtration).
- Cooling system troubleshooting.

**Course Reference:** *Preventive Maintenance*, p.2.

---

### 1.3 Power & Reliability Metrics

**Example Checkpoint Question**  
> *What term describes the average time between hardware failures in a large sample?*  
**Answer:** MTBF (Mean Time Between Failures).

**Why This Matters:**  
MTBF influences procurement, especially for enterprise storage arrays or critical servers. A low MTBF means you should keep more spares on hand or select a more reliable vendor.

**Broader Exam Connection:**  
Could also be framed as:
- Selecting between HDD and SSD for reliability.
- Choosing redundant PSU configurations.

**Course Reference:** *Preventive Maintenance*, p.6–7.

---

### 1.4 Planning for Security

Even in early design, you must plan how to **authenticate users**, **protect data**, and **log activity**.

**Example Checkpoint Question**  
> *In Windows Event Viewer, which log records user login attempts?*  
**Answer:** Security log.

**Why This Matters:**  
In a business setup, tracking logins can detect unauthorized access attempts early. For a home lab, it can help identify brute-force attacks on remote desktop services.

**Broader Exam Connection:**  
Any event log topic:
- System log (hardware events)
- Application log (software issues)

**Course Reference:** *Troubleshooting in Windows*, p.15.

---

### 1.5 Planning for Recovery

**Example Checkpoint Question**  
> *In data recovery, what’s the safest first step when files are accidentally deleted?*  
**Answer:** Stop writing to the drive immediately.

**Why This Matters:**  
Writing new data can overwrite deleted file sectors, making recovery impossible. In an enterprise, this could mean disconnecting the affected storage volume before engaging recovery services.

**Broader Exam Connection:**  
Similar logic applies to:
- Snapshot/backup creation.
- System Restore points.
- Imaging a failing drive before troubleshooting.

**Course Reference:** *Basic Data Recovery*, p.2–3.

---

### Practical Scenario: Enterprise vs. Home Build

- **Enterprise Example:** Designing a small business server room with a mixed SAS/SATA RAID array, hot-swappable PSUs with high MTBF, and a quarterly cleaning log in the maintenance schedule.
- **Home Example:** Building a gaming PC with an SSD + HDD combo, keeping cleaning tools for annual dust removal, and configuring Windows to log failed login attempts for remote gaming accounts.

---

**Key Troubleshooting Concepts in Planning Stage:**
1. Choose compatible hardware to avoid integration issues.
2. Consider preventive maintenance from day one.
3. Build in redundancy and reliability metrics.
4. Include security and logging in initial design.
5. Prepare a recovery strategy before disaster strikes.


## 2. Hardware Assembly & Initial Testing

Once the design is finalized and components are selected, the next step is assembling the hardware and ensuring it passes initial diagnostics.  
This stage covers **POST behavior**, **component seating**, **drive installation**, and **cable management**.

---

### 2.1 POST and Beep Codes

**Example Checkpoint Question**  
> *Which beep code usually indicates a memory problem?*  
**Answer:** Continuous beeping.

**Why This Matters:**  
Beep codes are the first diagnostic language of your system. Continuous beeping often means RAM is missing, improperly seated, or defective. Recognizing beep patterns speeds up diagnosis before software tools are even available.

**Broader Exam Connection:**  
Other beep-related questions could cover:
- Keyboard failures (3 long beeps).
- Video card failure (series of short beeps).
- No POST at all (possible CPU failure or power issue).

**Course Reference:** *POST Cards*, p.2.

---

### 2.2 Physical Component Issues

**Example Checkpoint Question**  
> *Which component of a hard disk contains the read/write heads?*  
**Answer:** Actuator arm assembly.

**Why This Matters:**  
If the actuator fails, even temporarily, it can cause bad sectors or total data loss. Physical drive faults need quick detection to prevent cascading failures.

**Broader Exam Connection:**  
Could lead into questions about:
- SSD vs HDD differences.
- Data recovery priorities.
- Mechanical vs electrical storage issues.

**Course Reference:** *Troubleshooting Storage Drives*, p.1–2.

---

### 2.3 Printer Hardware Integration

**Example Checkpoint Question**  
> *Which component of a laser printer fuses the toner to the paper?*  
**Answer:** Fuser assembly.

**Why This Matters:**  
In an office build, integrating networked laser printers means understanding their mechanical parts for maintenance contracts. A failing fuser means every print job is compromised until fixed.

**Broader Exam Connection:**  
Could also test knowledge of:
- Primary corona wire (charging drum).
- Photoreceptor drum (image holding).
- Development stage (toner application).

**Course Reference:** *Troubleshooting Printers*, p.2–4.

---

### 2.4 Memory Installation

**Example Checkpoint Question**  
> *Which type of RAM is commonly used in modern desktop systems?*  
**Answer:** DDR4 SDRAM.

**Why This Matters:**  
Incorrect RAM type or speed can prevent booting or cause random crashes. Knowing the standard (DDR4 for modern desktops) ensures compatibility during assembly.

**Broader Exam Connection:**  
Could be reframed as:
- Laptop RAM types (SO-DIMM).
- ECC memory for servers.
- Dual-channel configuration benefits.

**Course Reference:** *Troubleshooting Memory*, p.2–3.

---

### 2.5 Cabling & Connectivity

**Example Checkpoint Question**  
> *Which cable type uses copper to transmit signals as electrical pulses?*  
**Answer:** Twisted pair (Ethernet) cable.

**Why This Matters:**  
Proper cabling avoids signal loss and network instability. In a build phase, especially for enterprises, CAT6 or better is recommended for gigabit or higher speeds.

**Broader Exam Connection:**  
Could extend into:
- Fiber vs copper trade-offs.
- HDMI carrying both audio and video.
- Cable shielding and interference reduction.

**Course Reference:** *PC Troubleshooting Tips*, p.5.

---

### 2.6 Initial Testing

**Example Checkpoint Question**  
> *What does POST stand for?*  
**Answer:** Power-On Self-Test.

**Why This Matters:**  
POST ensures all essential hardware is functioning before the OS loads. Skipping attention to POST messages can cause you to miss early signs of hardware failure.

**Broader Exam Connection:**  
Exam might test:
- Specific POST sequence steps.
- Differences between BIOS and UEFI POST behavior.
- POST card usage for diagnosing failures.

**Course Reference:** *POST Cards*, p.1.

---

### Practical Scenario: Enterprise vs. Home Build

- **Enterprise Example:** After rack-mounting a server, you power it on, hear three long beeps — you immediately check and reseat the keyboard connection, log the incident, and run a POST card check for additional errors.
- **Home Example:** You install new RAM, hear continuous beeping, and recall from your study guide that it means a RAM fault — you swap back the old RAM and confirm boot success.

---

**Key Troubleshooting Concepts in Assembly Stage:**
1. Listen for and interpret POST beep codes immediately.
2. Visually check component seating before software troubleshooting.
3. Understand major subsystems in peripherals like printers.
4. Match memory type, speed, and configuration to motherboard specs.
5. Verify all cabling meets required data rates and environmental conditions.
6. Use POST results as a foundation for further diagnostics.

## 3. OS Installation & Configuration

Once hardware passes initial testing, the operating system is installed.  
This stage focuses on **driver installation**, **startup optimization**, **system restore setup**, and **built-in diagnostic tools**.

---

### 3.1 Boot Modes for Troubleshooting

**Example Checkpoint Question**  
> *In Windows, which boot option loads the last configuration that worked successfully?*  
**Answer:** Last Known Good Configuration.

**Why This Matters:**  
When a new driver or setting prevents startup, Last Known Good restores registry and driver settings from the last successful boot. This avoids a full reinstall and minimizes downtime.

**Broader Exam Connection:**  
Other boot mode topics include:
- Safe Mode (minimal drivers for troubleshooting).
- Safe Mode with Networking (adds network stack).
- Recovery Environment options.

**Course Reference:** *Troubleshooting in Windows*, p.6.

---

### 3.2 System Restore for Rollbacks

**Example Checkpoint Question**  
> *Which Windows feature creates restore points to roll back system changes?*  
**Answer:** System Restore.

**Why This Matters:**  
System Restore allows rollback of OS files, settings, and drivers without affecting user data. In an enterprise, it’s a quick recovery tool after failed updates.

**Broader Exam Connection:**  
May be asked as:
- How to create a restore point manually.
- Differences between restore points and backups.
- Limitations of System Restore.

**Course Reference:** *Troubleshooting in Windows*, p.13.

---

### 3.3 Disk and Partition Management

**Example Checkpoint Question**  
> *Which Windows utility can manage disk partitions without third-party tools?*  
**Answer:** Disk Management.

**Why This Matters:**  
Disk Management lets you create, delete, resize, and format volumes. In a new system build, you may use it to split OS and data partitions for better maintenance.

**Broader Exam Connection:**  
Could extend into:
- Formatting options (NTFS vs exFAT vs FAT32).
- Using diskpart for CLI-based control.
- Aligning partitions for SSD performance.

**Course Reference:** *Troubleshooting in Windows*, p.10–11.

---

### 3.4 Checking Disk Health

**Example Checkpoint Question**  
> *Which Windows utility can scan the hard disk for errors and attempt to repair them?*  
**Answer:** chkdsk.

**Why This Matters:**  
chkdsk verifies the file system and repairs logical errors, preventing corruption from spreading. In a deployment phase, run it after cloning drives to ensure integrity.

**Broader Exam Connection:**  
Could be about:
- `sfc /scannow` for system file repairs.
- SMART monitoring for physical disk health.
- Disk Cleanup for freeing space.

**Course Reference:** *Troubleshooting in Windows*, p.12.

---

### 3.5 DirectX Diagnostics

**Example Checkpoint Question**  
> *Which Windows utility can help diagnose video and audio issues related to DirectX?*  
**Answer:** DirectX Diagnostic Tool (dxdiag.exe).

**Why This Matters:**  
dxdiag provides driver versions, hardware info, and can run basic video/audio tests. During deployment, you can confirm that drivers installed with no conflicts.

**Broader Exam Connection:**  
May be asked as:
- Steps to open dxdiag.
- Information available under each tab.
- Troubleshooting games or multimedia software.

**Course Reference:** *Troubleshooting in Windows*, p.7.

---

### 3.6 Startup Management

**Example Checkpoint Question**  
> *Which Windows utility can identify startup programs and manage them?*  
**Answer:** Task Manager (Startup tab).

**Why This Matters:**  
Disabling unneeded startup programs reduces boot time and improves performance. In a corporate build, this also helps standardize user environments.

**Broader Exam Connection:**  
Also may be tested:
- msconfig’s role in startup troubleshooting.
- Disabling services for testing conflicts.
- Autoruns for advanced startup management.

**Course Reference:** *Troubleshooting in Windows*, p.9–10.

---

### Practical Scenario: Enterprise vs. Home Build

- **Enterprise Example:**  
  After imaging 50 workstations, a driver update causes boot loops. You boot into Last Known Good on one system to verify the fix, then roll back the update fleet-wide.
  
- **Home Example:**  
  Your gaming PC starts stuttering after a graphics driver update. You run dxdiag, verify the driver date, and use System Restore to revert to a stable configuration.

---

**Key Troubleshooting Concepts in OS Installation & Configuration:**
1. Use boot modes to recover from driver or configuration issues.
2. Leverage System Restore for quick rollback without losing data.
3. Manage partitions and file systems to improve maintainability.
4. Regularly check disk health during and after installation.
5. Verify multimedia subsystems with dxdiag.
6. Optimize startup to improve performance and stability.

## 4. Peripheral & Network Integration

Once the OS is installed and configured, peripherals and network connections must be set up for both functionality and reliability.  
This stage covers **printers**, **audio**, **video**, **network hardware**, and **user interaction skills**.

---

### 4.1 Laser Printer Process Knowledge

**Example Checkpoint Question**  
> *Which stage of the laser printing process applies toner to the latent image on the drum?*  
**Answer:** Developing stage.

**Why This Matters:**  
Knowing the stages (charging, exposing, developing, transferring, fusing, cleaning) allows targeted troubleshooting. If prints are blank but paper feeds, the problem could be in the developing stage or laser exposure.

**Broader Exam Connection:**  
You may also be asked:
- Which part fuses toner to paper (fuser assembly).
- Which part charges the drum (primary corona wire).
- Order of the printing process.

**Course Reference:** *Troubleshooting Printers*, p.2–3.

---

### 4.2 Printer Quality Issues

**Example Checkpoint Question**  
> *Which printer problem is often caused by using incorrect or low-quality toner?*  
**Answer:** Poor print quality (faded or inconsistent).

**Why This Matters:**  
Toner quality impacts fusing and particle distribution. In enterprise settings, procurement standards often specify manufacturer-approved toner to avoid warranty voids.

**Broader Exam Connection:**  
Also applies to:
- Ghosting issues from fuser problems.
- Streaking from dirty rollers.
- Incorrect media type causing smudging.

**Course Reference:** *Troubleshooting Printers*, p.4.

---

### 4.3 Audio Troubleshooting

**Example Checkpoint Question**  
> *Which Windows utility can adjust default playback devices and troubleshoot audio output?*  
**Answer:** Sound settings (mmsys.cpl).

**Why This Matters:**  
Selecting the correct playback device is essential in setups with multiple outputs (speakers, HDMI, USB headsets). Misconfiguration can appear as “no sound” even if hardware is fine.

**Broader Exam Connection:**  
Could also be asked:
- Checking volume mixer.
- Updating audio drivers.
- Using dxdiag to test audio hardware.

**Course Reference:** *Troubleshooting Audio*, p.2.

---

### 4.4 Video Troubleshooting

**Example Checkpoint Question**  
> *In video troubleshooting, what’s a likely cause if a system freezes when trying to play a video?*  
**Answer:** Resource conflict.

**Why This Matters:**  
If two devices compete for the same I/O addresses or IRQs, system instability occurs. Modern systems manage this better, but outdated drivers or add-in cards can still cause conflicts.

**Broader Exam Connection:**  
Also applies to:
- No signal on monitor (GPU or cable fault).
- Distorted video (driver or GPU failure).
- Incorrect resolution settings.

**Course Reference:** *Troubleshooting Video*, p.4.

---

### 4.5 Network Cabling

**Example Checkpoint Question**  
> *Which cable type uses copper to transmit signals as electrical pulses?*  
**Answer:** Twisted pair (Ethernet) cable.

**Why This Matters:**  
Twisted pair cables are the backbone of most LAN setups. Choosing CAT6 or higher is essential for gigabit speeds and future-proofing.

**Broader Exam Connection:**  
Exam could cover:
- Straight-through vs crossover cables.
- Fiber optic cable advantages.
- Shielding types (STP vs UTP).

**Course Reference:** *PC Troubleshooting Tips*, p.5.

---

### 4.6 User Interaction Skills

**Example Checkpoint Question**  
> *In client interaction, why is active listening important?*  
**Answer:** It ensures accurate understanding of the client’s problem.

**Why This Matters:**  
Good communication prevents misdiagnosis. Asking clarifying questions and repeating back the problem builds trust and accuracy.

**Broader Exam Connection:**  
Also applies to:
- Documenting symptoms.
- Managing client expectations.
- Avoiding technical jargon with non-technical users.

**Course Reference:** *Interacting With Clients*, p.2–3.

---

### Practical Scenario: Enterprise vs. Home Build

- **Enterprise Example:**  
  A network printer produces faint output. You recall that poor-quality toner can cause this and recommend switching to approved toner, preventing warranty issues.
  
- **Home Example:**  
  You connect a new gaming monitor via DisplayPort, but the PC freezes when playing a video. You check Device Manager and find the GPU driver is outdated, resolving the conflict after an update.

---

**Key Troubleshooting Concepts in Peripheral & Network Integration:**
1. Understand mechanical and electrical stages of laser printing.
2. Recognize how consumable quality impacts performance.
3. Set correct default devices in OS-level audio settings.
4. Diagnose resource conflicts and driver issues in video output.
5. Select proper cabling for performance and reliability.
6. Practice active listening to accurately capture problem details.


## 5. Security & Maintenance

A stable system isn’t just about performance — it’s also about long-term reliability and defense against security threats.  
This stage covers **preventive maintenance**, **security logging**, **malware prevention**, and **backup strategies**.

---

### 5.1 Preventive Maintenance Schedules

**Example Checkpoint Question**  
> *This is a computer systems maintenance item usually only performed once or twice a year.*  
**Answer:** Physical cleaning of the inside of the computer.

**Why This Matters:**  
Dust accumulation increases temperatures and reduces airflow, leading to shortened component lifespan. Regular internal cleaning is especially important in environments with high particulate matter.

**Broader Exam Connection:**  
Other preventive maintenance topics could include:
- Periodic software updates.
- Verifying backup integrity.
- Battery health checks for UPS and laptops.

**Course Reference:** *Preventive Maintenance*, p.2–3.

---

### 5.2 Security Event Tracking

**Example Checkpoint Question**  
> *In Windows Event Viewer, which log records user login attempts?*  
**Answer:** Security log.

**Why This Matters:**  
Security logs record login successes and failures, account lockouts, and privilege changes. Reviewing them regularly can detect early signs of unauthorized access.

**Broader Exam Connection:**  
Could be reframed as:
- Identifying the System log for hardware events.
- Using Application logs for software troubleshooting.
- Configuring audit policies for detailed logging.

**Course Reference:** *Troubleshooting in Windows*, p.15.

---

### 5.3 Malware Prevention

**Example Checkpoint Question**  
> *What is the best first step after detecting malware on a workstation?*  
**Answer:** Disconnect it from the network.

**Why This Matters:**  
Disconnecting prevents malware from spreading or communicating with control servers. Immediate isolation is critical in both enterprise and home setups.

**Broader Exam Connection:**  
Could also test:
- Running antivirus in Safe Mode.
- Using offline scanning tools.
- Steps for incident response in security breaches.

**Course Reference:** *Computer Security*, p.5–6.

---

### 5.4 Backup Strategy Design

**Example Checkpoint Question**  
> *What backup type only saves files changed since the last full backup?*  
**Answer:** Incremental backup.

**Why This Matters:**  
Incremental backups are storage-efficient but require the full backup and all subsequent incrementals to restore. Enterprises often combine full + incremental to balance recovery time and resource usage.

**Broader Exam Connection:**  
Could also include:
- Differential backups.
- Image-based backups.
- Cloud vs on-premise backup strategies.

**Course Reference:** *Preventive Maintenance*, p.5–6.

---

### 5.5 Data Recovery Basics

**Example Checkpoint Question**  
> *In data recovery, what’s the safest first step when files are accidentally deleted?*  
**Answer:** Stop writing to the drive immediately.

**Why This Matters:**  
New writes can overwrite the data’s physical location on the drive, making recovery impossible. In enterprise contexts, pulling the drive and cloning it before recovery attempts is standard practice.

**Broader Exam Connection:**  
Could be asked as:
- Using write blockers.
- Imaging before recovery attempts.
- File carving tools for deleted files.

**Course Reference:** *Basic Data Recovery*, p.2–3.

---

### Practical Scenario: Enterprise vs. Home Build

- **Enterprise Example:**  
  Security logs show multiple failed logins from a remote IP. You isolate the system, check event IDs in the Security log, and verify that no other machines are compromised.  
  Preventive maintenance includes dust removal from desktops during quarterly on-site service.

- **Home Example:**  
  Your personal PC suddenly slows down. You find an unknown background process, disconnect from Wi-Fi, run an offline antivirus scan, and later set up a weekly incremental backup to an external drive.

---

**Key Troubleshooting Concepts in Security & Maintenance:**
1. Follow preventive maintenance schedules for both hardware and software.
2. Regularly review logs for early signs of intrusion or malfunction.
3. Isolate infected systems before attempting cleanup.
4. Use a layered backup strategy for faster recovery and better data protection.
5. Protect recoverable data by avoiding unnecessary writes.


## 6. Troubleshooting Methodology

A disciplined troubleshooting process is the foundation of both PC repair and enterprise IT support.  
Following a structured approach ensures efficiency, accuracy, and clear documentation.

---

### 6.1 The Standard Troubleshooting Steps

**Example Checkpoint Question**  
> *During which step in the troubleshooting process would you attempt to recreate the situation that caused the symptom?*  
**Answer:** Test the theory.

**Why This Matters:**  
Testing the theory means reproducing the issue under controlled conditions to confirm its cause. Without confirmation, you risk applying fixes for the wrong problem.

**Broader Exam Connection:**  
Other troubleshooting steps may be tested:
- Identify the problem.
- Establish a theory of probable cause.
- Establish a plan of action.
- Verify full system functionality.
- Document findings.

**Course Reference:** *The Troubleshooting Procedure*, p.2–3.

---

### 6.2 Using Flowcharts

**Example Checkpoint Question**  
> *What is the main advantage of using a troubleshooting flowchart?*  
**Answer:** It provides a logical sequence for problem resolution.

**Why This Matters:**  
Flowcharts help technicians follow a consistent path, ensuring no diagnostic steps are skipped. They’re especially useful for less experienced techs or for complex multi-stage problems.

**Broader Exam Connection:**  
Could be reframed as:
- How to follow a decision point in a chart.
- Benefits of branching troubleshooting logic.
- Visual vs textual troubleshooting guides.

**Course Reference:** *Troubleshooting FlowChart Poster*.

---

### 6.3 Gathering Information

**Example Checkpoint Question**  
> *Why is active listening a critical skill in troubleshooting?*  
**Answer:** It ensures accurate understanding of the client’s problem.

**Why This Matters:**  
Many issues are described vaguely by users. Asking clarifying questions and summarizing back to the client prevents misdiagnosis and wasted time.

**Broader Exam Connection:**  
Other related skills:
- Avoiding technical jargon.
- Documenting symptoms in the client’s own words.
- Verifying client-reported steps that caused the issue.

**Course Reference:** *Interacting With Clients*, p.2–3.

---

### 6.4 Documentation

**Example Checkpoint Question**  
> *Why is documenting troubleshooting steps important even after a successful fix?*  
**Answer:** To create a record for future reference and improve efficiency.

**Why This Matters:**  
Documentation helps other techs resolve similar problems faster, supports compliance requirements, and provides evidence of work completed.

**Broader Exam Connection:**  
Could be about:
- Ticketing systems.
- Service logs.
- Knowledge base articles.

**Course Reference:** *The Troubleshooting Procedure*, p.3.

---

### 6.5 Verification & Prevention

**Example Checkpoint Question**  
> *What is the final step in any troubleshooting process?*  
**Answer:** Verify full system functionality and implement preventive measures.

**Why This Matters:**  
Ensuring the issue is truly fixed prevents repeat service calls. Preventive measures (updates, settings changes, training) reduce the chance of recurrence.

**Broader Exam Connection:**  
Could extend to:
- Stress testing hardware after replacement.
- Running extended diagnostics before sign-off.
- Adding protective hardware/software after repair.

**Course Reference:** *Preventive Maintenance*, p.6–7.

---

### Practical Scenario: Enterprise vs. Home Build

- **Enterprise Example:**  
  A user reports their network printer is offline.  
  You gather details (active listening), test the theory by pinging the printer’s IP, find that the static IP conflicts with another device, and resolve it by changing the printer’s address.  
  You document the fix in the service ticket system and update the network map to prevent future conflicts.

- **Home Example:**  
  Your PC randomly shuts down.  
  You reproduce the issue by running a stress test, discover CPU temps spiking, clean dust from the heatsink, and replace dried thermal paste.  
  You log this in your personal build notes for future reference.

---

**Key Troubleshooting Concepts in Methodology:**
1. Always follow a structured problem-solving framework.
2. Use flowcharts for logical decision-making.
3. Gather accurate information through client interaction.
4. Document every step for future efficiency.
5. Verify fixes and implement preventive measures to avoid repeat issues.


