# Getting Started with Airflow

To begin working with Airflow, follow these steps:

# Cloning the Repository

Open your terminal and run the following commands:
```bash
git clone https://github.com/sastriodjamier/dibimbing-airflow.git
```

```bash
cd dibimbing-airflow
```
This command will do the following things:

- Download the repository to your local machine.
- You'll be in dibimbing-airflow repository's directory

# Setting Up the Environment

```bash
source config.sh
```
This command will do the following things:

- Create `venv` directory if not exist.
- Activate virtual environment.
- Install all pip packages defined in `requirements.txt`.


# Airflow Setup

To start Airflow, you can run the following commands:
```bash
mkdir -p ./dags ./logs ./plugins ./config ./resources
```

```bash
touch .env
echo -e 'AIRFLOW_UID=50000' > .env
```

```bash
docker compose up airflow-init
```

```bash
docker-compose up -d
```
This command will start Airflow and its dependencies in separate Docker containers, and the -d flag runs the containers in detached mode, allowing you to continue using your terminal.

# Accessing Airflow

Once Airflow is running, you can access the Airflow UI by navigating to http://localhost:8082 in your web browser.

From the Airflow UI, you can create and manage DAGs, which are used to define workflows in Airflow.