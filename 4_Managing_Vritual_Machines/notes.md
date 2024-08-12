# **Managing Virtual Machines** 🖥️

> **Outline**:

- [ ] Basic VM Management
- [ ] Snapshot and Cloning
- [ ] VM Resource Management

---

## **Content**

### **Basic VM Management** 📋

#### **Basic VM Management Table**

| **Management Task**     | **Description**                                          | **How to Perform**                                                                |
| ----------------------- | -------------------------------------------------------- | --------------------------------------------------------------------------------- |
| **Power On/Off**        | Starting or stopping the VM.                             | Right-click on the VM in the vSphere client and select `Power On` or `Power Off`. |
| **Suspend/Resume**      | Pausing and resuming the VM's state.                     | Right-click on the VM and select `Suspend` or `Resume`.                           |
| **Restart**             | Rebooting the VM.                                        | Right-click on the VM and choose `Reboot` from the options.                       |
| **Edit Settings**       | Changing VM configuration like CPU, memory, or storage.  | Right-click on the VM, select `Edit Settings`, and adjust the configurations.     |
| **Snapshot Management** | Creating, deleting, and managing snapshots.              | Use the `Snapshots` tab to create or delete snapshots and manage them.            |
| **Clone VM**            | Making a copy of the VM for testing or deployment.       | Right-click on the VM, select `Clone`, and follow the cloning wizard.             |
| **Resource Allocation** | Adjusting the VM’s allocated resources (CPU, RAM, Disk). | Right-click on the VM, select `Edit Settings`, and modify resource settings.      |

### **Snapshot and Cloning** 📸🔄

#### **Snapshot** 📸

- **What is a Snapshot?**  
  A snapshot is a point-in-time image of a VM’s state, including its disk, memory, and settings. It allows you to revert to a previous state if needed.

- **How to Make a Snapshot from VM?**

  1. **Open vSphere Web Client** 🌐
  2. **Select the VM** 🖥️
  3. **Go to the `Snapshots` Tab** 📂
  4. **Click `Take Snapshot`** 📸
  5. **Enter Snapshot Name and Description** 📝
  6. **Choose Snapshot Options** (e.g., `Quiesce` option)
  7. **Click `OK`** to create the snapshot.

- **What is `Quiesce`?**  
  Quiesce ensures that the VM’s file system and applications are in a consistent state before taking the snapshot. It minimizes data corruption.

- **How to Merge Data for Current Time to Snapshot Time?**  
  To merge data, revert the VM to a snapshot and then delete or consolidate snapshots. This process integrates changes made after the snapshot was taken.

#### **Cloning** 🔄

- **What is Cloning a VM?**  
  Cloning creates a copy of an existing VM. It can be a full clone (independent of the original) or a linked clone (depends on the original VM’s disk).

- **How to Clone a VM?**
  1. **Open vSphere Web Client** 🌐
  2. **Select the VM** 🖥️
  3. **Right-click on the VM and Choose `Clone`** 🔄
  4. **Follow the Cloning Wizard** to specify the name, destination, and other options.
  5. **Complete the Wizard** to create the cloned VM.

#### **Snapshot vs Backups** 📸💾

| **Aspect**      | **Snapshot**                                 | **Backup**                                                          |
| --------------- | -------------------------------------------- | ------------------------------------------------------------------- |
| **Definition**  | A point-in-time image of the VM’s state.     | A copy of the VM’s data and configuration, often stored externally. |
| **Purpose**     | Revert to a previous state quickly.          | Restore data in case of failure or corruption.                      |
| **Storage**     | Stored in the same datastore as the VM.      | Typically stored in a different location (e.g., network storage).   |
| **Performance** | Minimal performance impact during creation.  | May impact performance during backup operations.                    |
| **Frequency**   | Used for short-term recovery.                | Used for long-term data protection and disaster recovery.           |
| **Retention**   | Retained with the VM until manually deleted. | Managed through backup policies and schedules.                      |

### **VM Resource Management** 📊

- **What are Resources for VM?**  
  Resources include CPU, memory, disk space, and network bandwidth allocated to the VM.

  - **Example**:  
    Suppose you have a VM with 2 CPUs and 4 GB of RAM. These resources are allocated based on the needs of the VM’s applications and services.

  - **Adjusting Resources**:
    1. **Open vSphere Web Client** 🌐
    2. **Select the VM** 🖥️
    3. **Right-click and Choose `Edit Settings`** ⚙️
    4. **Modify CPU, Memory, and Disk Settings** according to requirements.
    5. **Click `OK`** to apply changes.

---
