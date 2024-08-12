# **vSphere ESXi Management** 🌐

> **Outline**:

- [x] Access ESXi through vSphere (web client)
- [x] Access ESXi through SSH
- [x] Create a new VM on vSphere environment
- [x] Download and install OS on vSphere VM

---

## **Content**

### **Access ESXi through vSphere (Web Client)** 🌐

#### **How to Connect ESXi through vSphere?**

To access and manage your ESXi host through the vSphere Web Client:

1. **Open a Web Browser** 🌍

   - Use a browser like Chrome, Firefox, or Edge.

2. **Enter the ESXi Host URL** 🌐

   - In the address bar, enter the IP address or hostname of your ESXi host. For example: `https://<ESXi_IP_Address>/`.

3. **Log In to the vSphere Web Client** 🔐

   - Enter the root username and password.
   - Click `Login` or press `Enter`.

4. **Navigate the vSphere Web Client** 🗂️

   - You’ll be directed to the main dashboard where you can manage your ESXi host and VMs.

   ![vSphere Web Client](https://www.vmware.com/content/dam/digitalmarketing/vmware/en/images/vsphere-web-client.png)

#### **Common vSphere Configuration Table**

| Configuration Item        | Description                                         |
| ------------------------- | --------------------------------------------------- |
| **Host IP Address**       | The IP address of the ESXi host.                    |
| **Port**                  | Default port is `443` for secure connections.       |
| **Username**              | Usually `root` for administrative access.           |
| **Password**              | Password set during ESXi installation.              |
| **Datacenter**            | Logical grouping of ESXi hosts and VMs.             |
| **Cluster**               | A group of ESXi hosts for resource management.      |
| **Resource Pool**         | Logical container for managing resource allocation. |
| **Storage**               | Datastores used for VM storage.                     |
| **Network Configuration** | Network settings for VM network connectivity.       |

### **Access ESXi through SSH** 🔐

#### **How to Connect ESXi through SSH using PuTTY**

1. **Enable SSH on ESXi** 🛠️

   - Access the ESXi console.
   - Press `F2` to customize the system.
   - Navigate to `Troubleshooting Options` and enable `SSH`.

2. **Download and Install PuTTY** 📥

   - Download from [PuTTY’s official website](https://www.putty.org/).

3. **Open PuTTY** 💻

   - Launch the application.

4. **Configure PuTTY Connection** 🌐

   - Enter the ESXi IP address in the `Host Name (or IP address)` field.
   - Set the `Port` to `22` and select `SSH`.

5. **Connect and Log In** 🔑

   - Click `Open`.
   - Accept any security alerts.
   - Log in with root username and password.

   ![PuTTY Terminal](https://www.putty.org/images/putty_terminal.png)

### **Create a New VM on vSphere Environment** 🖥️

#### **How to Create a New VM on vSphere**

1. **Open vSphere Web Client** 🌐

   - Log in as described above.

2. **Navigate to the Datacenter** 🗂️

   - Click on the `Datacenter` where you want to create the VM.

3. **Create a New Virtual Machine** ➕

   - Right-click on the `Datacenter` or `Cluster` and select `New Virtual Machine`.
   - Follow the `New Virtual Machine Wizard`.

4. **Configure VM Settings** ⚙️

   - **Name**: Enter a name for the VM.
   - **Compatibility**: Select compatibility settings.
   - **Datastore**: Choose a datastore for VM storage.
   - **Resource Allocation**: Configure CPU and memory settings.
   - **Network**: Select the network to connect the VM.

5. **Install OS** 🖥️

   - Attach the ISO file for the OS installation in the VM settings.
   - Power on the VM and follow the OS installation wizard.

   ![Create VM](https://www.vmware.com/content/dam/digitalmarketing/vmware/en/images/vm_creation.png)

### **Download and Install OS on vSphere VM** 🛠️

#### **How to Download and Install an OS on a vSphere VM**

1. **Download the OS ISO** 📥

   - Obtain the ISO image for the desired operating system from the official source.

2. **Upload ISO to Datastore** 🗂️

   - Log in to the vSphere Web Client.
   - Navigate to the `Datastore Browser`.
   - Upload the ISO file to the desired datastore.

3. **Attach ISO to VM** 🔗

   - Edit the VM settings.
   - Go to the `CD/DVD Drive` section.
   - Select `Datastore ISO file` and choose the uploaded ISO.

4. **Power On and Install** ⚡

   - Power on the VM.
   - The VM should boot from the ISO, starting the OS installation process.
   - Follow the OS installation prompts to complete the setup.

   ![OS Installation](https://www.vmware.com/content/dam/digitalmarketing/vmware/en/images/iso_installation.png)

---
