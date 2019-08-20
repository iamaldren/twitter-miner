# Twitter Miner

Mines tweets using Twitter API, and groups data based on Sentiment Polarity (Positive/Negative/Neutral)

The idea and code came from [Real Python Blog](https://realpython.com/twitter-sentiment-python-docker-elasticsearch-kibana/#kibana-visualizer)

## Background

I was reading an article on what are some Python projects that I can do to kickstart my learning, and I saw the blog about the Twitter Sentiment Analysis and I got interested.

I made some minor changes, like instead of hardcoding the Tweet keyword, I am passing it via System argument instead.

## Pre-requisites
- Python
- Kibana
- Elasticsearch
- Docker

## Setup

### Elasticsearch and Kibana

1. Run the docker command below on your terminal
    ```sh
    docker run -d -p 9200:9200 -p 5601:5601 nshou/elasticsearch-kibana
    ```
    > Simple and lightweight docker image for previewing Elasticsearch and Kibana from `nshou`.

2. Verify Elasticsearch is running via http://localhost:9200

3. Verify Kibana is running via http://localhost:5601

### Twitter Developer App

1. You must create a developer account for Twitter, and get the necessary Access Token for oAuth validation when invoking the Twitter APIs.

2. Once Twitter Developer App is create, update the file `config.py` with the necessary details.

### Run Python Program

1. Clone the repository

2. Run the program by executing below in terminal
    ```sh
    python sentiment.py MCU
    ```
    > You can put whatever keyword you want to use in place of MCU
    
 ## Access the mined data
 
 Please read the blog about it in [Real Python Blog](https://realpython.com/twitter-sentiment-python-docker-elasticsearch-kibana/#kibana-visualizer)
