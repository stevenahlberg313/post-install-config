<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This project will demonstrate and document how to setup osTicket post-installation in an example setting. 
<p>This project is a continuation of my osTicket Installation project. As such this project has been conducted on the same Virtual Machine.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Enterprise multi-session, version 22H2 - x64 Gen2

<h2>Post-Install Configuration Objectives</h2>

- Establish "Roles".
  - "Roles" determine the permissions an Agent has within their "Department(s)".
- Establish "Departments".
  - "Departments" organize and route tickets, facilitating their retrieval and care by the appropriate support agents.
- Establish "Teams"
  - "Teams" allow support agents from different departments to collaborate on and resolve tickets.
- Authorize anyone the right to create and submit a ticket.
- Establish "Agents"
  - "Agents" are staff members with the necessary permissions to manage and resolve tickets. 
- Establish "Users".
  - "Users" are individuals who submit tickets for resolution. 
- Establish an SLA plan.
  - SLA (Service Level Agreements) is a timeframe within which tickets of different priorities are expected to be closed.
- Establish "Help Topics"
  - "Help Topics" are groupings of common issues that users can use to categorize their requests, facilitating how tickets are routed and handled. 

<h2>Configuration Steps</h2>  

<p> To begin, I navigated to http://localhost/osTicket/scp/login.php , and logged in with the Admin account I had made in the previous project. 
<p>
<img <img width="2546" height="524" alt="Screenshot 2026-08-20 085946" src="https://github.com/user-attachments/assets/e0c14403-b54c-427f-9133-3acb520ae526" />

</p>
<p>
Upon login, osTicket sends me to the "Agent Panel". To make the desired changes, I switched over to the "Admin Panel" by clicking "Admin Panel" in the top right of the window.
</p>
<br />

<p>
<img <img width="1752" height="417" alt="Screenshot 2026-08-20 090251" src="https://github.com/user-attachments/assets/458fc189-e5f8-4d24-ba47-ca5a2c2d3a48" />


</p>
<p>
The simplest indicator that I was in the "Admin Panel" was the "Admin Panel" button  had changed to "Agent Panel".
</p>
<br />

<p>
<img <img width="956" height="140" alt="Screenshot 2026-08-20 091657" src="https://github.com/user-attachments/assets/51813bc1-81ce-4cd1-931c-9404f6bdc91d" />

</p>
<p>
The first objective I had was to establish a "Role". To do so, from the Admin panel, I clicked "Agents", "Roles", and "Add New Role"
</p>
<br />

<p>
<img <img width="956" height="381" alt="Screenshot 2026-08-20 093050" src="https://github.com/user-attachments/assets/804bf161-ce25-4faf-94dd-2489d5cdfdb0" />

</p>
<p>
In "Name" I put "Supreme Admin". As for permissions, I granted all permissions.
</p>
<br />

<p>
<img width="958" height="571" alt="Screenshot 2026-08-20 094545" src="https://github.com/user-attachments/assets/44f705c8-ea47-424d-a7d3-c1e7f2386657" />
<img width="955" height="706" alt="Screenshot 2026-08-20 094736" src="https://github.com/user-attachments/assets/8c18efd8-7456-4815-bc2b-b25c4a2e03de" />
<img width="962" height="558" alt="Screenshot 2026-08-20 095211" src="https://github.com/user-attachments/assets/50aa3c65-f50f-4495-bc6e-6281a13fb1b0" />
<img width="954" height="404" alt="Screenshot 2026-08-20 095224" src="https://github.com/user-attachments/assets/8f77509e-7cbd-4593-872e-f6941ca4c20c" />


</p>
<p>
The new "Supreme Admin" role had been successfully established.
</p>
<br />

<p>
<img width="957" height="453" alt="Screenshot 2026-08-20 094852" src="https://github.com/user-attachments/assets/58ce5275-8e78-44b4-8a2e-bb265f915887" />

</p>
<p>
The Second objective was to establish a "Department". To do so, from the Admin panel, I clicked "Agents", "Departments", and "Add New Departments". 
</p>
<br />

<p>
<img width="955" height="326" alt="Screenshot 2026-08-20 095623" src="https://github.com/user-attachments/assets/88c71d35-5163-43f0-9522-b2c45a3334cc" />

</p>
<p>
I then filled in the desired information necessary for this new department, and clicked "Create Dept".
</p>
<br />

<p>
<img width="959" height="1131" alt="Screenshot 2026-08-20 101000" src="https://github.com/user-attachments/assets/b354b9c9-2c21-44f8-bc79-caeb011bc3fd" />

</p>
<p>
The new department SysAdmins had been successfully added.
</p>
<br />

<p>
<img width="959" height="394" alt="Screenshot 2026-08-20 101030" src="https://github.com/user-attachments/assets/bb20a911-6764-4a86-9df1-0d158ebcee04" />

</p>
<p>
The third objective was to establish a "Team". To do so, from the Admin panel, I clicked "Agents", "Teams", and "Add New Team".
</p>
<br />

<p>
<img width="960" height="300" alt="Screenshot 2026-08-20 101948" src="https://github.com/user-attachments/assets/920b5807-9e2d-41c2-8074-c6553934a03f" />
</p>
<p>
I named the team "Online Banking" and clicked "Create Team".
</p>
<br />

<p>
<img width="958" height="682" alt="Screenshot 2026-08-20 103122" src="https://github.com/user-attachments/assets/41c96f65-4e7c-4db5-bcb1-2526142f7349" />
</p>
<p>
Back on the "Teams" page, we could see that the "Online Banking" team had been successfully established.
</p>
<br />

<p>
<img width="961" height="329" alt="Screenshot 2026-08-20 103530" src="https://github.com/user-attachments/assets/de09cfd5-6bab-4fd8-bb9d-251502522310" />
</p>
<p>
The fourth objective was to allow anyone to create tickets. To accomplish that, from the Admin panel, I clicked settings and users. I had to ensure, under "Authentication Settings", that "Require registration and login to create tickets" remained unchecked.
</p>
<br />

<p>
<img width="958" height="684" alt="Screenshot 2026-08-20 104122" src="https://github.com/user-attachments/assets/f7c3b6d4-0768-4053-8444-58d33c277e7e" />
</p>
<p>
The fifth objective was to establish two Agents. To do so, from the Admin panel, I clicked "Agents" and "Add New Agent".
</p>
<br />

<p>
<img width="956" height="342" alt="Screenshot 2026-08-20 105343" src="https://github.com/user-attachments/assets/c4db35ab-66d4-4e17-94f0-f936ea39fe5d" />
</p>
<p>
I filled out the necessary information and passwords for both of my new agents.
  - The first agent will be Theresa. She is in the SysAdmin department, her role will be Supreme Admin, and is on the Online Banking team. Clicking "Create" finished this agents creation.
</p>
<br />

<p>
<img width="956" height="956" alt="Screenshot 2026-08-20 110554" src="https://github.com/user-attachments/assets/26484be3-6e2c-4462-8d7d-bb68c1e2345c" />
<img width="957" height="951" alt="image" src="https://github.com/user-attachments/assets/5a163e90-3400-436f-b99b-51d1fbcf04fe" />
<img width="957" height="539" alt="Screenshot 2026-08-20 110638" src="https://github.com/user-attachments/assets/febc772e-0e79-4e1f-8d1e-e938c8b2bd0e" />
<img width="956" height="425" alt="Screenshot 2026-08-20 110701" src="https://github.com/user-attachments/assets/9a3a6a52-a5a7-4c2c-bea9-ea4a098580ac" />
</p>
<p>
  - Next came Valerie. She is in the Support department and her role will be "View Only" She will not be on any teams for now. Clicking "Create" finished this agents creation.
</p>
<br />

<p>
<img width="965" height="956" alt="Screenshot 2026-08-20 111748" src="https://github.com/user-attachments/assets/6627d6d2-21ca-4dd5-8481-8694a05d0516" />
<img width="957" height="951" alt="image" src="https://github.com/user-attachments/assets/85416230-d6aa-4dfe-bdd8-ea090ab6354a" />
<img width="961" height="536" alt="Screenshot 2026-08-20 111808" src="https://github.com/user-attachments/assets/e39e79b8-a7d5-4d2f-8273-bcb7779e2e03" />
</p>
<p>
Both of my new agents had been successfully established.
</p>
<br />

<p>
<img width="959" height="398" alt="Screenshot 2026-08-20 111837" src="https://github.com/user-attachments/assets/2c1b7556-1e29-48c1-99e1-4fbfa8e13b62" />

</p>
<p>
The sixth objective was to fabricate two example users. To begin their creation, from the Agent panel, I clicked "Users", and "Add New".
</p>
<br />

<p>
<img width="952" height="344" alt="Screenshot 2026-08-20 113433" src="https://github.com/user-attachments/assets/5deae1f6-cf32-4794-8e75-7a6bdc7ffba0" />
</p>
<p>
First was Barbie Doll.
</p>
<br />

<p>
<img width="639" height="399" alt="Screenshot 2026-08-20 114246" src="https://github.com/user-attachments/assets/ce39bef6-c86a-45f0-b5cd-e8d0a1d754ee" />
</p>
<p>
Second was Ken Doll.
</p>
<br />

<p>
<img width="646" height="389" alt="Screenshot 2026-08-20 114347" src="https://github.com/user-attachments/assets/4480d67a-38eb-4364-851a-e2ee81c7916e" />
</p>
<p>
Both were successfully fabricated.
</p>
<br />

<p>
<img width="960" height="398" alt="Screenshot 2026-08-20 114407" src="https://github.com/user-attachments/assets/0eaaaa35-524c-465d-b507-41b406eb1f97" />
</p>
<p>
The seventh objective was to establish three SLA plans. To do that, from the Admin panel, I clicked "Manage", "SLA", and "Create New SLA".
</p>
<br />

<p>
<img width="959" height="299" alt="Screenshot 2026-08-20 115530" src="https://github.com/user-attachments/assets/c78a65f6-3ceb-4f59-8ba9-2525a74cd685" />
</p>
<p>
The three SLA plans I needed to establish were:
  - Sev-A Grace Period: 1 hour, Schedule: 24/7.
  - Sev-B Grace Period: 4 hours, Schedule: 24/7.
  - Sev-C Grace Period: 8 hours, Business Hours/ 9:00 am- 5:00 pm.
</p>
<br />

<p>
<img width="960" height="662" alt="Screenshot 2026-08-20 120847" src="https://github.com/user-attachments/assets/73b658ed-3c66-4837-96fe-00addc77e43b" />
<img width="957" height="658" alt="Screenshot 2026-08-20 120957" src="https://github.com/user-attachments/assets/aa18bcbc-7cf6-4970-8159-62c21d7da181" />
<img width="962" height="662" alt="Screenshot 2026-08-20 121115" src="https://github.com/user-attachments/assets/e8ec0bcd-5bf0-4864-ab89-97cce5dd6d7d" />
</p>
<p>
All three SLA plans were successfully established.
</p>
<br />

<p>
<img width="960" height="418" alt="Screenshot 2026-08-20 121129" src="https://github.com/user-attachments/assets/2373e22e-9fab-4734-90c4-4179706c0015" />
</p>
<p>
The eighth objective was to establish five Help Topics. To accomplish this, from the Admin panel, I clicked "Manage", Help Topics", and "Create New Help Topic".
</p>
<br />

<p>
<img width="957" height="418" alt="Screenshot 2026-08-20 121816" src="https://github.com/user-attachments/assets/2d68cb3f-ff8b-442f-bdc4-745fbc80b85a" />
</p>
<p>
The five Help Topics I needed to establish were:
  - Business Critical Outage (Parent Topic: Report a Problem)
  - Personal Computer Issues (Parent Topic: Report a Problem)
  - Equipment Request (Parent Topic: General Inquiry)
  - Password Reset (Parent Topic: Report a Problem)
  - Other (Parent Topic: General Inquiry)
</p>
<br />

<p>
<img width="959" height="632" alt="Screenshot 2026-08-20 122405" src="https://github.com/user-attachments/assets/87c8bd72-799e-4a9e-8d48-bbd4948b6101" />
<img width="958" height="635" alt="Screenshot 2026-08-20 122647" src="https://github.com/user-attachments/assets/ef9a3438-be9d-46ac-9f91-3cac28036b68" />
<img width="959" height="634" alt="Screenshot 2026-08-20 122844" src="https://github.com/user-attachments/assets/1e826223-71f2-4346-b478-2d33a2c5a4dd" />
<img width="957" height="626" alt="Screenshot 2026-08-20 123122" src="https://github.com/user-attachments/assets/efb4aa51-00b3-4a97-b90d-f70fd272cd11" />
<img width="959" height="632" alt="Screenshot 2026-08-20 123236" src="https://github.com/user-attachments/assets/69f055fe-9a31-42da-8e9c-01809b65d8cb" />
</p>
<p>
All five chosen Help Topics were successfully established. 
</p>
<br />

<p>
<img width="955" height="646" alt="Screenshot 2026-08-20 123406" src="https://github.com/user-attachments/assets/750d5e61-de64-44d0-8aa9-998e45b921a1" />

