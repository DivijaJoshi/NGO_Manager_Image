
# NGO Manager System Architecture

This repository contains a comprehensive architectural diagram and detailed explanation of the **NGO Manager**, a smart system designed to facilitate volunteer task management, event organization, idea tracking, notifications, analytics, and domain-based smart matching for non-profit organizations.

<object type="image/svg+xml" data="https://kroki.io/mermaid/svg/eNqNWG1v2zYQ_p5fIWAokABMsSbL0vTDAKeWtwDJMNRu90HwB8aibc2KZIh0Whf68SOP7y-SkwCJyHt05N09Ot5x0-H9NltMzzL-8-5dNmfHumo22ZSsq6ZiVdtQEK1qTCmfzMgPRroG19m6qutPv8xm-c30DlHWtTsihre__nathpffq5JtP13tf_gq9l27IpQqDfn17Go2NRo-3N3-Pr06oaHEDD9jSvQmrvOb2Y1RcXv_YTY5pYIenjfCdmGw0XMzc_Xc5eL3hJ513X7Xlnyc3eTWF1f57fQ6sQ3t6lx7Mm8Y9zSRjv5KSXd-Lv5eXMDEpHypmvNz-Kem8hdc1XPSvVYrUhQwytRwuTT6p9xJPJ5t52iGYQHqs-n9xRIEC0x3SiAerSB_JQ1TEni2ooeSYCURj1bwd8uqdbXCgjoK4E5Z4LTl-9YQOZBCQ8UX3LHsCbPVVjByfqSMvIBQx05CNAJE4qesOrKCxRb3ZvKh2R_YP5J5HFzAOLMTS4OUe9FaC7U1Pba4f9tuV7e4nPAYHmlFCz2R6RmL5etwjhADVeMEcr5qO76MtLZQI2W8RcFu_iQN6cCrBYwzO2GRQw7ILt9f_hHYOo4NbBgHh84Z8K4EezYP-WwMGq42hvVmJTDwJkBJUxomTg5sy9mvKTzjn7zPQx8wTsTHdlM1Bfy1UfpCNhXfT1foh4g6X_c86RFDHDm0qAXPMc03XFelJASMMzuRIARsQTogeDvalkSZBJLe2xAoUC5hwmOKM5G7IQk94QZvyItIOrG_BcICxv0tsJ87Ipwn_8HM0pNPOHM3TSH_JeTK-crOOcPs4H6yJgsVTs5KeNxuRbldJ16DMN5TDDaaE4tZHXLfCYuGlrE2vRXh5vChuHl5Pg6aK6bjMQOo-iBJoR-sR--rjm1LfARcoUd-zKTMjyUcYlIAj4kYBRHwVvL0OyCznL-Qg7ALp21wnKytjY0ZA9kFxlDebBxYSwEv-4mkynMbTSU-LRuPZ754LBRrrMvNu0pSwMRPJ8zfKnrgeeOnTGlTTLfPLe7K01Hj6w3FyhVFUXJkpsBJvLZ4VEkssGDQNAn3zEkbaXPomBxqwShOT6JMUQuqks_JsoV4tvWenhXP1Kn29DwMqK319Lx4pnGlp8Uwpz7EL2TfdowftVooJ-jS37EgVfa5bRpJG1urgq09nFJ9dF44Y4mDU6a3rosA6gQifXBE-dTp1ZHmrxjsCZzWu360lbpEyPQbQ5yxBMLKfZCAfcr2D826fYMq6ft-MFUHhs53vGmhb9ALhw2hyreBKyRPeo88EZs8U-1Hd5b4BpWxb1B3ytz4DXmeDRgCxO5drofc96ww6eEsThbKhpOqEvtJGKMIVZOOUYffg0i1wXRej2blO6JVHPbk4FLQeYrgO_1o1KDqXYmaKb1G-PGoPNFHGSSZVlwLbGIMyD7hueW1YscBncEHJzY7tHzI1zFsQIshaMDEZAYKOuaxxBBlPvkeX9lRMNRlh4k4ygbyhgC8HTR-Kb_Li4ZBdOB30P0X7zja7ph-IejUggQVlMuRv1QrL90WtL6m2tnv66O-BrNXPWAYAn4hj936PsyBOgFAjv-Qm5GQkw1Q4qNAEc33TojtlsA6ZPyILD2RYR-KvnrkukZfpgUW2H4W-e2Wp44iU-sg7zbGv2BzdMOBjnRnibwWEgW9IrIdE7JdDbLNibMm8opb5JXXyNTQyBbKiNdxKKzUkFduoYCDyCcNCu8dUHBngbzLBhSyV9wdGuI94mN7YDyF_XegTPhZhprTcCfvKEuyxoeaZVXD_bZva1HC87hV9H-Ddv01"></object>

## 📌 Overview

The **NGO Manager** centralizes multiple workflows relevant to NGOs: volunteer coordination, domain-based task assignment, notification dispatch, and impact analytics. Its architecture is modular and scalable, integrating multiple process pipelines with both admin and user-facing interfaces.

View full diagram:  
[**Live Viewer**](https://divijajoshi.github.io/NGO_Manager_Image/)  
[**Direct SVG Link** (for embedding and export)](https://kroki.io/mermaid/svg/eNqNWG1v2zYQ_p5fIWAokABMsSbL0vTDAKeWtwDJMNRu90HwB8aibc2KZIh0Whf68SOP7y-SkwCJyHt05N09Ot5x0-H9NltMzzL-8-5dNmfHumo22ZSsq6ZiVdtQEK1qTCmfzMgPRroG19m6qutPv8xm-c30DlHWtTsihre__nathpffq5JtP13tf_gq9l27IpQqDfn17Go2NRo-3N3-Pr06oaHEDD9jSvQmrvOb2Y1RcXv_YTY5pYIenjfCdmGw0XMzc_Xc5eL3hJ513X7Xlnyc3eTWF1f57fQ6sQ3t6lx7Mm8Y9zSRjv5KSXd-Lv5eXMDEpHypmvNz-Kem8hdc1XPSvVYrUhQwytRwuTT6p9xJPJ5t52iGYQHqs-n9xRIEC0x3SiAerSB_JQ1TEni2ooeSYCURj1bwd8uqdbXCgjoK4E5Z4LTl-9YQOZBCQ8UX3LHsCbPVVjByfqSMvIBQx05CNAJE4qesOrKCxRb3ZvKh2R_YP5J5HFzAOLMTS4OUe9FaC7U1Pba4f9tuV7e4nPAYHmlFCz2R6RmL5etwjhADVeMEcr5qO76MtLZQI2W8RcFu_iQN6cCrBYwzO2GRQw7ILt9f_hHYOo4NbBgHh84Z8K4EezYP-WwMGq42hvVmJTDwJkBJUxomTg5sy9mvKTzjn7zPQx8wTsTHdlM1Bfy1UfpCNhXfT1foh4g6X_c86RFDHDm0qAXPMc03XFelJASMMzuRIARsQTogeDvalkSZBJLe2xAoUC5hwmOKM5G7IQk94QZvyItIOrG_BcICxv0tsJ87Ipwn_8HM0pNPOHM3TSH_JeTK-crOOcPs4H6yJgsVTs5KeNxuRbldJ16DMN5TDDaaE4tZHXLfCYuGlrE2vRXh5vChuHl5Pg6aK6bjMQOo-iBJoR-sR--rjm1LfARcoUd-zKTMjyUcYlIAj4kYBRHwVvL0OyCznL-Qg7ALp21wnKytjY0ZA9kFxlDebBxYSwEv-4mkynMbTSU-LRuPZ754LBRrrMvNu0pSwMRPJ8zfKnrgeeOnTGlTTLfPLe7K01Hj6w3FyhVFUXJkpsBJvLZ4VEkssGDQNAn3zEkbaXPomBxqwShOT6JMUQuqks_JsoV4tvWenhXP1Kn29DwMqK319Lx4pnGlp8Uwpz7EL2TfdowftVooJ-jS37EgVfa5bRpJG1urgq09nFJ9dF44Y4mDU6a3rosA6gQifXBE-dTp1ZHmrxjsCZzWu360lbpEyPQbQ5yxBMLKfZCAfcr2D826fYMq6ft-MFUHhs53vGmhb9ALhw2hyreBKyRPeo88EZs8U-1Hd5b4BpWxb1B3ytz4DXmeDRgCxO5drofc96ww6eEsThbKhpOqEvtJGKMIVZOOUYffg0i1wXRej2blO6JVHPbk4FLQeYrgO_1o1KDqXYmaKb1G-PGoPNFHGSSZVlwLbGIMyD7hueW1YscBncEHJzY7tHzI1zFsQIshaMDEZAYKOuaxxBBlPvkeX9lRMNRlh4k4ygbyhgC8HTR-Kb_Li4ZBdOB30P0X7zja7ph-IejUggQVlMuRv1QrL90WtL6m2tnv66O-BrNXPWAYAn4hj936PsyBOgFAjv-Qm5GQkw1Q4qNAEc33TojtlsA6ZPyILD2RYR-KvnrkukZfpgUW2H4W-e2Wp44iU-sg7zbGv2BzdMOBjnRnibwWEgW9IrIdE7JdDbLNibMm8opb5JXXyNTQyBbKiNdxKKzUkFduoYCDyCcNCu8dUHBngbzLBhSyV9wdGuI94mN7YDyF_XegTPhZhprTcCfvKEuyxoeaZVXD_bZva1HC87hV9H-Ddv01)

---

## 🧠 Architecture Breakdown

### 1. **External Actors**
- **User**: Volunteers or general participants interacting with the system.
- **Admin**: NGO coordinators and system managers.
- **Email Service**: Responsible for sending email-based alerts and notifications.

### 2. **Data Stores**
- `User DB`: Stores user profiles, skills, and activity logs.
- `Task DB`: Stores task definitions, status, and assignments.
- `Event DB`: Maintains all event-related data.
- `Idea DB`: Tracks suggestions and contributions from users.
- `Notification DB`: Stores alerts, reminders, and email logs.
- `Domain DB`: Stores domain knowledge and classification info for matching.

### 3. **Core Process Blocks**

#### **Authentication Flow**
Handles login, registration, token validation, and profile management. All interactions flow through secure validation against the `User DB`.

#### **Task Management**
Includes task creation, update, assignment, and integration with a smart match system. It also interacts with the notification engine to alert users of changes.

#### **Event and Idea Management**
Users can create or participate in events and contribute ideas. These get stored, linked to notifications, and made visible to others via updates.

#### **Smart Matching System**
Matches tasks to users based on:
- **Domain Matching** (via `Domain DB`)
- **Profile Analysis** (skills from `User DB`)
- **Workload Analysis** (active tasks per user)

A scoring mechanism selects best-fit users, who are then auto-assigned or suggested.

#### **Notifications System**
Generates task updates, birthday reminders, and event alerts. Routes output both to UI and email services.

#### **Analytics Engine**
Performs ETL on user/task/event/idea data, analyzes trends, and presents insights via an admin/user-facing dashboard.

---

## 🧩 System Flow Summary

1. Users authenticate and update profiles.
2. Admins or users create tasks, events, or ideas.
3. Smart Matching engine matches users to tasks.
4. Notifications are triggered and optionally emailed.
5. Analytics engine tracks usage and outputs dashboards for impact reporting.

---

## 🔐 Copyright

This system architecture, including its design and associated visuals, is an original work protected under copyright law. Reproduction or commercial usage of the diagram without explicit permission is prohibited.

**Source Diagram:** See live: [NGO Manager Image](https://divijajoshi.github.io/NGO_Manager_Image/)  
**Raw Diagram Source:** Stored as a [Mermaid Diagram](https://mermaid.js.org/) rendered via [Kroki.io](https://kroki.io/)

**Contact:** Divija Joshi and Team
