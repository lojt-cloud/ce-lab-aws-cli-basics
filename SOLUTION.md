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

What is your AWS Account ID?
*********010
What is your IAM User ARN?
Arn": "arn:aws:iam::********010:user/lojt-bootcamp
What is your configured default Region?
eu-west-2
What output format is configured?
json
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

### Screenshot


<img width="846" height="167" alt="task3-caller-identity" src="https://github.com/user-attachments/assets/f9dec890-a0fb-4ce6-ab82-caaf3415c8a9" />


# Task 4 - AWS Regions

Number of Regions:17

Default Region: eu-west-2

Closest Region: REGIONS ec2.eu-central-1.amazonaws.com  opt-in-not-required     eu-central-1  (Frankfurt)

Why should production workloads use multiple Availability Zones?
Because if a major incident (like a power outage, flood, or fire) knocks out an entire data centre facility in one zone, the application won't go offline. Traffic will automatically route to the remaining zones, keeping the app running smoothly without any downtime or data loss.

### Screenshot

<img width="816" height="336" alt="task4-regions" src="https://github.com/user-attachments/assets/a4854f02-44ca-4df8-aafd-16c21be99976" />


---

# Task 5 - Availability Zones

Number of AZs: 123

Why are multiple AZs important?
Since AZs are physically isolated, a localised disaster or power outage in one zone won’t affect the others, traffic is automatically rerouted to a healthy zone to prevent downtime.
The ultra-low latency between AZs enables real-time data replication, preventing data loss and allowing for automated disaster recovery.

### Screenshot

<img width="647" height="762" alt="task5-availability-zones" src="https://github.com/user-attachments/assets/abfdfa94-1bf3-4be7-abb6-61f961872861" />


---

# Task 6 - S3 Investigation

Buckets:
2026-07-06 12:31:56 aws-cloudtrail-logs-743631836010-4d76b8fa
2026-07-06 12:34:08 aws-cloudtrail-logs-743631836010-65e73e3a

Reason if none exist:
N/A

### Screenshot

<img width="583" height="65" alt="task6-s3-buckets" src="https://github.com/user-attachments/assets/29540653-4a86-4afe-bc74-de0f6d94924b" />


---

# Task 7 - IAM Investigation

IAM Users:
1 
------------------------------------------------------------------
|                            ListUsers                           |
+----------------------------------------------------------------+
||                             Users                            ||
|+------------+-------------------------------------------------+|
||  Arn       |  arn:aws:iam::********010:user/lojt-bootcamp    ||
||  CreateDate|  2026-07-06T19:28:57+00:00                      ||
||  Path      |  /                                              ||
||  UserId    | *****************27NCE                          ||
||  UserName  |  lojt-bootcamp                                  ||
|+------------+-------------------------------------------------+|

Why avoid using the root account?
The root account has absolute, unrestricted power over the entire AWS account, including billing and the ability to delete everything. If those credentials are leaked or hacked, someone could easily lock the owner out, delete infrastructure, or run up a massive bill.

### Screenshot

<img width="856" height="315" alt="task7-iam-users" src="https://github.com/user-attachments/assets/6ac7a27d-ce95-4942-bf45-02c39486d014" />


---

# Task 8 - EC2 Investigation

Running Instances:
none

Key Pairs:
none

Instance Types:
N/A

### Screenshot

<img width="606" height="190" alt="task8-ec2-info" src="https://github.com/user-attachments/assets/d94edcbe-aefa-4fc8-ba8e-e56c160f6bbf" />


---

# Task 9 - Output Formats

Preferred format:
json

Reason:
JSON is the industry standard for AWS because it structures the data cleanly, making it easy to read. It's also the best format that can be used to pass the CLI output into other tools, scripts, or automation.

### Screenshot

<img width="424" height="69" alt="task9-output-formats" src="https://github.com/user-attachments/assets/08403e1f-3439-4063-9ac7-1ff27d116203" />


---

# Reflection
Moving away from clicking around the AWS console and switching entirely to the command line felt like a turning point in how I view the cloud. Running commands to pull account details, check security identities, and audit active EC2 resources helped me understand how actual cloud engineers manage infrastructure efficiently. The standout concept for me was how AWS handles resilience. Seeing firsthand how regions map out and realising that Availability Zones are physically separated to survive major power outages, while still being close enough to share data instantly.


# Bonus

### Screenshot

![Bonus](screenshots/bonus-vpc.png)
