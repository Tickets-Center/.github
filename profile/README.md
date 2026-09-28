# 🎫 Ticket Center

> **A modern, real-time platform for managing support requests and service workflows.**

Ticket Center is an open-source platform designed to help organizations **create, manage, assign, track, and resolve requests** through a centralized system.

It connects **reporters, workers, dispatchers, and administrators** through a shared platform with real-time communication, notifications, authentication, and workflow management.

The goal is to build a **flexible, production-oriented support platform** that can adapt to different organizations and use cases.

---

## 🚀 What is Ticket Center?

Ticket Center provides a structured workflow for handling requests from creation to resolution.

```text
                        ┌─────────────────┐
                        │   Ticket Center │
                        └────────┬────────┘
                                 │
             ┌───────────────────┼───────────────────┐
             │                   │                   │
             ▼                   ▼                   ▼
          Reporter          Dispatcher            Worker
             │                   │                   │
             │ Create            │ Assign            │ Resolve
             │ request           │ request           │ request
             └───────────────────┴───────────────────┘
                                 │
                                 ▼
                              Resolved
```

A request can be created, assigned, discussed, updated, tracked, and eventually resolved while keeping its history throughout the process.

### Core capabilities

* 🎫 Request and ticket management
* 👥 Role-based access control
* 🔐 Authentication and authorization
* 📋 Assignment and workflow management
* 💬 Real-time communication
* 🔔 Real-time notifications
* 📧 Email and OTP authentication
* 🔎 Request tracking
* 📊 Analytics and reporting
* ⚡ Real-time updates
* 🐳 Containerized deployment
* 🧪 Automated testing

---

## 🌍 Designed for Different Use Cases

Ticket Center is not limited to a single industry.

The platform can be adapted for different types of support and service workflows, including:

* 💻 IT and technical support
* 🏢 Internal company requests
* 🎓 University and educational support
* 🛠️ Maintenance requests
* 📞 Customer support
* 🏥 Service requests
* 🏛️ Organizational help desks
* 🔧 Technical service management

The underlying system is designed around **requests, workflows, users, assignments, communication, and resolution**, allowing organizations to adapt it to their own needs.

---

## 🏗️ Architecture

Ticket Center is organized into independent applications so each part of the platform can evolve separately.

```text
                         Ticket Center
                              │
                ┌─────────────┴─────────────┐
                │                           │
                ▼                           ▼
        ┌───────────────┐           ┌───────────────┐
        │ React Web App │           │ Laravel API   │
        │               │◄─────────►│               │
        │   Frontend    │   REST    │    Backend    │
        └───────────────┘   API     └───────┬───────┘
                                            │
                         ┌──────────────────┼──────────────────┐
                         │                  │                  │
                         ▼                  ▼                  ▼
                     Database            Reverb             Mail
                                       Realtime             / OTP
```

Keeping the frontend and backend separate allows the platform to support additional clients in the future, such as mobile applications.

---

## 📦 Repositories

| Repository                       | Description                    | Technology                 |
| -------------------------------- | ------------------------------ | -------------------------- |
| **[Ticket-Center-api](https://github.com/Tickets-Center/Ticket-Center-api)**            | Backend API and business logic | Laravel / PHP              |
| **Ticket-Center-web**            | Web application                | React / Vite               |
| **Ticket-Center-mobile**         | Mobile application             | React Native *(planned)*   |
| **Ticket-Center-infrastructure** | Infrastructure and deployment  | Docker / Linux *(planned)* |

> More repositories may be introduced as the platform evolves.

---

## 🛠️ Technology

### Backend

* PHP
* Laravel
* REST API
* Laravel Sanctum
* Laravel Reverb
* WebSockets
* Events & Listeners
* Queues & Jobs
* Notifications
* Email / OTP
* Database migrations
* API Resources
* PHPUnit / Pest

### Frontend

* React
* Vite
* JavaScript / TypeScript
* REST API integration
* WebSocket communication
* Responsive UI

### Infrastructure

* Linux
* Docker
* Nginx
* GitHub Actions
* CI/CD
* Database management
* Logging and monitoring

---

## 👥 User Roles

Ticket Center is built around several types of users.

### 👤 Reporter

Creates requests and follows their progress.

### 🧑‍🔧 Worker

Handles assigned requests, communicates with reporters, performs the required work, and updates the request status.

### 📋 Dispatcher

Manages incoming requests and assigns them to appropriate workers.

### 🛡️ Administrator

Manages users, permissions, configuration, and the overall platform.

---

## ⚡ Real-Time Communication

Real-time functionality is an important part of Ticket Center.

The platform uses **Laravel Reverb** to provide live communication between clients and the backend.

Real-time functionality can be used for:

* New request notifications
* Assignment updates
* Status changes
* New messages
* User notifications
* Live request updates

```text
React Client
     │
     │ WebSocket
     ▼
Laravel Reverb
     │
     ▼
Laravel Application
     │
     ├── Events
     ├── Notifications
     └── Database
```

---

## 🔐 Security

Security is considered a fundamental part of the platform.

The project focuses on:

* Authentication
* Authorization
* Role-based permissions
* Request validation
* Secure password handling
* OTP verification
* API authentication
* Rate limiting
* Authorization policies
* Secure production configuration

---

## 🗺️ Roadmap

### Current

* [x] Authentication
* [x] Role-based access
* [x] Request management
* [x] REST API
* [x] React web application
* [x] Real-time communication
* [x] Notifications
* [x] OTP authentication

### In Progress

* [ ] Automated test coverage
* [ ] API documentation
* [ ] Improved analytics
* [ ] Production deployment
* [ ] Docker development environment
* [ ] CI/CD pipeline
* [ ] Improved notification system

### Planned

* [ ] Mobile application
* [ ] Push notifications
* [ ] Advanced analytics
* [ ] AI-assisted request classification
* [ ] Automatic request routing
* [ ] Knowledge base
* [ ] SLA management
* [ ] Advanced reporting
* [ ] Public API documentation

---

## 🤖 AI-Assisted Workflows

One future direction for Ticket Center is using AI to assist support workflows.

For example:

```text
New Request
     │
     ▼
┌────────────────┐
│ AI Classification │
└────────┬───────┘
         │
         ├── Category
         ├── Priority
         ├── Department
         └── Suggested Worker
                  │
                  ▼
             Request Queue
```

AI can help automate repetitive tasks while keeping important decisions under human control.

---

## 📱 Future Mobile Application

A future React Native application will extend Ticket Center to mobile devices.

Potential capabilities include:

* Push notifications
* Assigned requests
* Request details
* Status updates
* Worker notes
* Real-time chat
* Attachments
* Offline support

---

## 🤝 Contributing

Ticket Center is an open-source project and contributions are welcome.

To contribute:

1. Fork the relevant repository.
2. Create a feature branch.
3. Make your changes.
4. Add or update tests where appropriate.
5. Run the project's checks.
6. Open a pull request.

For larger changes, consider opening an issue first to discuss the proposed approach.

---

## 📚 Documentation

Each repository contains documentation specific to its responsibility.

Documentation covers areas such as:

* Architecture
* Installation
* API endpoints
* Authentication
* Database structure
* Real-time events
* Local development
* Testing
* Docker
* Deployment
* Contribution guidelines

---

## 🌱 Project Vision

Ticket Center aims to become a **flexible, extensible, and open-source platform for managing support and service workflows**.

The project is built with a focus on:

* 🧩 Modularity
* 🔐 Security
* ⚡ Real-time systems
* 🧪 Testable software
* 📡 API-first architecture
* 📈 Scalability
* 🤝 Open-source collaboration

---

## ⭐ Get Involved

Whether you want to **use the platform, explore the architecture, report an issue, suggest an improvement, or contribute code**, you're welcome to participate.

Explore the repositories and help build Ticket Center.

---

<p align="center">
  Built with ❤️ using PHP, Laravel, React, and open-source technologies.
</p>
