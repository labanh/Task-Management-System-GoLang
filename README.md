
# Task Management System / 任务管理系统

## Project Overview / 项目概述

This project is a **Task Management System** built with Go, designed to help users create, manage, and query tasks with support for multi-user concurrency, data persistence, and a RESTful API. The project progresses from basic task management operations to more advanced functionalities, showcasing Go’s core syntax, data structures, and concurrent programming capabilities.

本项目是使用Go语言开发的**任务管理系统**，旨在帮助用户创建、管理和查询任务，支持多用户并发、数据持久化和RESTful API。项目从基础的任务管理操作逐步扩展到更高级的功能，展示了Go语言的核心语法、数据结构和并发编程能力。

---

## Features / 功能特点

- **Task Management (CRUD)**: Create, delete, update, and query tasks.
- **User Management**: Add user registration, login, and authentication.
- **Concurrency Support**: Allows concurrent operations on tasks with safe synchronization.
- **Data Persistence**: Saves tasks and user data in a JSON file.
- **RESTful API**: Provides a RESTful API for external access.
- **Scheduled Backups**: Supports scheduled data backups.

- **任务管理（CRUD）**：创建、删除、更新和查询任务。
- **用户管理**：支持用户注册、登录和身份验证。
- **并发支持**：允许并发操作任务，并确保线程安全。
- **数据持久化**：使用JSON文件保存任务和用户数据。
- **RESTful API**：提供RESTful API以便外部访问。
- **定时备份**：支持定时备份数据。

---

## Project Structure / 项目结构

```plaintext
├── main.go                  # Entry point / 程序入口
├── models/                  # Data models / 数据模型
│   ├── task.go              # Task model / 任务模型
│   └── user.go              # User model / 用户模型
├── handlers/                # HTTP handlers / HTTP处理器
│   ├── taskHandler.go       # Task API endpoints / 任务API端点
│   └── userHandler.go       # User API endpoints / 用户API端点
├── services/                # Core services / 核心服务
│   ├── taskService.go       # Task management service / 任务管理服务
│   └── userService.go       # User management service / 用户管理服务
├── utils/                   # Utility functions / 工具函数
│   ├── jsonUtil.go          # JSON read/write utilities / JSON读写工具
│   └── authUtil.go          # Authentication utilities / 认证工具
└── data/                    # Data files / 数据文件
    ├── tasks.json           # Task data file / 任务数据文件
    └── users.json           # User data file / 用户数据文件
```

---

## Setup and Usage / 设置和使用

1. **Clone the repository**  
   ```bash
   git clone https://github.com/yourusername/task-management-system.git
   cd task-management-system
   ```

2. **Install Dependencies**  
   Ensure Go is installed on your system. Check the [official Go documentation](https://golang.org/doc/install) for installation steps.

3. **Run the Application**  
   ```bash
   go run main.go
   ```

4. **Access API**  
   The application exposes several API endpoints for task management. Here’s an example of creating a new task:
   ```bash
   curl -X POST -d '{"title":"New Task","description":"Task Description"}' http://localhost:8080/tasks
   ```

1. **克隆仓库**  
   ```bash
   git clone https://github.com/yourusername/task-management-system.git
   cd task-management-system
   ```

2. **安装依赖**  
   确保系统已安装Go语言环境。安装步骤参考[Go官方文档](https://golang.org/doc/install)。

3. **运行程序**  
   ```bash
   go run main.go
   ```

4. **访问API**  
   应用程序提供多个API端点用于任务管理。以下是创建新任务的示例：
   ```bash
   curl -X POST -d '{"title":"New Task","description":"Task Description"}' http://localhost:8080/tasks
   ```

---

## Contributing / 参与贡献

Feel free to submit issues or pull requests for new features, optimizations, or bug fixes.

欢迎提交问题、贡献新功能、优化或修复Bug的拉取请求。

---

## License / 许可证

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

本项目使用MIT许可证。详情请参见 [LICENSE](LICENSE) 文件。
