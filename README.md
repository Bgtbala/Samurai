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

Samurai includes 19–25 interlinked modules, each representing a crucial part of the manufacturing process — from job creation to dispatch.
Every model interacts with others through shared references and automated logic, ensuring consistency and traceability throughout the system.

Key Modules include:

Job Card Management

Work Order & Department Workflow

Quality Control (QC Pass / Reject / Line Damage)

Material & Inventory Management

Purchase Cycle (Indent → Order → Inward → QC → Stock)

Batch Release & FG Store

Outward Management

Alerts & Notifications via Socket

🏭 2. Intelligent Workflow System

Each Work Order flows through a customized department sequence based on the job card configuration.
At each department level:

The process time is tracked precisely — Start, Pause, Resume, Stop.

QC checks determine whether items pass, fail, or get marked as Line Damage.

Upon Batch Release, processed goods automatically progress to the next department.

When the final department completes processing, the output is transferred to the FG Store, ready for outward dispatch.

📦 3. Material & Inventory Management

Samurai’s material management system is deeply integrated with production:

Begins with BOM (Bill of Materials) selection.

Proceeds through Purchase Indent → Purchase Order → Material Inward QC → Inventory Update.

Departments consume materials directly from inventory against their assigned work orders.

After completion, leftover materials are automatically returned to inventory, maintaining real-time accuracy.

This closed-loop material flow ensures zero leakage, proper tracking, and accountability across all levels.

🔁 4. Automation & Aggregations

Mongoose Pre-save Hooks are extensively used to automate status updates, calculate process timings, and maintain relational consistency between models.

MongoDB Aggregation Pipelines optimize performance and deliver data-driven insights, even across large datasets and multiple relational lookups.

Example automation:

When a department completes its task, the next department automatically gets its batch assigned — no manual triggers required.

⚡ 5. Real-Time Socket Notifications

Using Socket.io, the system delivers instant alerts for critical operations:

🧾 Job Card Created notifications

⚠️ Low Stock Warnings

✅ Department Completion Updates

🔄 Batch Transfers

This ensures that admins, managers, and workers are always synchronized with the ongoing production flow.

🧱 6. Scalable & Secure Architecture

Built on modular MERN architecture with isolated services and shared data layers.

JWT-based authentication and role-based access control across all modules.

Deployed on AWS EC2 using Nginx reverse proxy and PM2 for production stability.

Configuration-driven design for easy scaling and department addition.

🧠 Highlights

✅ 19+ interconnected modules for seamless production flow
✅ Department-level workflow with time tracking and QC handling
✅ Automated material management and return flow
✅ Real-time socket alerts for key operations
✅ Pre-save automation and MongoDB aggregations for optimized logic
✅ Deployed on AWS for stability, scalability, and performance

🌐 Deployment

Frontend: React.js app deployed on AWS EC2 via Nginx
Backend: Node.js & Socket.io server managed by PM2
Database: MongoDB with indexed collections and aggregation pipelines
