# Kafka Producer and Consumer Scripts

This repository includes two new scripts designed to emulate Facebook posts from users and process that data using Apache Kafka. Below, you'll find instructions to set up and run the producer and consumer scripts, as well as how to start the necessary services in a WSL (Windows Subsystem for Linux) environment.

## Running the Producer and Consumer Scripts

### Activate the Python Virtual Environment

```shell

py -m venv .venv
.venv\Scripts\Activate
py -m pip install -r requirements.txt


```

### Start Producer and Consumer 

.venv\Scripts\activate
py -m producers.kafka_producer_moss

.venv\Scripts\activate
py -m consumers.kafka_consumer_moss


### Start WSL Terminal

Terminal 1

PS C:\Users\nolan> wsl
moss@InspironNolan:~$ cd ~/kafka
moss@InspironNolan:~/kafka$ bin/zookeeper-server-start.sh config/zookeeper.properties

Terminal 2

PS C:\Users\nolan> wsl
moss@InspironNolan:/mnt/c/Users/nolan$ cd ~/kafka
moss@InspironNolan:~/kafka$ bin/kafka-server-start.sh config/server.properties








# buzzline-02-case

Streaming data is often too big for any one machine. 
A streaming platform helps organize our pipelines.

A common pattern for managing streaming pipelines is publish-subscribe, similar to how Twitter operates:

- Producers publish streaming information.
- Consumers subscribe to specific "topics" to process, analyze, and generate alerts based on detected conditions.

In this project, we use Apache Kafka, a popular, open-source streaming platform.
We write producers that send data to topics and consumers that read from topics.

> Kafka needs space - it's big. We'll use the Windows Subsystem for Linux on Windows machines. 

## Task 1. Install and Start Kafka (using WSL if Windows)

Before starting, ensure you have completed the setup tasks in <https://github.com/denisecase/buzzline-01-case> first. 
Python 3.11 is required. 

In this task, we will download, install, configure, and start a local Kafka service. 

1. Install Windows Subsystem for Linux (Windows machines only)
2. Install Kafka Streaming Platform
3. Start the Zookeeper service (leave the terminal open).
4. Start the Kafka service (leave the terminal open).

For detailed instructions, see:

- [SETUP-KAFKA](docs/SETUP-KAFKA.md) (all machines)


## Task 2. Copy This Example Project & Rename

Copy/fork this project into your GitHub account
and create your own version of this project to run and experiment with. 
Name it `buzzline-02-yourname` where yourname is something unique to you.
Follow the instructions in [FORK-THIS-REPO.md](https://github.com/denisecase/buzzline-01-case/blob/main/docs/FORK-THIS-REPO.md)).
    

## Task 3. Manage Local Project Virtual Environment

Follow the instructions in [MANAGE-VENV.md](https://github.com/denisecase/buzzline-01-case/blob/main/docs/MANAGE-VENV.md) to:
1. Create your .venv
2. Activate .venv
3. Install the required dependencies using requirements.txt.

## Task 4. Start a Kafka Producer

Producers generate streaming data for our topics.

In VS Code, open a terminal.
Use the commands below to activate .venv, and start the producer. 

Windows:
```shell
.venv\Scripts\activate
py -m producers.kafka_producer_case
```

Mac/Linux:
```zsh
source .venv/bin/activate
python3 -m producers.kafka_producer_case
```

## Task 5. Start a Kafka Consumer

Consumers process data from topics or logs in real time.

In VS Code, open a NEW terminal in your root project folder. 
Use the commands below to activate .venv, and start the consumer. 

Windows:
```shell
.venv\Scripts\activate
py -m consumers.kafka_consumer_case
```

Mac/Linux:
```zsh
source .venv/bin/activate
python3 -m consumers.kafka_consumer_case
```

## Later Work Sessions
When resuming work on this project:
1. Open the folder in VS Code. 
2. Start the Zookeeper service.
3. Start the Kafka service.
4. Activate your local project virtual environment (.env).

## Save Space
To save disk space, you can delete the .venv folder when not actively working on this project.
You can always recreate it, activate it, and reinstall the necessary packages later. 
Managing Python virtual environments is a valuable skill. 

## License
This project is licensed under the MIT License as an example project. 
You are encouraged to fork, copy, explore, and modify the code as you like. 
See the [LICENSE](LICENSE.txt) file for more.


