# SOC Azure Active Directory RBAC Permissions Lab
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>


In this lab, I configured and observed different role-based access control (RBAC) permissions within Azure Active Directory (AAD) at the tenant, subscription, and resource group levels. I created users with specific roles—Tenant-Level Global Reader, Subscription-Level Reader, and Resource Group Contributor—and tested their permissions by logging in with their respective accounts. This hands-on project demonstrates my ability to manage and audit role-based permissions, ensuring proper access control within an enterprise Azure environment.




<h2>Environments and Technologies Used</h2>

- Active Directory Domain Services
  

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1 - Configure and Observe Tenant-Level Global Reader
- Step 2 - Configure and Observer Subscription Reader
- Step 3 - Configure and Observe Resource Group Contributor (like an admin)


<h2>Deployment and Configuration Steps</h2>

- Configure and Observe Tenant-Level Global Reader
- Create a user within Azure Active Directory (AAD) (username: globalreaderjohn)
- Assign Tenant-Level Global Reader
- In a new browser/incognito, log in as globalreaderjohn and observe result of being a Tenant Level “Global Reader”
- Close browser/incognito when satisfied

  ![Screenshot 2024-10-08 175011](https://github.com/user-attachments/assets/567baa73-a2af-4538-9516-0769cfe9f0ca)
  ![Screenshot 2024-10-08 175336](https://github.com/user-attachments/assets/cfecd7fe-7944-41ec-aab3-2996c922e811)
  ![Screenshot 2024-10-08 175804](https://github.com/user-attachments/assets/7e457e86-1861-4485-ac5e-3d39ae8af629)
  - Here I can't see subscriptions because I'm a Global reader at the tenant level
  ![Screenshot 2024-10-08 180156](https://github.com/user-attachments/assets/84497d47-0cde-408c-a7f5-2990e6200f05)

- Configure and Observer Subscription Reader
- Back in main browser, create another user within AAD  (username: subreaderjane)
- Assign Subscription-Level Reader 
- In a new browser/incognito, log in as subreaderjane and observe result of being a Subscription Level “Global Reader”
- Close browser/incognito when satisfied
![Screenshot 2024-10-08 180829](https://github.com/user-attachments/assets/87b82903-fdf3-45ac-a608-d7e100b45208)
![Screenshot 2024-10-08 181550](https://github.com/user-attachments/assets/ca756538-2135-4b06-830d-4b05348d5024)
- By this user having Subscription Level Access as a Global Reader, here tehy can view the subscription
![Screenshot 2024-10-08 181745](https://github.com/user-attachments/assets/1d5068b7-a104-4e1e-80c8-74f91435b545)

- Configure and Observe Resource Group Contributor (like an admin)
- Back in main browser, create another user within AAD  (username: rgcontributordave)
- Create a new resource group called “Permissions-Tester”
- Assign Resource Group-level Contributor
- For our resource group (RG-Cyber-Lab), assign Contributor Permissions
- In a new browser/incognito, log in as rgcontributordave and observe result of being a Subscription Level Reader
- Observe the result of being a Resource Group Level Contributor
![Screenshot 2024-10-08 182430](https://github.com/user-attachments/assets/1e6dcee2-a3c9-4b25-bbd7-28f5746e4791)
![Screenshot 2024-10-08 182742](https://github.com/user-attachments/assets/17c6c4f4-d74c-4dd2-807c-d5a0bccd08cb)
![Screenshot 2024-10-08 183009](https://github.com/user-attachments/assets/df4a4e65-5fe4-4231-8827-935a4888f218)
![Screenshot 2024-10-08 183233](https://github.com/user-attachments/assets/964b17b7-fa2e-422e-8b32-07addc065170)
- As a Resource Group Level Contributor, This is the only resource group this user has control of because this is the one that was assigned to him in the previous step.
![Screenshot 2024-10-08 183723](https://github.com/user-attachments/assets/c4d7ce19-085e-4f16-9cb2-953bbae3cdb6)
















