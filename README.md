<h1>Local DNS Cache Exercise</h1>
This tutorial outlines how Local DNS Cache works.<br />

<h2>Environments and Technologies Used</h2>

**Technologies and Servies**
- Oracle VM VirtualBox
- Active Directory Domain Services

**Environment/Operating System**
- Windows Server 2022
- Windows 10

<h2>High-Level Deployment and Configuration Steps</h2>

**Step 1: Change A-Record’s Address**
- Log into DC-1 as an admin (mydomain\jane.admin).
- Change mainframe’s address to 8.8.8.8
<p>
  <img src="https://github.com/AllanMontalvo/Local-DNS-Cache-Exercise/assets/135927674/c828d531-f2b3-4d2f-9b15-5911b78d58b9" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

**Step 2: Verify Change**
- Log into Client-1.
- Open cmd prompt.
- Type "ping  mainframe" in cmd prompt.
- Still pings to old address (10.1.10.2).
<p>
  <img src="https://github.com/AllanMontalvo/Local-DNS-Cache-Exercise/assets/135927674/61a381e2-4d88-4b71-b3a5-0ad4a845dc9d" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

**Step 3: Observe Local DNS Cache**
- In cmd prompt on Client-1, type “ipconfig/displaydns”.
- Observe the local DNS cache.
<p>
  <img src="https://github.com/AllanMontalvo/Local-DNS-Cache-Exercise/assets/135927674/b4d09f9a-f3e7-4a13-8c35-549aa210f919" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

**Step 4: Clear DNS Cache**
- Open cmd prompt as an admin on Client-1.
- Type “ipconfig/flushdns”.
<p>
  <img src="https://github.com/AllanMontalvo/Local-DNS-Cache-Exercise/assets/135927674/8d3147b4-33f0-4287-8dec-756313d14567" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

**Step 5: Verify Updated A-Record Address**
- In Client-1, type "ping mainframe" on cmd prompt.
- Observe the new address of mainframe.
<p>
  <img src="https://github.com/AllanMontalvo/Local-DNS-Cache-Exercise/assets/135927674/99feb19a-90c3-42c4-a974-be479d274317" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h2>Final Notes</h2>

