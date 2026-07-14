# 🚀 Edge AI Orchestrator

### Enterprise Edge AI Deployment Platform

[![GitHub stars](https://img.shields.io/github/stars/vishakha2121/edge-ai-orchestrator)](https://github.com/vishakha2121/edge-ai-orchestrator/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/vishakha2121/edge-ai-orchestrator)](https://github.com/vishakha2121/edge-ai-orchestrator/network)
[![GitHub issues](https://img.shields.io/github/issues/vishakha2121/edge-ai-orchestrator)](https://github.com/vishakha2121/edge-ai-orchestrator/issues)
[![License](https://img.shields.io/github/license/vishakha2121/edge-ai-orchestrator)](https://github.com/vishakha2121/edge-ai-orchestrator/blob/main/LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

---

## 📖 Overview

**Edge AI Orchestrator** is a comprehensive platform for deploying, monitoring, and managing machine learning models across edge devices including drones, IoT sensors, surveillance cameras, and mobile devices. Built with **FastAPI** and **React**, it provides centralized monitoring, real-time analytics, and AI-powered optimization using Google's **Gemini API**.

### 🎯 Key Features

- 🔄 **Seamless ML Model Deployment** across multiple edge devices
- 📊 **Real-time Performance Monitoring** and analytics
- 🤖 **AI-Powered Insights** via Google Gemini API
- 🎯 **ONNX & TensorRT** model format support
- 🖥️ **Beautiful Dashboard** with dark/light themes
- 📱 **Multi-Device Support**: Drones, IoT, Cameras, Mobile
- ⚡ **CPU-Based Simulation** (No GPU required)
- 🔒 **Enterprise-Grade Security** with JWT authentication
- 📈 **Comprehensive Analytics** and reporting
- 🔔 **Smart Alert System** with real-time notifications
- 🌐 **WebSocket Support** for live updates
- 🐳 **Docker Containerization** for easy deployment

---

## 🏗️ Architecture

### Technology Stack

#### Backend
| Technology | Purpose |
|------------|---------|
| **FastAPI** | REST API framework |
| **Python 3.10+** | Programming language |
| **PostgreSQL** | Primary database |
| **SQLAlchemy** | ORM framework |
| **Redis** | Caching & session storage |
| **Celery** | Task queue for background jobs |
| **ONNX Runtime** | Model inference |
| **TensorRT (CPU)** | Model optimization (simulated) |
| **Google Gemini** | AI intelligence & insights |
| **JWT** | Authentication & authorization |
| **WebSocket** | Real-time communication |
| **Pytest** | Testing framework |
| **Alembic** | Database migrations |

#### Frontend
| Technology | Purpose |
|------------|---------|
| **React 18** | UI framework |
| **Vite** | Build tool |
| **Tailwind CSS** | Utility-first styling |
| **Material-UI** | Component library |
| **Redux Toolkit** | State management |
| **React Router** | Navigation |
| **Recharts** | Data visualization |
| **Socket.io** | WebSocket client |
| **Axios** | HTTP client |
| **React Hook Form** | Form handling |
| **Zod** | Schema validation |
| **Framer Motion** | Animations |

#### DevOps & Infrastructure
| Technology | Purpose |
|------------|---------|
| **Docker** | Containerization |
| **Docker Compose** | Multi-container orchestration |
| **GitHub Actions** | CI/CD pipeline |
| **Nginx** | Reverse proxy |
| **Prometheus** | Metrics collection |
| **Grafana** | Visualization |

---

## 📁 Project Structure

---

## 🚀 Quick Start

### Prerequisites

| Requirement | Version |
|------------|---------|
| Python | 3.10 or higher |
| Node.js | 18 or higher |
| npm | 9 or higher |
| Docker | 20.10 or higher (optional) |
| PostgreSQL | 15 or higher |
| Git | 2.30 or higher |

### Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/vishakha2121/edge-ai-orchestrator.git
cd edge-ai-orchestrator

# Create and activate virtual environment
cd backend
python -m venv venv

# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate

# Install dependencies
pip install --upgrade pip
pip install -r requirements.txt

# Copy environment variables
cp .env.example .env

# Edit .env with your configurations
# IMPORTANT: Add your Gemini API key
# GEMINI_API_KEY=your_actual_gemini_api_key_here

# Run database migrations
alembic upgrade head

# Start the backend server
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

# Open a new terminal
cd frontend

# Install dependencies
npm install

# Copy environment variables
cp .env.example .env

# Start the development server
npm run dev