# Medical-IoT-Devices-Threat-Detection-using-Deep-Learning

## Dataset

Download the "CIC IoMT dataset 2024" dataset in CSV format from [here](https://www.unb.ca/cic/datasets/iomt-dataset-2024.html).

After downloading, extract and place the CSV files in the appropriate directories (`data/train/` and `data/test/`) as detailed below.  

### Directory Setup

Within the `data/` directory, create `train/` and `test/` folders to hold the CSV files for training and testing, respectively.

### Training Data (data/train)
The following files should be placed in `data/train` (51 items):
- ARP_Spoofing_train.pcap.csv
- Benign_train.pcap.csv
- MQTT-DDoS-Connect_Flood_train.pcap.csv
- MQTT-DDoS-Publish_Flood_train.pcap.csv
- MQTT-DoS-Connect_Flood_train.pcap.csv
- MQTT-DoS-Publish_Flood_train.pcap.csv
- MQTT-Malformed_Data_train.pcap.csv
- Recon-OS_Scan_train.pcap.csv
- Recon-Ping_Sweep_train.pcap.csv
- Recon-Port_Scan_train.pcap.csv
- Recon-VulScan_train.pcap.csv
- TCP_IP-DDoS-ICMP1_train.pcap.csv
- TCP_IP-DDoS-ICMP2_train.pcap.csv
- TCP_IP-DDoS-ICMP3_train.pcap.csv
- TCP_IP-DDoS-ICMP4_train.pcap.csv
- TCP_IP-DDoS-ICMP5_train.pcap.csv
- TCP_IP-DDoS-ICMP6_train.pcap.csv
- TCP_IP-DDoS-ICMP7_train.pcap.csv
- TCP_IP-DDoS-ICMP8_train.pcap.csv
- TCP_IP-DDoS-SYN1_train.pcap.csv
- TCP_IP-DDoS-SYN2_train.pcap.csv
- TCP_IP-DDoS-SYN3_train.pcap.csv
- TCP_IP-DDoS-SYN4_train.pcap.csv
- TCP_IP-DDoS-TCP1_train.pcap.csv
- TCP_IP-DDoS-TCP2_train.pcap.csv
- TCP_IP-DDoS-TCP3_train.pcap.csv
- TCP_IP-DDoS-TCP4_train.pcap.csv
- TCP_IP-DDoS-UDP1_train.pcap.csv
- TCP_IP-DDoS-UDP2_train.pcap.csv
- TCP_IP-DDoS-UDP3_train.pcap.csv
- TCP_IP-DDoS-UDP4_train.pcap.csv
- TCP_IP-DDoS-UDP5_train.pcap.csv
- TCP_IP-DDoS-UDP6_train.pcap.csv
- TCP_IP-DDoS-UDP7_train.pcap.csv
- TCP_IP-DDoS-UDP8_train.pcap.csv
- TCP_IP-DoS-ICMP1_train.pcap.csv
- TCP_IP-DoS-ICMP2_train.pcap.csv
- TCP_IP-DoS-ICMP3_train.pcap.csv
- TCP_IP-DoS-ICMP4_train.pcap.csv
- TCP_IP-DoS-SYN1_train.pcap.csv
- TCP_IP-DoS-SYN2_train.pcap.csv
- TCP_IP-DoS-SYN3_train.pcap.csv
- TCP_IP-DoS-SYN4_train.pcap.csv
- TCP_IP-DoS-TCP1_train.pcap.csv
- TCP_IP-DoS-TCP2_train.pcap.csv
- TCP_IP-DoS-TCP3_train.pcap.csv
- TCP_IP-DoS-TCP4_train.pcap.csv
- TCP_IP-DoS-UDP1_train.pcap.csv
- TCP_IP-DoS-UDP2_train.pcap.csv
- TCP_IP-DoS-UDP3_train.pcap.csv
- TCP_IP-DoS-UDP4_train.pcap.csv

### Testing Data (data/test)
The following files should be placed in `data/test`(21 items):
- ARP_Spoofing_test.pcap.csv
- Benign_test.pcap.csv
- MQTT-DDoS-Connect_Flood_test.pcap.csv
- MQTT-DDoS-Publish_Flood_test.pcap.csv
- MQTT-DoS-Connect_Flood_test.pcap.csv
- MQTT-DoS-Publish_Flood_test.pcap.csv
- MQTT-Malformed_Data_test.pcap.csv
- Recon-OS_Scan_test.pcap.csv
- Recon-Ping_Sweep_test.pcap.csv
- Recon-Port_Scan_test.pcap.csv
- Recon-VulScan_test.pcap.csv
- TCP_IP-DDoS-ICMP1_test.pcap.csv
- TCP_IP-DDoS-ICMP2_test.pcap.csv
- TCP_IP-DDoS-SYN_test.pcap.csv
- TCP_IP-DDoS-TCP_test.pcap.csv
- TCP_IP-DDoS-UDP1_test.pcap.csv
- TCP_IP-DDoS-UDP2_test.pcap.csv
- TCP_IP-DoS-ICMP_test.pcap.csv
- TCP_IP-DoS-SYN_test.pcap.csv
- TCP_IP-DoS-TCP_test.pcap.csv
- TCP_IP-DoS-UDP_test.pcap.csv
  
### Notes

Please ensure that the CSV files follow the specified directory structure to prevent data loading errors.

Follow the model execution path to convert the data files to .parquet files or we can access the converted dataset from the below link. 

The purpose of dataset conversion is to avoid CPU crashing issues and to make the model to work efficiently at Google Collab.

### Other ways to fetch Dataset:

Use this below link to access the .parquet files directly by skipping the file convertion step.

https://drive.google.com/drive/folders/1e2H5lgDKGrgPTc_Sr-MpZblv7ZwxeBMV?usp=drive_link


------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------
## **Project Overview**

This repository includes the code and setup instructions for implementing our proposed Bi-LSTM, RNN and Logistic Regression intrusion detection model for IoMT systems. The model performs multi-class classification on network traffic to distinguish between 19 attack types and benign traffic, based on the CICIoMT2024 dataset.



### Proposed system Architecture.
![Bi-LSTM Model](https://drive.google.com/uc?export=view&id=1ZIBsZeqs7Q9v4W2QHLNTcDWNJAqV5CBB)

Bi-LSTM Model Architecture

## Getting Started

### 1. Prerequisites

- **Python 3.7+**
- **Required Libraries:** Install dependencies by running the first cell of each notebook.


### 2. Data Preparation

**Dataset:**  
Download the "CIC IoMT dataset 2024" dataset in CSV format from [here](https://www.unb.ca/cic/datasets/iomt-dataset-2024.html)(details in README_DATA.md).
After downloading, extract and place the CSV files in the appropriate directories (`data/train/` and `data/test/`).

Then convert those files by using the code at "AI_and_Sus_Final---->File_Comversion--->File_Convert_to_parquet".

or use the below drive link to access the converted file directly.

https://drive.google.com/drive/folders/1e2H5lgDKGrgPTc_Sr-MpZblv7ZwxeBMV?usp=drive_link

### 3. Data Preprocessing

* To begin training we need to preprocess the data to convert the shape of them and also to make the model run on paticular classification task, to achive that we need to perform the data preprocessing. 

*Navigate to the path "AI_and_Sus_Final---->Models_and_Result--->Preprocessing code". 

*Based on the CLass requirement run the code.

### 4. Training and Evaluation

* There three types of classification proposed in our model and the code for Bi-LSTM, RNN and Logistic regression code files were saved under each Class folder.

* For accessing the models navigatie to "AI_and_Sus_Final---->Models_and_Result---->Class_2----->Model".(Based on our choose the model).

* For other classes also do the same by navigating to the respective class names such Class_6 or Class_19.

* For Compressed model navigate to the path AI_and_Sus_Final---->Models_and_Result---->Class_19----->Model----->Compressed Models

* For Evaluating the results navigate to the path for fetching the result notebook "Same as followed for Class.... ---->Model------>Result". To analye the results we need to feed the saved .json files for evaluating. For those files refer Saved model to fetch google drive link.

* For Evaluating the results of the Compressed model navigate to the path for fetching the result notebook "Same as followed for compressed model....----->Result_Compressed".


### 5. Saved models

To get more info on the saved model and also the code navigate to the below google drive link.

https://drive.google.com/drive/folders/1HhAceYOGYz9L2nwyM748IitFAPEaPnqc?usp=sharing