## Part 1 : Data Migration and Processing

### GSP860 : Migrating On-premises MySQL Using a Continuous Database Migration Service Job
```
gcloud services enable datamigration.googleapis.com --quiet
gcloud services enable servicenetworking.googleapis.com --quiet
```
```
curl -O https://raw.githubusercontent.com/PerkVerse/google-cloud-arcade/refs/heads/main/2026/April%202026/Sprint2/lab1.sh
sudo chmod +x lab1.sh
./lab1.sh
```

### GSP647 : Configuring IAM Permissions with gcloud
```
export ZONE=$(gcloud compute project-info describe \
--format="value(commonInstanceMetadata.items[google-compute-default-zone])")
gcloud compute ssh centos-clean --zone=$ZONE --quiet
```
```
curl -O https://raw.githubusercontent.com/PerkVerse/google-cloud-arcade/refs/heads/main/2026/April%202026/Sprint2/lab2.sh
sudo chmod +x lab2.sh
./lab2.sh
```
```
echo -n "Enter PROJECTID2: "
read PROJECTID2
if [[ -z "$PROJECTID2" ]]; then
echo "ERROR: PROJECTID2 cannot be empty"
exit 1
fi
gcloud config set project $PROJECTID2
gcloud iam service-accounts create instance-admin-sa 
--display-name "Instance Admin SA" || true
export SA=instance-admin-sa@$PROJECTID2.iam.gserviceaccount.com
```

### GSP212 : VPC Flow Logs - Analyzing Network Traffic
```
curl -O https://raw.githubusercontent.com/PerkVerse/google-cloud-arcade/refs/heads/main/2026/April%202026/Sprint2/lab3.sh
sudo chmod +x lab3.sh
./lab3.sh
```

### GSP185 : App Dev: Storing Image and Video Files in Cloud Storage - Python
```
curl -O https://raw.githubusercontent.com/PerkVerse/google-cloud-arcade/refs/heads/main/2026/April%202026/Sprint2/lab4.sh
sudo chmod +x lab4.sh
./lab4.sh
```
