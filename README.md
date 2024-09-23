# Linux Crontab Automation Guide

This guide demonstrates how to use crontab in Linux for automating tasks, including logging current time and disk usage information.

## Table of Contents
1. [Logging Current Time](#1-logging-current-time)
2. [Logging Current Time with Python](#2-logging-current-time-with-python)
3. [Logging Disk Usage with Python](#3-logging-disk-usage-with-python)

## 1. Logging Current Time

### Step 1: Check Current Directory
```bash
pwd
```


### Step 2: Configure Crontab
```bash
crontab -e
```
![Current Directory](https://github.com/user-attachments/assets/ff973957-a8c5-44b3-affc-f1db2da5a54c)
Add the following line:
```
* * * * * date > /home/username/aaa.log
```
![Crontab Configuration](https://github.com/user-attachments/assets/2e0f03a8-c778-4d8a-8aa5-4b0f4bfaaecd)

### Step 3: Restart Cron Service
```bash
sudo service cron restart
sudo service cron status
```
![image](https://github.com/user-attachments/assets/aecb7406-dc38-4127-812d-19338391d424)

### Step 4 : Results
![Cron Service Restart](https://github.com/user-attachments/assets/148efdf4-80fc-4663-a42e-bde59ba1d449)

## 2. Logging Current Time with Python

### Step 1: Create Python Script
Create a file named `test.py`:
```python
import datetime

nowTime = datetime.datetime.now()
print(nowTime)
```
![Python Script](https://github.com/user-attachments/assets/e7acadb4-6fae-4891-82f5-78cd76daa935)

### Step 2: Configure and test Python Script
```bash
python3 test.py
```
![image](https://github.com/user-attachments/assets/ad9711e9-0b14-492b-b051-83bbb22de2cd)


### Step 3: Configure Crontab
```bash
crontab -e
```
![Python Script Test](https://github.com/user-attachments/assets/dcc6383f-1902-4602-abc5-11c566c6b2e4)

Add the following line:
```
* * * * * python3 /home/username/test.py >> /home/username/test.log
```

### Step 4: Restart Cron Service
```bash
sudo service cron restart
sudo service cron status
```
![Crontab Configuration for Python](https://github.com/user-attachments/assets/17f64f55-b12d-4cde-98ee-44319e2dbcbb)

### Step 5 : Result
![Cron Service Restart for Python](https://github.com/user-attachments/assets/aaaf21f6-7f99-495a-91ce-1e3bf2a89341)

## 3. Logging Disk Usage with Python

### Step 1: Create Python Script
Create a file named `disk.py`:
```python
import datetime
import os

nowTime = datetime.datetime.now()

disk = os.statvfs("/")
totalDisk = disk.f_blocks * disk.f_frsize / 1024 / 1024 / 1024
usedDisk = (disk.f_blocks - disk.f_bfree) * disk.f_frsize / 1024 / 1024 / 1024
freeDisk = disk.f_bavail * disk.f_frsize / 1024 / 1024 / 1024

print(nowTime, str(totalDisk)[:4]+"GB", str(usedDisk)[:4]+"GB", str(freeDisk)[:4]+"GB")

```
![Disk Usage Python Script](https://github.com/user-attachments/assets/bb57bae9-215a-4298-a826-69771a237c6c)

### Step 2: Test Python Script
```bash
python3 disk.py
```
![image](https://github.com/user-attachments/assets/492313aa-ea7c-42aa-b55e-69ffac74b98d)

### Step 3: Configure Crontab
```bash
crontab -e
```
Add the following line:
```
* * * * * python3 /home/username/disk.py >> /home/username/aaa.log
```
![Disk Usage Script Test](https://github.com/user-attachments/assets/45b02773-9f46-4382-a83c-d5a20285a428)


### Step 4: Restart Cron Service
```bash
sudo service cron restart
sudo service cron status
```
![Crontab Configuration for Disk Usage](https://github.com/user-attachments/assets/8ebd6339-de54-471f-bcea-135ce67d70d5)

### Step 5 : Result
![Cron Service Restart for Disk Usage](https://github.com/user-attachments/assets/e33c79fb-7ebc-4aa9-90e7-469293f3e851)

---
