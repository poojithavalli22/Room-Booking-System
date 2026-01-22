# Room Booking System – ServiceNow

## 📌 Project Overview
The Room Booking System is a ServiceNow-based application that allows users to request rooms by selecting date, time, and room details. The system prevents double-bookings, validates inputs, and automatically sends confirmation emails, ensuring efficient and reliable room scheduling.

---

## 🎯 Objectives
- Simplify room reservation requests using ServiceNow
- Prevent scheduling conflicts and invalid bookings
- Automate booking confirmations
- Improve overall user experience

---

## ✨ Features
- Submit room booking requests with date, time, room, and purpose
- Automatically assigns booking to the logged-in user
- Prevents double-bookings using Business Rules
- Sends email confirmation on successful booking
- Tracks booking status (Confirmed / Cancelled)
- Centralized booking records list

---

## 🧠 Concepts Used
- Custom Tables (`u_booking`, `u_room`)
- Service Catalog
- Record Producer
- Business Rules
- Email Notifications
- Update Sets

---

## ⚙️ Technical Implementation

### Step 1: Create Custom Tables
- **u_room** – Stores room details
- **u_booking** – Stores booking information

### Step 2: Service Catalog & Record Producer
- Created a Record Producer for room booking requests
- Captured booking details through catalog variables

### Step 3: Record Producer Script
- Mapped catalog variables to table fields
- Auto-filled the logged-in user as the requester

### Step 4: Business Rules
- Prevented overlapping bookings for the same room
- Blocked bookings with past dates or invalid time ranges

### Step 5: Notifications
- Configured email notifications for booking confirmation
- Prevented notifications for cancelled bookings

---

## 🧪 Testing

### Positive Test Cases
- Booking created with valid date, time, and room
- Logged-in user auto-populated
- Email confirmation sent successfully

### Negative Test Cases
- Overlapping bookings blocked
- Past date bookings prevented
- Mandatory fields enforced

### Edge Cases
- Start time greater than end time blocked
- Cancelled bookings do not trigger notifications

---

## 🚀 Future Enhancements
- Approval workflow for restricted rooms
- Calendar view using Service Portal
- Seat-level booking support
- Dashboard for booking analytics

---

## 🛠️ Platform
- **ServiceNow Developer Instance**

---

## 👤 Author
- **Your Name**
