# AWS CLI Basics - Solution

Name: Balint Lojt

GitHub Username: lojt-cloud

---

# Task 1 - Verify AWS CLI

## aws --version
aws-cli/2.31.35 Python/3.14.4 Linux/6.6.114.1-microsoft-standard-WSL2 source/x86_64.ubuntu.26

```

### Screenshot

<img width="929" height="76" alt="task1-aws-version" src="https://github.com/user-attachments/assets/26a5b265-760e-423d-80a7-61a9eec177ee" />


---

# Task 2 - AWS Configuration

## aws configure list

NAME       : VALUE                    : TYPE             : LOCATION
profile    : <not set>                : None             : None
access_key : ****************UA73     : shared-credentials-file :
secret_key : ****************5CXA     : shared-credentials-file :
region     : eu-west-2                : config-file      : ~/.aws/config

```

### Screenshot

<img width="912" height="279" alt="task2-configure-list" src="https://github.com/user-attachments/assets/635c6c32-8250-4258-888f-081d441c0360" />


---

# Task 3 - Caller Identity

## aws sts get-caller-identity

 aws sts get-caller-identity
{
    "UserId": "*************27NCE",
    "Account": "*************010",
    "Arn": "arn:aws:iam::*************010:user/lojt-bootcamp"
}

```

### Screenshot


<img width="846" height="167" alt="task3-caller-identity" src="https://github.com/user-attachments/assets/f9dec890-a0fb-4ce6-ab82-caaf3415c8a9" />


# Task 4 - AWS Regions

Number of Regions:17

Default Region: eu-west-2

Closest Region: REGIONS ec2.eu-central-1.amazonaws.com  opt-in-not-required     eu-central-1  (Frankfurt)

### Screenshot

<img width="816" height="336" alt="task4-regions" src="https://github.com/user-attachments/assets/a4854f02-44ca-4df8-aafd-16c21be99976" />


---

# Task 5 - Availability Zones

Number of AZs: 123

Why are multiple AZs important?
Since AZs are physically isolated, a localised disaster or power outage in one zone won’t affect the others, traffic is automatically rerouted to a healthy zone to prevent downtime.
The ultra low latency between AZs enables real-time data replication, preventing data loss and allowing for automated disaster recovery.

### Screenshot

<img width="647" height="762" alt="task5-availability-zones" src="https://github.com/user-attachments/assets/abfdfa94-1bf3-4be7-abb6-61f961872861" />


---

# Task 6 - S3 Investigation

Buckets:

Reason if none exist:

### Screenshot

![Task 6](screenshots/task6-s3-buckets.png)

---

# Task 7 - IAM Investigation

IAM Users:

Why avoid using the root account?

### Screenshot

![Task 7](screenshots/task7-iam-users.png)

---

# Task 8 - EC2 Investigation

Running Instances:

Key Pairs:

Instance Types:

### Screenshot

![Task 8](screenshots/task8-ec2-info.png)

---

# Task 9 - Output Formats

Preferred format:

Reason:

### Screenshot

![Task 9](screenshots/task9-output-formats.png)

---

# Reflection

...

---

# Bonus

### Screenshot

![Bonus](screenshots/bonus-vpc.png)
