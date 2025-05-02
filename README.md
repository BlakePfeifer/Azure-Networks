# Azure-Networks
# How to Create a Virtual Network (VNet) on Microsoft Azure

## Introduction
In this tutorial, we will walk through how to create a Virtual Network (VNet) in Microsoft Azure and why VNets are essential.

A **Virtual Network (VNet)** in Azure is a logically isolated network you create to securely connect Azure resources like virtual machines, databases, and applications. It is similar to a traditional network you would operate in your own data center but with added benefits like scalability, high availability, and security.



## Environments and Technologies Used
- **Microsoft Azure Portal**: For deploying and managing the virtual network.
- **Azure Resource Manager (ARM)**: The backend system that manages network resources.
- **Web Browser**: (e.g., Microsoft Edge, Google Chrome, Firefox).
- **Windows 11** *(Optional)*: If you are working from a Windows 11 environment.

<h2>Operating Systems Used </h2>

- Windows 11 (23H2)
---

## Prerequisites
- A Microsoft account (free to create if you don't have one).
- An Azure subscription (you can start with the **Azure Free Account** which gives you free credits).
- Access to the Azure Portal: [https://portal.azure.com](https://portal.azure.com)

---

## Steps to Create a Virtual Network

### 1. Sign in to the Azure Portal
- Open [https://portal.azure.com](https://portal.azure.com).
- Log in with your Microsoft account credentials.

![image](https://github.com/user-attachments/assets/1f1b2efa-5e70-44e0-8421-d0b952185058)


---

### 2. Navigate to Virtual Networks
- On the left-hand menu, click **"Virtual networks"**.
- Or use the search bar at the top to find **"Virtual networks"**.

![image](https://github.com/user-attachments/assets/5e5a2563-8a6f-4ba8-a819-731d5165153e)


---

### 3. Start Creating a New Virtual Network
- Click the **"+ Create"** button at the top.

![image](https://github.com/user-attachments/assets/fa671dee-a346-4b34-b75c-210ec5bede93)


---

### 4. Configure Basic Settings
- **Subscription**: Select your Azure subscription.
- **Resource Group**: Select an existing Resource Group or create a new one.
- **Name**: Enter a name for your Virtual Network (example: `MyFirstVNet`).
- **Region**: Choose the region where you want your VNet resources to be hosted (example: `East US`).

![image](https://github.com/user-attachments/assets/befb47f1-f654-4022-aa4d-55a2ae75869d)


---

### 5. Configure IP Addressing
- In the **IP Addresses** tab:
  - Define the **Address Space** (example: `10.0.0.0/16`).
  - Configure at least one **Subnet** (example: `10.0.1.0/24`).

*Subnets divide your VNet into smaller address spaces that you can assign to resources.*

![image](https://github.com/user-attachments/assets/e1e28119-4dd8-4189-84b0-fb237cabe802)


---

### 6. Configure Security and Advanced Options (Optional)
- You can configure **DDoS Protection**, **Firewall**, or **Service Endpoints** if needed, but for a basic setup, you can leave defaults.

![image](https://github.com/user-attachments/assets/ca60d540-ac4b-4aa4-b77f-4a90b9036701)



---

### 7. Review and Create
- Click **Review + Create**.
- Verify the settings are correct.
- Click **Create** to deploy the Virtual Network.

![image](https://github.com/user-attachments/assets/cbf2d301-4f1c-42a7-a021-a5b9e009ccfa)

---

### 8. View Your Virtual Network
- Once deployment finishes, go to **Virtual Networks** and click on your new VNet to view details.
- Here you can manage subnets, security settings, and connected resources.

![image](https://github.com/user-attachments/assets/63f4e042-b1bb-439f-8717-3bb034c96756)


---

## Summary
In this tutorial, you successfully created a Virtual Network (VNet) in Azure by:
- Configuring network basics like address space and subnets.
- Deploying the network to a specific Azure region.
- Preparing a secure environment for hosting cloud resources.

---

## Common Mistakes and Tips

Here are some important things to watch out for when creating Virtual Networks:

- ✅ **Plan Address Spaces Carefully**: Make sure your address space doesn't overlap with other VNets if you plan to connect them later.
- ✅ **Use Clear Naming Conventions**: Use names that clearly describe the network (like `Prod-VNet-EastUS`).
- ✅ **Create Subnets**: Always define subnets instead of leaving your VNet flat — it’s important for organization and security.
- ✅ **Understand Region Limitations**: Resources in a VNet must generally be in the same region unless using special services.
- ✅ **Security Settings**: By default, all VMs in a VNet can talk to each other. You may want to configure **Network Security Groups (NSGs)** later to restrict traffic.
- ✅ **Cost Awareness**: Creating a VNet itself doesn't cost money, but services deployed inside the VNet (like VMs) can generate charges.

> **Important Reminder**:  
> Virtual Networks are the foundation of all networking in Azure — setting them up properly at the start makes scaling and securing your cloud infrastructure much easier!

---
