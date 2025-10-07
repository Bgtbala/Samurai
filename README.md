⚔️ Samurai

Custom Management System for Manufacturing

A fully integrated manufacturing management platform built on the MERN stack, designed to handle complex production workflows, material management, and inter-department communication.
Every module in Samurai is interconnected — ensuring seamless data flow, real-time tracking, and operational efficiency across all manufacturing stages.

🚀 Tech Stack

Frontend: React.js, Context API / Redux, Axios
Backend: Node.js, Express.js, Socket.io
Database: MongoDB (Aggregation Framework, Pre-save Hooks)
Deployment: AWS EC2, Nginx, PM2
Other Tools: JWT Authentication, Mongoose, Bcrypt

⚙️ Key Features
🧩 1. Unified Modular Architecture

Samurai includes 19–25 interlinked modules, each representing a critical component of the manufacturing cycle — from Job Card creation to final dispatch.
All models are linked through shared references and automation, ensuring end-to-end consistency and traceability.

Key Modules include:

Job Card Management

Work Order & Department Workflow

Quality Control (QC Pass / Reject / Line Damage)

Material & Inventory Management

Purchase Cycle (Indent → Order → Inward → QC → Stock)

Batch Release & FG Store

Outward Management

Alerts & Notifications via Socket

📊 2. Comprehensive Dashboard Overview

The Samurai Dashboard provides a unified view of all major operations, allowing admins and managers to monitor system performance in real time.

It includes live insights and summaries for:

Job Cards & Work Orders

Quality Reports (Pass / Reject / Damage)

Quotations & Leads

Purchase Orders & Material Flow

Departmental Progress & Alerts

This centralized dashboard ensures that decision-makers have complete visibility over production, procurement, and quality at a glance.

🏭 3. Intelligent Workflow System

Each Work Order flows through a customized department sequence based on its job card configuration.
At each stage:

Processing time is tracked precisely — Start, Pause, Resume, Stop.

QC actions handle Pass, Reject, or Line Damage.

Upon Batch Release, items automatically move to the next department.

Once all stages are complete, finished goods are transferred directly to the FG Store for dispatch.

📦 4. Material & Inventory Management

Begins with BOM (Bill of Materials) selection.

Progresses through Purchase Indent → Purchase Order → Material Inward QC → Inventory Update.

Departments pull materials directly from inventory for their assigned work orders.

Leftover materials are automatically returned to inventory, ensuring zero leakage and real-time accuracy.

This tightly controlled material cycle maintains transparency and accountability across all departments.

🔁 5. Automation & Aggregations

Mongoose Pre-save Hooks automate status updates, timestamp calculations, and model relationships.

MongoDB Aggregation Pipelines power analytics, reports, and multi-stage data transformations efficiently.

Example:

When a department completes processing, the next department’s batch assignment triggers automatically — eliminating manual intervention.

⚡ 6. Real-Time Socket Notifications

Socket.io enables instant system-wide alerts for:

🧾 Job Card Creation

⚠️ Low Stock Notifications

✅ Department Completion

🔄 Batch Transfers

This ensures every key participant stays informed and production runs without delay.

🧱 7. Scalable & Secure Architecture

Built on a modular MERN architecture with shared data layers.

JWT-based authentication and role-based access control across all routes.

Deployed on AWS EC2, served through Nginx, and managed by PM2.

Configuration-driven for easy scalability and future department additions.

🧠 Highlights

✅ 19+ interconnected modules ensuring complete production flow
✅ Department-level workflow with real-time time tracking and QC management
✅ BOM-driven purchase and material lifecycle with automatic inventory sync
✅ Centralized dashboard for production, quality, and procurement overview
✅ Automated backend logic using pre-saves and aggregations
✅ Real-time alerts powered by Socket.io
✅ AWS-deployed, scalable, and fault-tolerant architecture

🌐 Deployment

Frontend: React.js app deployed on AWS EC2 via Nginx
Backend: Node.js + Socket.io server managed by PM2
Database: MongoDB with indexed collections and aggregation pipelines

📸 Dashboard Preview
<p align="center"> <span style="display:inline-block; text-align:center; width:60%;"> <strong>⚔️ Samurai Dashboard</strong><br/> <img src="https://github.com/Bgtbala/Samurai/blob/main/samuraiScreenshots/dashboard.png?raw=true" alt="Samurai Dashboard" width="100%"/> </span> </p>
