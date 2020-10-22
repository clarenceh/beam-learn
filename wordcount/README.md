# Apache Beam - Wordcount

## Install

    go install github.com/clarenceh/beam-learn/wordcount

## Run locally

    wordcount --input kinglear.txt --output counts

## Run on GCP Cloud Dataflow

    wordcount --input gs://dataflow-samples/shakespeare/kinglear.txt \
            --output gs://clarence-myek-dev/counts \
            --runner dataflow \
            --project myek-dev \
            --region us-central1 \
            --temp_location gs://clarence-myek-dev/tmp/ \
            --staging_location gs://clarence-myek-dev/binaries/ \
            --worker_harness_container_image=apache/beam_go_sdk:latest
