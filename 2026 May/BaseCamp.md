## GSP004 : Creating a Persistent Disk

```
curl -O https://raw.githubusercontent.com/PerkVerse/google-cloud-arcade/refs/heads/main/2026/May%202026/BaseCamp/lab1.sh
sudo chmod +x lab1.sh 
./lab1.sh 
```

## The Basics of Google Cloud Compute: Challenge Lab 

```
export ZONE=
```

```
curl -O https://raw.githubusercontent.com/PerkVerse/google-cloud-arcade/refs/heads/main/2026/May%202026/BaseCamp/lab3.sh
sudo chmod +x lab3.sh
./lab3.sh 
```
```
sudo apt update
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
EOF_END
```
```
gcloud compute scp prepare_disk.sh my-instance:/tmp --zone=$ZONE --quiet

gcloud compute ssh my-instance --zone=$ZONE --quiet --command="sudo bash /tmp/prepare_disk.sh"
```

## Entity and Sentiment Analysis with the Natural Language API 

```
export GOOGLE_CLOUD_PROJECT=$(gcloud config get-value core/project)
```

```
gcloud iam service-accounts create my-natlang-sa \
  --display-name "my natural language service account"

gcloud iam service-accounts keys create ~/key.json \
  --iam-account my-natlang-sa@${GOOGLE_CLOUD_PROJECT}.iam.gserviceaccount.com
  ```
```
export GOOGLE_APPLICATION_CREDENTIALS="$HOME/key.json"
```
```
echo "GOOGLE_CLOUD_PROJECT=$GOOGLE_CLOUD_PROJECT"
echo "GOOGLE_APPLICATION_CREDENTIALS=$GOOGLE_APPLICATION_CREDENTIALS"
```
```
gcloud ml language analyze-entities --content="Michelangelo Caravaggio, Italian painter, is known for 'The Calling of Saint Matthew'." > result.json
```

## Speech-to-Text API: Qwik Start

```
export API_KEY=
```

```
curl -O https://raw.githubusercontent.com/PerkVerse/google-cloud-arcade/refs/heads/main/2026/May%202026/BaseCamp/lab8.sh
sudo chmod +x lab8.sh 
./lab8.sh 
```
