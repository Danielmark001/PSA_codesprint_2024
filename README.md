
<p align="center">
  <img width="620" src="public/ecoport-logo.png" alt="Ecoport Logo">
</p>

# EcoPort :Nature:

## About :blue_book:
Ecoport is a synergistic eco-friendly transformation portal that leverages the power of data, AI, and IoT Systems.

**1. Ecoport :leaf:** <br>
<video controls src="public/Ecoport Demo _ Dashboard - Google Chrome 2024-10-12 20-52-52 (online-video-cutter.com).mp4" title="<img width="400" src="public/portbot.gif" alt="PortBot GIF">"></video> <br>
A real-time monitoring and AI-driven solution designed to optimize energy consumption and reduce carbon 
emissions in port operations. By integrating IoT sensors, machine learning models, and an interactive dashboard, this system provides actionable insights into 
energy usage and recommends strategies to reduce environmental impact while maintaining operational efficiency. <br>

**2. Smart Energy Monitoring System :bulb:** <br>
<video controls src="public/Ecoport_ Dashboards - Google Chrome 2024-10-12 20-54-31 (online-video-cutter.com).mp4" title="Title"></video> <br>
A smart energy management system that uses AI to forecast energy consumption and optimize energy usage in real-time. It has three key features: temperature & humidity monitoring, fuel monitoring, and fleet tracking. <br> 


## Installation

### Prerequisites
- **Python 3.9+**
- **Node.js 14+**
- **Docker** (for local containerization)
- **PostgreSQL** (for database setup)
- **Kubernetes Engine API**
- **Google Container Registry API**
- **Google Cloud SDK**
- **Kubectl**

### Clone the Repository
```bash
git clone https://github.com/your-repo/port-energy-management-system.git
cd port-energy-management-system
```

### Environment Variables
Create a `.env` file in the root directory to store your environment variables:
```bash
DATABASE_URL=your_database_url
SECRET_KEY=your_secret_key
```


## Backend Setup

### Install Python Dependencies
Navigate to the `/backend` directory and install the required dependencies:
```bash
cd backend
pip install -r requirements.txt
```

### Initialize the Database
Ensure your database is running and initialize it:
```bash
python database/init_db.py
```

### Run the Backend Server
```bash
python api/app.py
```
The API should now be running at `http://localhost:5000`.



## Frontend Setup

### Install Frontend Dependencies
Navigate to the `/frontend` directory and install the required dependencies:
```bash
cd frontend
npm install
```

### Run the Frontend
```bash
npm start
```
The frontend should now be running at `http://localhost:3000`.

---

## AI Model

### Training the AI Model
Ensure your historical energy data is stored in the `/data` folder. Train the AI model with the following command:
```bash
python ai_model/train.py
```

### Running Predictions
You can use the trained model to predict future energy usage:
```bash
python ai_model/predict.py
```

---

## Deployment

### Docker Compose (Local Deployment)
You can run the entire system (backend, frontend, and database) locally using Docker Compose:
```bash
docker-compose up --build
```

### Cloud Deployment
For cloud deployment, use Kubernetes or Google Cloud Run. Follow the instructions in the `infrastructure/` folder:
- **Kubernetes Deployment:** Use the `k8s-deployment.yaml` for Kubernetes.
- **Google Cloud Run:** Use the `cloud_run_deploy.sh` script for Google Cloud deployment.



## Usage

### Real-Time Monitoring
1. Access the dashboard via `http://localhost:3000`.
2. View real-time energy consumption and emissions data.
3. Receive AI-driven recommendations for optimizing energy usage.

### Forecasting Emissions
- Use the AI model to forecast future energy usage and carbon emissions.
- Visualize predicted trends in the dashboard.

### AI Recommendations
- Access energy-saving recommendations in the dashboard.
- Apply suggestions to reduce energy consumption during peak operational hours.




## **Tech Stack**

#### **Backend**
- **Python 3.9+**
- **FastAPI** 
- **PostgreSQL** 
- **SQLAlchemy** 
- **Redis & Celery**
- **Docker**
- **Google Kubernetes Engine (GKE)**

#### **Frontend**
- **React**
- **Plotly.js**
- **npm & Webpack**
- **Tailwind CSS**
- **Docker**

#### **Machine Learning**
- **TensorFlow/Keras**
- **Scikit-learn, Pandas, NumPy**

#### **Cloud & Deployment**
- **Google Cloud Platform (GCP)**
- **Kubernetes Secrets**




