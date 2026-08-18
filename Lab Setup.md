# Peppermint Ticketing System Lab

## 1 Installing Docker and Peppermint

### What is Docker?

- Docker allows applications to run in lightweight, isolated **containers**.
- Useful for:
  - Avoiding dependency conflicts.
  - Consistent environments.
  - Fast testing and deployment.
  - DevOps and security labs.

### What is Peppermint?

- **Peppermint** is an open-source IT help desk and ticketing system.
- Used to:
  - Create and track tickets.
  - Assign tickets to technicians.
  - Manage users and clients.
  - Organize IT support workflows.

### Installing Docker

<img width="830" height="237" alt="image" src="https://github.com/user-attachments/assets/b3f7520b-e2d1-4213-9ac7-cfa32e854978" />

<img width="665" height="421" alt="image" src="https://github.com/user-attachments/assets/a753f75e-4bde-4601-8a5d-f24a62e9138c" />

- Installed Docker and Docker Compose on Ubuntu.
- Verified the Docker service:
  - `sudo systemctl status docker`
- Enabled Docker at startup:
  - `sudo systemctl enable docker`
- Tested the installation:
  - `sudo docker run hello-world`

### Installing Peppermint

<img width="760" height="406" alt="image" src="https://github.com/user-attachments/assets/0c0c0fa5-fb1a-40a7-85d0-3eec0163c805" />

<img width="778" height="85" alt="image" src="https://github.com/user-attachments/assets/73326282-c939-453d-b6db-91fc3b294b83" />

<img width="819" height="687" alt="image" src="https://github.com/user-attachments/assets/c08777b1-99bf-4f29-8f72-f69fc8d454a4" />

- Created a dedicated directory:
  - `mkdir peppermint`
  - `cd peppermint`
- Created the Docker Compose file:
  - `nano docker-compose.yml`
- Added the Peppermint and PostgreSQL configuration.
- Started the containers:
  - `sudo docker compose up -d`
- Verified the containers:
  - `sudo docker ps`
- Accessed Peppermint:
  - `http://localhost:3000`
- Used the default credentials to access the lab dashboard.

> **Security Note:** Default credentials should only be used in an isolated lab environment. They should be changed immediately in a real deployment.

## 2 Configuring Peppermint

- Explored the Peppermint dashboard and practiced:
  - Managing users.
  - Managing clients.
  - Creating and tracking tickets.
  - Reviewing roles and permissions.
  - Checking system activity.

### Creating Users

<img width="970" height="298" alt="image" src="https://github.com/user-attachments/assets/d9a1a77c-8c13-4a13-875c-096120b213ff" />

<img width="1068" height="569" alt="image" src="https://github.com/user-attachments/assets/bf4864f3-a8c3-40b9-aa09-7e33fd818a68" />


- Created test users to simulate an IT support environment.
- Added:
  - Name.
  - Email.
  - Password.
- Verified the accounts by logging in.

### Creating Clients

<img width="310" height="430" alt="image" src="https://github.com/user-attachments/assets/edf14a82-5ff1-41b3-acc4-1357258bec38" />

<img width="777" height="298" alt="image" src="https://github.com/user-attachments/assets/aa028f35-2a84-4a8c-ac9a-7f1ef2a45cc5" />

<img width="754" height="349" alt="image" src="https://github.com/user-attachments/assets/f635140f-e6a9-4c60-b0c0-33b4e4bde0e7" />


- Created three test clients.
- Added client information and verified the accounts.
- Tested associating clients with support tickets.

### Client Portal

<img width="339" height="395" alt="image" src="https://github.com/user-attachments/assets/d6227374-8f8c-4cfb-88e5-f4cee168c5a0" />

<img width="732" height="259" alt="image" src="https://github.com/user-attachments/assets/d6c09eb2-341d-4647-8c61-f242ee36d0a8" />

- Explored:
  - **Portal URL**
  - **Portal Register**
  - **Guest Ticket URL**
- Tested client registration and ticket submission.

### Creating Support Tickets

<img width="448" height="441" alt="image" src="https://github.com/user-attachments/assets/92568424-4a4e-4649-81eb-0c0cb1e52154" />

- Reviewed the information required for a support ticket:
  - **Name and Email** – Client contact information.
  - **Subject** – Summary of the issue.
  - **Issue Type** – Categorizes the request.
  - **Priority** – Low, Medium, High, or Urgent.
  - **Description** – Details about the issue and troubleshooting performed.

### Peppermint Features

<img width="778" height="155" alt="image" src="https://github.com/user-attachments/assets/77bb1772-8272-4c91-894d-d851af2986d1" />

<img width="792" height="132" alt="image" src="https://github.com/user-attachments/assets/1cd921af-e31e-4e82-b86d-5353d56b0bad" />

<img width="465" height="297" alt="image" src="https://github.com/user-attachments/assets/e0fe65dd-5eab-4a86-8cc5-7e81c254805d" />

<img width="752" height="179" alt="image" src="https://github.com/user-attachments/assets/a659aa10-7c38-4355-98a4-288666fe2ff8" />


- **Email Queues** – Manage ticket-related emails.
- **Webhooks** – Send ticket events to external applications.
- **SMTP Email** – Configure outgoing email notifications.
- **Authentication** – Manage user access, roles, and permissions.

## 3 Creating, Commenting, Assigning and Closing Tickets

<img width="613" height="384" alt="image" src="https://github.com/user-attachments/assets/d5a059d5-f96f-4cb2-a148-6a5f98d03736" />

<img width="758" height="495" alt="image" src="https://github.com/user-attachments/assets/1e6049c0-4c26-4f83-811c-2165d860d7b1" />

- Practiced the complete ticket workflow:
  - Creating tickets.
  - Adding comments.
  - Assigning tickets.
  - Changing priority.
  - Adding tags.
  - Closing resolved tickets.

### Ticket Management

<img width="615" height="191" alt="image" src="https://github.com/user-attachments/assets/579593be-1860-49a6-87e3-569a81273f97" />

- Created a test ticket containing:
  - **Issue Title**
  - **Name**
  - **Email**
- Added comments describing troubleshooting performed.
- Reassigned tickets to other team members.
- Changed ticket priority.
- Added tags such as:
  - **Needs Support**
  - **In Progress**
  - **Done**
- Closed the ticket after resolving the issue.

## Lab Summary

- Gained hands-on experience deploying **Docker and Peppermint**.
- Practiced using a ticketing system for:
  - User and client management.
  - Ticket creation.
  - Ticket assignment.
  - Troubleshooting documentation.
  - Ticket prioritization.
  - Ticket resolution.
