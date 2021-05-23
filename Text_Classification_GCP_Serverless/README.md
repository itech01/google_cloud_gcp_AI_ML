
To deploy the model on serverless infrastructure (Cloud Run), execute the below commands
------------------------------------------------------------------------------------------

Building the container image - gcloud builds submit --tag gcr.io/<your GCP project>/complaintsapi .

List the image - gcloud builds list --filter complaints

Checking logs of built image - gcloud builds log <container id from list command above>

Deploy the container on google cloud run - gcloud run deploy complaintsapi --image gcr.io/<your GCP project>/complaintsapi --platform managed --memory 1G
  
