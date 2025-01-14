**Network Design for a Four-Story Startup Office**

Scenario Overview
Design a scalable network infrastructure for a four-story building to accommodate a growing startup. The requirements include:

Separate floors for key departments.
Two small conference rooms and one large presentation room.
A 70 m² canteen.
Dedicated manager offices for each department.
Scalability for a 30% workforce expansion in the future.
Floor Plan and Department Allocation
**Floor 1**
Reception: 3 staff.
Human Resource Department: 12 staff + 1 manager + 2 admin officers.
Accounting Department: 12 staff + 1 manager + 2 admin officers.
Presentation Room: Large enough for product demos.
Canteen: 70 m².
**Floor 2**
Conference Rooms: 2 rooms, 30 m² each.
Sales Department: 20 staff + 1 manager + 2 admin officers.
Training Room 1: 18 computers.
**Floor 3**
Design Department: 30 staff + 1 manager + 2 admin officers.
Training Room 2: 18 computers.
**Floor 4**
Software Development Department: 25 staff + 1 manager + 2 admin officers.
Technical Support Department: 15 staff + 1 manager + 2 admin officers.
View Floor Layout

**Project Requirements**
1. Physical Layout
Use Cisco Packet Tracer to design the physical network layout.
Incorporate structured cabling and both wired and wireless networks.
2. Logical Layout (IP Addressing)
Subnet the provided network: 150.128.0.0/23.
Assign static IPs to all devices.
Example Addressing Table:
Device	Interface	IP Address	Subnet Mask	Default Gateway
Router R1	Gig0/0/0	192.168.1.1	255.255.255.0	-
PCs 1-24	Fa0/1	192.168.1.2-25	255.255.255.0	192.168.1.1
3. VLAN Configuration
Configure VLANs for department communication:
Design ↔ Software Development: Allowed communication.
Sales ↔ Accounting: Allowed communication.
Design/Software Development ↔ Sales/Accounting: No communication.
VLAN Table:
VLAN ID	Name	Interface
5	Software Development Dept	Fa0/6 - Fa0/10
10	Design Department	Fa0/18 - Fa0/24
15	Accounting Department	Fa0/11 - Fa0/17
20	Sales Department	Fa0/2 - Fa0/5
4. Network Security
Configure network devices with:
VTY Password: COMMUNICATIONS.
Console Password: COMPUTERNETWORK.
Secret Password: RMIT.
Encrypt all passwords and set appropriate hostnames.
Create a custom Welcome Message for each device.
5. Company Web Page
Host a webpage on the company server:
URL: http://cosc2174.webpage.com.
Content:
html
Copy code
<html>
<body>
<h1>Welcome to Semester 2-2024 COSC2174 - Data Communication and Net-centric Computing Web Page</h1>
<table>
  <tr><td>Accounting Department</td></tr>
  <tr><td>Sales Department</td></tr>
  <tr><td>Human Resource Department</td></tr>
  <tr><td>Technical Support Department</td></tr>
  <tr><td>Software Development Department</td></tr>
  <tr><td>Design Department</td></tr>
  <tr><td>Training Rooms</td></tr>
</table>
</body>
</html>
6. Internet of Things (IoT) Applications
Implement IoT solutions for:

Intruder alert.
Fire alert.
Energy conservation.
Choose relevant categories from Packet Tracer: Home, Smart City, Industrial, or Power Grid.
Simulation Tools
Use the Multiuser Function in Packet Tracer to connect the four floors.
Simulate the entire network infrastructure, ensuring VLANs and IP address assignments function as designed.
