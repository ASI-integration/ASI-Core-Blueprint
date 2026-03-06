структура системы.
Слои, принципы, ограничения.

---------------

\# ASI — System Architecture



Version: 1.0  

Last update: 2026-03-03



---



\# SYSTEM OVERVIEW



ASI is a modular platform designed to automate property management, booking operations, financial tracking, and communication workflows.



The system consists of three major layers:



1\. Backend (core logic)

2\. Frontend (user interface)

3\. Automation \& AI layer



---



\# SYSTEM LAYERS



\## 1. BACKEND



Technology stack:

\- NestJS

\- Prisma ORM

\- PostgreSQL

\- Docker



Responsibilities:

\- business logic

\- data management

\- API endpoints

\- system automation triggers



Core backend modules:



Property Module  

Manages properties and units



Owner Module  

Manages owners and permissions



Booking Module  

Handles reservations and availability



Communication Module  

Messaging and webhook events



Finance Module  

Revenue tracking and financial flows



Automation Module  

Event-based automation engine



---



\## 2. FRONTEND



Technology stack:

\- Next.js

\- React

\- TailwindCSS



Responsibilities:

\- dashboards

\- object management

\- booking interface

\- system monitoring



Main areas:



Dashboard  

System overview



Objects / Units  

Property and unit management



Bookings  

Reservation management



Finance  

Revenue analytics



Communication  

Messaging interface



---



\## 3. AUTOMATION LAYER



Automation connects system events with actions.



Examples:



Booking created  

→ trigger communication



Payment received  

→ update finance ledger



Owner added  

→ send onboarding workflow



Automation components:



Event system  

Task queue  

Background workers



---



\## 4. AI LAYER



Future layer integrating AI systems.



Planned integrations:



Antigravity  

AI coding and development automation



Gemini  

AI task orchestration



AI Agents  

Automated decision-making workflows



---



\# DATA FLOW



Example booking flow:



User creates booking  

→ Frontend sends API request  

→ Backend Booking Module processes  

→ Database updated via Prisma  

→ Automation triggers communication  

→ Communication Module sends message



---



\# DATABASE



Database management handled via:



Prisma ORM



Primary entities:



Property  

Unit  

Booking  

Owner  

Transaction  

Message



Schema reference:



schema.prisma



---



\# CORE DESIGN PRINCIPLES



Modular architecture  

Each module independent



Event-driven automation  

System reacts to events



Scalable infrastructure  

Designed for multi-property systems



Automation-first mindset  

Manual tasks minimized



---



\# FUTURE EXPANSION



Planned expansions:



Dynamic pricing engine  

OTA integrations  

Smart automation workflows  

AI-driven system management

