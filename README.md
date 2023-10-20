# Starting to work

To start working with Airflow you can run the following command:

Open your terminal then run the following commands:

```bash
git clone git@github.com:sastriodjamier/dibimbing-airflow.git
```

```bash
source config.sh
```

This command will do the following things:

- Create `venv` directory if not exist.
- Activate virtual environment.
- Update to latest pip.
- Install all pip packages defined in `requirements.txt`.


# Airflow Setup

To start Airflow, you can run the following commands:

```zsh
mkdir .env
echo -e "AIRFLOW_UID=$(id -u)" > .env
```

```zsh
docker build -t airflow_image .
```

This command will do the following things:
- Build an airflow image.
- Install all pip packages defined in `requirements.txt`.


```zsh
docker-compose up -d
```
This command will start Airflow and its dependencies in separate Docker containers, and the -d flag runs the containers in detached mode, allowing you to continue using your terminal.

# Accessing Airflow

Once Airflow is running, you can access the Airflow UI by navigating to http://localhost:8080 in your web browser.

From the Airflow UI, you can create and manage DAGs, which are used to define workflows in Airflow.


# Stop working

To stop working with Airflow , you can run the following commands:

```zsh
docker-compose down
deactivate
```