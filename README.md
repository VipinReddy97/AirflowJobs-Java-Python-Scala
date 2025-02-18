# 🚀 Apache Airflow Supercharged with Java, Scala, and Python Spark Jobs  

This project enables **seamless orchestration of Spark jobs** written in **Python, Scala, and Java** using **Apache Airflow** in a **Dockerized environment**.  
The DAG is designed to **automate Spark job submission**, ensuring efficient and reliable **data processing pipelines** run on a scheduled basis.

---

## 🏗️ **Project Overview**

The **`sparking_flow`** DAG executes the following tasks:

- **🟢 `start`** → Logs `"Jobs started"` in Airflow.
- **🐍 `python_job`** → Submits a **Python Spark job**.
- **🔥 `scala_job`** → Submits a **Scala Spark job**.
- **☕ `java_job`** → Submits a **Java Spark job**.
- **✅ `end`** → Logs `"Jobs completed successfully"`.

### ✨ **Why is Airflow ‘On Steroids’ Here?**
🚀 **Runs Spark jobs in multiple languages** (**Python, Scala, Java**).  
🔄 **Parallel execution** of tasks to **speed up workflows**.  
📊 **Automated scheduling, monitoring, and logging** with Airflow.  
🐳 **Runs everything inside Docker**, making deployment seamless.  

---

## ⚠️ **Why Python Works Out-of-the-Box but Java & Scala Need Setup?**
✅ **Docker includes a Python environment by default**, so Python Spark jobs **run effortlessly**.  
❌ **Java & Scala require compilation** before submission, which means we need:
   - **Java Development Kit (JDK)** to compile and run Java jobs.
   - **Scala Build Tool (SBT)** to package Scala jobs into `.jar` files.  
🛠 **This setup ensures all Spark jobs are packaged correctly before execution.**  

---

## 📌 **Prerequisites**
Before running this project, ensure you have the following installed:

✅ **Docker & Docker Compose**  
✅ **Apache Airflow Docker image** (or a custom setup)  
✅ **Apache Spark Docker image** (or a pre-configured Spark installation)  
✅ **Mounted Docker volumes** for Airflow DAGs, logs, and Spark jobs  

---

---

## 🛠️ Docker Setup

To run this project using Docker, follow these steps:

1. Clone this repository to your local machine.
2. Navigate to the directory containing the `docker-compose.yml` file.
3. Build and run the containers using Docker Compose:

   ```bash
   docker-compose up -d --build
   ```

This command will start the necessary services defined in your docker-compose.yml, such as Airflow webserver, scheduler, Spark master, and worker containers
