## Usage
### 1. Run Containers
`docker-compose up -d`

### 2. Kafka
`docker-compose exec kafka /bin/bash`

`/opt/kafka/bin/kafka-console-consumer.sh --topic quickstart-events --from-beginning --bootstrap-server localhost:9092`

### 3. Deepstream
Open another console window, and

`xhost +`

`docker-compose exec deepstream /bin/bash`

`cd /opt/nvidia/deepstream/deepstream-5.0/sources/apps/sample_apps/deepstream-occupancy-analytics`

`make`

`./deepstream-test5-analytics -c config/test5_config_file_src_infer_tlt.txt`