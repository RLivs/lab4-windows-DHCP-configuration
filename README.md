# DHCP Server Configuration Lab (Windows Server 2022)

This lab demonstrates the full process of configuring a DHCP server on Windows Server 2022 and testing automatic IP address assignment on a client machine.

---

## Environment

- **Server OS:** Windows Server 2022  
- **Client OS:** Windows 10 (domain-joined)  
- **Domain:** `test.local`  
- **IP Range:** `192.168.50.100 – 192.168.50.200`  
- **Default Gateway:** `192.168.50.1`  
- **DNS Server:** `192.168.50.1`

---

## Steps and Screenshots

| No. | Description                                                                 | Screenshot |
|-----|------------------------------------------------------------------------------|------------|
| 1   | DHCP role installed and visible in Server Manager                           | ![](screenshots/01_DHCP_Manager_ServerVisible.png) |
| 2   | Server network adapter set to Internal network                              | ![](screenshots/02_NetworkSettings_Server_Internal.png) |
| 3   | Client network adapter set to Internal as well                              | ![](screenshots/03_NetworkSettings_Client_Internal.png) |
| 4   | Starting the New Scope Wizard                                               | ![](screenshots/04_NewScope_Start.png) |
| 5   | Entering a name for the DHCP scope                                          | ![](screenshots/05_Scope_Name.png) |
| 6   | Specifying the IP address range for the scope                               | ![](screenshots/06_Scope_IP_Range.png) |
| 7   | Setting the lease duration                                                  | ![](screenshots/07_Lease_Duration.png) |
| 8   | Adding the default gateway                                                  | ![](screenshots/08_Default_Gateway.png) |
| 9   | Specifying DNS server IP address                                            | ![](screenshots/09_DNS_Settings.png) |
|10   | Scope successfully created and visible in DHCP console                      | ![](screenshots/10_Scope_Created_Overview.png) |
|11   | Client IPv4 settings set to obtain IP address automatically                 | ![](screenshots/11_Client_IPv4_Automatic.png) |
|12   | DHCP service is running on the server                                       | ![](screenshots/12_Dhcp_Service_Running.png) |
|13   | Client successfully receives IP address from DHCP server                    | ![](screenshots/13_DHCP_successful_ip_assignment_client.png) |
|14   | DHCP server authorized in Active Directory                                  | ![](screenshots/14_DHCP_Authorization_Successful.png) |
|15   | DHCP service restarted after successful authorization                       | ![](screenshots/15_DHCP_Service_Restart_After_Authorization.png) |
|16   | DHCP server now authorized and running properly                             | ![](screenshots/16_DHCP_Authorized_and_Running.png) |
|17   | Client confirmed to be configured for auto IP via DHCP                      | ![](screenshots/17_Client_IP_auto_obtain.png) |
|18   | Final confirmation of successful IP lease from server to client             | ![](screenshots/18_DHCP_successful_IP_assignment.png) |


---

## ✅ Result

DHCP server was successfully installed, configured, authorized in Active Directory, and tested with a client device.

---

## 💡 What I Learned

- How to install and configure the DHCP role on Windows Server 2022  
- How to create and configure a DHCP scope with custom IP range, gateway, and DNS  
- The process of authorizing a DHCP server in Active Directory  
- Troubleshooting client connectivity and verifying successful IP address lease  
- The importance of internal network setup for testing DHCP functionality in a virtualized environment  
- Using PowerShell and GUI tools together for administrative tasks

---

**📁 All screenshots are stored in the `/screenshots` folder.**
