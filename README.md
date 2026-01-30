# Appointment Scheduling Automation (n8n)

## Assignment 5 – Short Documentation

### Overview

This project implements an **automated appointment scheduling system** for **Dr. Strange (Physiotherapy Doctor)** using **n8n** as the backend automation tool and **Lovable** as the frontend UI.

The system receives appointment requests, validates business rules, checks availability, books appointments, and sends confirmations automatically.

---

### Documentation

**Website**
![ss](/img/web.png)
Free Access : https://drstrange.lovable.app/

**Workflow n8n**
![ss](/img/workflow.png)

### Input Format (API / Webhook)

```json
{
  "patient_name": "Tony Stark",
  "patient_email": "tony@stark.com",
  "appointment_date": "2026-02-02",
  "appointment_time": "09:00",
  "appointment_duration": 60
}
```

---

### Output Examples

**Success**

```json
{
  "status": "confirmed",
  "message": "Your appointment has been booked successfully."
}
```

**Failure**

```json
{
  "status": "invalid",
  "message": "Requested time is unavailable."
}
```

---

### Business Rules

- Working days: **Monday – Friday**
- Working hours: **09:00 – 17:00**
- Lunch break: **13:00 – 14:00**
- Buffer time: **30 minutes between appointments**
- No overlapping calendar events

---
