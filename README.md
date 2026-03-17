# DevOps Foundation Training 

## DAY - 1

---

# 1️⃣ SDLC Models – Agile vs Waterfall

## What is SDLC?

SDLC (Software Development Life Cycle) is the structured process used to design, develop, test, and deploy software.

---

## 🔵 Waterfall Model

### Definition
Waterfall is a linear and sequential development model where each phase must be completed before moving to the next.

### Flow
Requirement → Design → Development → Testing → Deployment → Maintenance

### Key Characteristics
- Fixed scope
- Heavy documentation
- Late testing
- Difficult to accommodate changes
- Suitable for stable requirements

### Real-World Use Cases
- Government projects
- Banking systems
- Regulatory systems

### Why Not Ideal for DevOps?
- No continuous feedback
- Testing happens late
- Deployment only at end
- No CI/CD integration

---

## 🟢 Agile Model

### Definition
Agile is an iterative and incremental methodology that delivers software in small, usable pieces.

### Core Principles
- Frequent delivery of working software
- Continuous feedback
- Collaboration
- Adaptability to change

### Sprint Duration
Typically:
- 2 weeks
- 3 weeks
- 4 weeks

### Why Agile Fits DevOps?
- Supports Continuous Integration
- Supports Continuous Deployment
- Enables faster feedback loops
- Small incremental releases

---

# 2️⃣ Agile Terminologies

---

## 📘 Epic

A large feature that cannot be completed in one sprint.

Example:
> User Management System

---

## 📗 User Story

A small requirement written from the user's perspective.

### Format:
> As a <role>, I want <feature>, so that <benefit>

Example:
> As an admin, I want to create users so that I can manage access.

### INVEST Criteria
- Independent
- Negotiable
- Valuable
- Estimable
- Small
- Testable

---

## 📙 Task

Technical work required to complete a story.

Example:

Story: Create user

Tasks:
- Create API
- Create DB schema
- Write unit test
- Configure CI pipeline

---

## 🏃 Sprint

A fixed time-boxed iteration where selected stories are completed.

### Sprint Activities:
- Sprint Planning
- Daily Standup
- Development
- Testing
- Sprint Review
- Retrospective

---

# 3️⃣ Git & GitHub for DevOps Engineers

---

## What is Git?

Git is a distributed version control system used to track changes in:
- Application code
- Infrastructure as Code (Terraform)
- Kubernetes manifests
- CI/CD pipelines
- Configuration files

---

## What is GitHub?

GitHub is a cloud platform for hosting Git repositories.

### Features:
- Remote repositories
- Pull Requests
- Code reviews
- Branch protection
- CI/CD integration (GitHub Actions)

---

# 4️⃣ Core Git Concepts

---

## Repository
A project folder tracked by Git.

---

## Commit
A snapshot of changes.

---

## Branch
An independent line of development.

Common branches:
- main
- master
- feature/*
- bugfix/*

---

## Merge
Combines changes from one branch into another.

---

## Pull Request (PR)
A request to merge code into the main branch.

---

# 5️⃣ Git Commands Required for DevOps Engineers

---

## 🔹 Setup

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## 🔹 Initialize Repository

```bash
git init
```

---

## 🔹 Clone Repository

```bash
git clone <repo-url>
```

---

## 🔹 Check Status

```bash
git status
```

---

## 🔹 Add Files

Add single file:

```bash
git add file.txt
```

Add all files:

```bash
git add .
```

---

## 🔹 Commit

```bash
git commit -m "Added Dockerfile"
```

---

## 🔹 View History

```bash
git log
git log --oneline
```

---

## 🔹 Branching

Create branch:

```bash
git checkout -b feature/docker-setup
```

Switch branch:

```bash
git checkout main
```

---

## 🔹 Push Changes

```bash
git push origin main
```

Push new branch:

```bash
git push origin feature/docker-setup
```

---

## 🔹 Pull Changes

```bash
git pull origin main
```

---

## 🔹 Fetch

```bash
git fetch
```

(Fetch downloads changes but does NOT merge automatically.)

---

## 🔹 Merge

```bash
git merge feature/docker-setup
```

---

## 🔹 Rebase (Advanced)

```bash
git rebase main
```

---

## 🔹 Stash

```bash
git stash
git stash pop
```

---

## 🔹 View Differences

```bash
git diff
```

---

## 🔹 Delete Branch

```bash
git branch -d feature/docker-setup
```

---

## 🔹 Tagging Releases

```bash
git tag v1.0
git push origin v1.0
```

---

# 6️⃣ Git Workflow in DevOps Projects

---

## Feature Branch Workflow

1. Pull latest main branch
2. Create feature branch
3. Make changes
4. Commit changes
5. Push branch
6. Create Pull Request
7. Code review
8. Merge to main
9. CI/CD triggers deployment

---

# 7️⃣ Real DevOps Use Cases of Git

---

## Infrastructure as Code
Terraform files stored and version controlled in Git.

## Kubernetes Deployments
deployment.yaml, service.yaml tracked in Git.

## GitOps
Tools like ArgoCD pull manifests from Git and deploy automatically.

## CI/CD
GitHub Actions triggers on:
- push
- pull_request

---

# 8️⃣ Important Interview Topics

Make sure you understand:

- git fetch vs git pull
- merge vs rebase
- conflict resolution
- squash commits
- branching strategies (GitFlow vs Trunk-Based)
- .gitignore usage
- release tagging

---

# 9️⃣ Practice Exercise

1. Create a GitHub repository
2. Add:
   - Dockerfile
   - README.md
   - Kubernetes deployment.yaml
3. Create a feature branch
4. Raise a Pull Request
5. Merge into main
6. Setup simple GitHub Action workflow

---

### Day 2 

# Day-to-Day Linux Commands for DevOps Engineers

This guide lists commonly used Linux commands that DevOps engineers use for daily operations such as troubleshooting, system monitoring, file management, and networking.

---

## 1. Basic Navigation Commands

| Command | Description | Example |
|--------|-------------|--------|
| pwd | Print current working directory | pwd |
| ls | List files and directories | ls -l |
| cd | Change directory | cd /var/log |
| tree | Display directory structure | tree |

Example:

```
pwd
ls -la
cd /etc
tree
```

---

## 2. File and Directory Management

| Command | Description | Example |
|--------|-------------|--------|
| touch | Create empty file | touch file.txt |
| mkdir | Create directory | mkdir logs |
| cp | Copy files/directories | cp file.txt backup/ |
| mv | Move or rename files | mv file.txt newfile.txt |
| rm | Delete files/directories | rm file.txt |

Example:

```
mkdir project
touch app.log
cp app.log backup/
mv app.log app-old.log
rm app-old.log
```

---

## 3. File Viewing Commands

| Command | Description | Example |
|--------|-------------|--------|
| cat | Display file content | cat file.txt |
| less | View large files | less logfile.log |
| head | View first lines | head -n 10 file.txt |
| tail | View last lines | tail -n 20 file.txt |
| tail -f | Follow live logs | tail -f app.log |

Example:

```
cat config.yaml
less /var/log/syslog
tail -f application.log
```

---

## 4. Search and Text Processing

| Command | Description | Example |
|--------|-------------|--------|
| grep | Search text in files | grep error app.log |
| find | Find files | find / -name file.txt |
| awk | Pattern scanning | awk '{print $1}' file.txt |
| sed | Stream editor | sed 's/old/new/g' file.txt |
| wc | Count lines/words | wc -l file.txt |

Example:

```
grep ERROR app.log
find /var -name "*.log"
wc -l access.log
```

---

## 5. Process Management

| Command | Description | Example |
|--------|-------------|--------|
| ps | Show running processes | ps aux |
| top | Monitor processes | top |
| htop | Interactive process viewer | htop |
| kill | Kill process | kill 1234 |
| kill -9 | Force kill process | kill -9 1234 |

Example:

```
ps aux | grep nginx
top
kill 4567
```

---

## 6. System Monitoring

| Command | Description | Example |
|--------|-------------|--------|
| df | Disk usage | df -h |
| du | Directory size | du -sh /var/log |
| free | Memory usage | free -m |
| uptime | System uptime | uptime |
| vmstat | System performance | vmstat |

Example:

```
df -h
free -m
du -sh *
uptime
```

---

## 7. Networking Commands

| Command | Description | Example |
|--------|-------------|--------|
| ping | Test connectivity | ping google.com |
| curl | Test HTTP endpoints | curl http://localhost:8080 |
| wget | Download files | wget https://example.com/file |
| netstat | Network connections | netstat -tulnp |
| ss | Socket statistics | ss -tulnp |

Example:

```
ping 8.8.8.8
curl http://localhost:8080/health
ss -tulnp
```

---

## 8. Permissions and Ownership

| Command | Description | Example |
|--------|-------------|--------|
| chmod | Change file permissions | chmod 755 script.sh |
| chown | Change ownership | chown ubuntu:ubuntu file.txt |
| whoami | Show current user | whoami |

Example:

```
chmod +x deploy.sh
chown ec2-user:ec2-user app.log
```

---

## 9. Compression and Archiving

| Command | Description | Example |
|--------|-------------|--------|
| tar | Archive files | tar -cvf archive.tar folder |
| tar -xvf | Extract archive | tar -xvf archive.tar |
| gzip | Compress file | gzip file.txt |
| gunzip | Decompress file | gunzip file.txt.gz |

Example:

```
tar -cvf logs.tar logs/
tar -xvf logs.tar
gzip file.txt
```

---

## 10. Useful DevOps Commands

| Command | Description |
|--------|-------------|
| history | Show command history |
| watch | Run command repeatedly |
| crontab -l | View scheduled jobs |
| crontab -e | Edit cron jobs |

Example:

```
history
watch df -h
crontab -l
```

---

## 11. Log Troubleshooting (Very Important for DevOps)

```
tail -f /var/log/syslog
tail -f /var/log/messages
journalctl -u nginx
journalctl -xe
```

---

## Quick DevOps Troubleshooting Workflow

1. Check pod/server status  
2. Check logs  
3. Check CPU/Memory  
4. Check disk usage  
5. Check network connectivity  

Example:

```
top
df -h
free -m
ping service
tail -f /var/log/app.log
```


DAY 4
⏺ # AWS Cloud - Beginner's Guide (Hands-On from Console)                                                                                                           
                                                                                          
  ## Prerequisites                                                                                                                                                 
  - AWS Account (Free Tier: https://aws.amazon.com/free)                                                                                                           
  - A browser (Chrome / Firefox)                                                                                                                                   
  - Login to: https://console.aws.amazon.com                                                                                                                       
                  
  ---

  ## Module 1: AWS S3 (Simple Storage Service)
  **What is S3?** Object storage to store files (images, videos, backups, static websites).

  ### Key Concepts
  - **Bucket** → Container (like a folder) to store objects
  - **Object** → Any file you upload
  - **Region** → Physical location of your data

  ### Hands-On Lab 1 — Create a Bucket & Upload a File
  1. Go to **S3** in the AWS Console
  2. Click **Create bucket**
  3. Enter a unique bucket name (e.g., `myname-demo-bucket-2024`)
  4. Choose a region (e.g., `us-east-1`)
  5. Keep all defaults → Click **Create bucket**
  6. Click on your bucket → Click **Upload**
  7. Upload any file (image or text file)
  8. Click on the uploaded file → observe the **Object URL**

  ### Hands-On Lab 2 — Host a Static Website
  1. Go to your bucket → **Properties** tab
  2. Scroll to **Static website hosting** → Enable it
  3. Set index document: `index.html`
  4. Go to **Permissions** tab → Edit **Block Public Access** → Uncheck all → Save
  5. Add a **Bucket Policy** to make files public:
  ```json
  {
    "Version": "2012-10-17",
    "Statement": [{
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
    }]
  }
  6. Upload an index.html file → Access the website URL

  ---
  Module 2: AWS EC2 (Elastic Compute Cloud)

  What is EC2? Virtual machines (servers) in the cloud.

  Key Concepts

  - Instance → A virtual server
  - AMI → Amazon Machine Image (OS template: Amazon Linux, Ubuntu, etc.)
  - Instance Type → CPU + RAM specs (e.g., t2.micro = Free Tier)
  - Key Pair → SSH key to log into your server
  - Security Group → Firewall rules (which ports are open)
  - Elastic IP → Static public IP for your instance

  Hands-On Lab 1 — Launch an EC2 Instance

  1. Go to EC2 → Click Launch Instance
  2. Name: my-first-server
  3. AMI: Amazon Linux 2023 (Free Tier eligible)
  4. Instance type: t2.micro (Free Tier)
  5. Key pair: Click Create new key pair → Name it → Download the .pem file (save it!)
  6. Network settings: Allow SSH (port 22) and HTTP (port 80)
  7. Click Launch Instance


  Hands-On Lab 2 — Install a Web Server (Apache)

  1. Connect to your instance:
    - Select your instance → Click Connect → Use EC2 Instance Connect (browser SSH)
  2. Run these commands:
  sudo yum update -y
  sudo yum install httpd -y
  sudo systemctl start httpd
  sudo systemctl enable httpd
  echo "<h1>Hello from My EC2 Server!</h1>" | sudo tee /var/www/html/index.html
  3. Copy the Public IPv4 address of your instance
  4. Paste in browser: http://YOUR-PUBLIC-IP → You should see your webpage!

## DAY 5 - AWS IAM & EC2 Deep Dive

### Module 11: IAM — Users, Groups, Policies

**Simple Analogy:** IAM is like an **office building access card system**.
- **Root Account** = Building owner (has all keys — use only for emergencies)
- **IAM User** = Individual employee with their own access card
- **IAM Group** = Department (Developers, DevOps, Finance) — assign permissions once to the group
- **IAM Policy** = Rules on the card (can enter Server Room, cannot enter CEO office)

**Key Concepts:**
| Term | What it means |
|------|--------------|
| User | A person or app that logs into AWS |
| Group | Collection of users sharing same permissions |
| Policy | JSON document saying what is Allow/Deny |
| Role | Temporary access (for EC2, Lambda, etc.) |

**Policy Example (Read-only S3):**
```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Effect": "Allow",
    "Action": ["s3:GetObject", "s3:ListBucket"],
    "Resource": "*"
  }]
}
```

**Hands-on Lab:**
1. Go to AWS Console → IAM
2. Create a Group called `Developers` → attach `AmazonEC2ReadOnlyAccess` policy
3. Create a User `dev-user` → add to `Developers` group
4. Enable Console Access with a password
5. Login with `dev-user` → try to **stop** an EC2 instance → it will be **denied** ✅
6. **Best Practice:** Never use root account for daily tasks — always create IAM users

---

### Module 12: Security Groups

**Simple Analogy:** Security Group is a **firewall/bouncer** at the door of your EC2 instance.
- Controls **who can come IN** (Inbound rules) and **who you can reach OUT to** (Outbound rules)
- Works at the **instance level**
- **Stateful** — if you allow inbound traffic, the response automatically goes out

**Key Concepts:**
| Term | Meaning |
|------|---------|
| Inbound Rules | Traffic allowed TO your instance |
| Outbound Rules | Traffic allowed FROM your instance |
| Port | Door number (HTTP=80, HTTPS=443, SSH=22, MySQL=3306) |
| Source | Who is allowed (IP, CIDR, or another Security Group) |

**Common Rules for a Web Server:**
```
Inbound:
  HTTP  (Port 80)  → Source: 0.0.0.0/0      (everyone)
  HTTPS (Port 443) → Source: 0.0.0.0/0      (everyone)
  SSH   (Port 22)  → Source: Your IP only   (e.g. 203.0.113.5/32)

Outbound:
  All traffic → 0.0.0.0/0   (allow everything out — default)
```

**Hands-on Lab:**
1. Launch an EC2 instance (Amazon Linux 2)
2. Add Inbound Rule: SSH Port 22, Source = My IP
3. SSH into the instance — it works ✅
4. **Remove** the SSH rule → try again → **Connection timed out** ✅
5. Add HTTP Port 80 → install Apache → access via browser ✅
6. add below script to userdata.
```bash

#!/bin/bash
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
echo "<h1>Hello from EC2!</h1>" | sudo tee /var/www/html/index.html
```

---

### Module 13: EC2 Instance Role (IAM Role for EC2)

**Simple Analogy:** Instead of giving your **employee (EC2)** a username/password to access the filing room (S3), you give them a **badge (role)** that grants automatic temporary access — no passwords stored anywhere.

**Why use Roles instead of Access Keys?**
- Access keys stored on EC2 can be stolen if the instance is compromised
- Roles provide **temporary credentials** that auto-rotate every few hours
- No hardcoded secrets in your code or environment

**How it works:**
```
EC2 Instance → Assumes IAM Role → Gets temporary credentials → Accesses AWS services
```

**Hands-on Lab:**
1. IAM → Roles → Create Role → Select **EC2** as trusted entity
2. Attach policy: `AmazonS3ReadOnlyAccess`
3. Name it: `ec2-s3-read-role`
4. Launch EC2 → under **IAM Instance Profile** select `ec2-s3-read-role`
5. SSH into EC2 → run:
```bash
# No credentials needed — role provides them automatically!
aws s3 ls                           # Lists your S3 buckets ✅
aws s3 cp s3://your-bucket/file .   # Downloads a file ✅
```
6. Launch another EC2 **without** the role → run same commands → **Access Denied** ✅

---

DAY 6

### Module 14: EC2 Instance Purchasing Options

**Simple Analogy:** Like booking a hotel — different ways to pay based on your needs.

| Option | Hotel Analogy | Best For | Savings |
|--------|--------------|----------|---------|
| **On-Demand** | Pay per night, no commitment | Dev/test, unpredictable workloads | Baseline |
| **Reserved (1yr/3yr)** | Book room for a year upfront | Steady production workloads | Up to 72% |
| **Savings Plans** | Commit to hourly spend | Flexible workloads | Up to 66% |
| **Spot Instances** | Last-minute hotel deal | Batch jobs, fault-tolerant tasks | Up to 90% |
| **Dedicated Host** | Rent entire hotel floor | Compliance/BYOL licensing | Varies |
| **Dedicated Instance** | Private room, no shared walls | Security-sensitive workloads | Higher cost |

**Rule of Thumb:**
```
Always-on production DB?    → Reserved Instance (1 or 3 year)
Variable web traffic?       → On-Demand + Auto Scaling
Big data / ML training?     → Spot Instances (cheap, but can be interrupted)
Compliance required?        → Dedicated Host
```

**Hands-on Lab:**
1. EC2 Console → **Spot Requests** → Request Spot Instance
2. Set max price (e.g., `$0.01/hr` for t3.micro)
3. Instance launches only when spot price ≤ your max price ✅
4. Go to **AWS Cost Explorer** → Savings Plans → view the savings calculator

---

### Module 15: Private IP, Public IP, and Elastic IP

**Simple Analogy:**
- **Private IP** = Your home address — only reachable inside your neighborhood (VPC)
- **Public IP** = Your phone number — internet-reachable, but changes when you restart
- **Elastic IP** = A permanent phone number you own — never changes

| Type | Scope | Changes on Reboot? | Cost |
|------|-------|-------------------|------|
| Private IP | Inside VPC only | No — always same | Free |
| Public IP | Internet-facing | Yes — on stop/start | Free while running |
| Elastic IP | Internet-facing | No — static | Free if attached; ~$0.005/hr if idle |

**IP Ranges:**
```
Private IPs use RFC 1918 ranges:
  10.0.0.0/8
  172.16.0.0/12
  192.168.0.0/16

Public IPs:  Assigned from AWS pool, released when instance stops
Elastic IP:  Allocated to your account, you assign/reassign freely
```

**Hands-on Lab:**
1. Launch EC2 → note the **Public IP** (e.g., `54.123.45.67`) and **Private IP** (e.g., `10.0.1.25`)
2. **Stop** the instance → **Start** it → Public IP **changed** ✅, Private IP stayed same ✅
3. Allocate an Elastic IP: EC2 → Elastic IPs → **Allocate Elastic IP address**
4. Associate it with your instance
5. Stop and Start again → Elastic IP **stays the same** ✅
6. **Cleanup:** Release Elastic IP when not in use to avoid charges

---

### Module 16: EC2 Storage — EBS and EFS

**Simple Analogy:**
- **EBS** = USB hard drive — plugged into **one laptop (EC2)** at a time
- **EFS** = Network shared drive (like Google Drive) — **multiple EC2s** can read/write simultaneously

#### EBS (Elastic Block Store)

| Feature | Details |
|---------|---------|
| Type | Block storage (like a hard disk) |
| Attachment | One EC2 at a time (must be in same AZ) |
| Persistence | Data survives instance stop/start |
| Use case | OS disk, databases, application data |

**EBS Volume Types:**
```
gp3  → General Purpose SSD     — default, best price/performance
gp2  → Older General Purpose SSD
io2  → Provisioned IOPS SSD    — high-performance databases (MySQL, Oracle)
st1  → Throughput HDD          — big data, log processing
sc1  → Cold HDD                — infrequent access, cheap archival
```

**EBS Hands-on Lab:**
```bash
# 1. Create a 10GB gp3 volume in same AZ as your EC2
# 2. EC2 Console → Volumes → Attach Volume → select your instance

# 3. SSH into EC2 and set it up:
lsblk                           # See the new disk (e.g., /dev/xvdf)
sudo mkfs -t ext4 nvme1n1    # Format the disk
sudo mkdir /data                # Create mount point
sudo mount /dev/nvme1n1 /data      # Mount it
df -h                           # Verify it's mounted ✅

# 4. Write and read data:
echo "Hello EBS" | sudo tee /data/test.txt
cat /data/test.txt              # Hello EBS ✅

# 5. Persist mount across reboots — add to /etc/fstab:
echo "/dev/xvdf /data ext4 defaults,nofail 0 2" | sudo tee -a /etc/fstab
```

#### EFS (Elastic File System)

| Feature | Details |
|---------|---------|
| Type | Network file system (NFS) |
| Attachment | Multiple EC2s simultaneously, across AZs |
| Scaling | Automatically grows and shrinks |
| Use case | Shared web content, CMS files, ML datasets |

**EFS Hands-on Lab:**
```bash
# 1. EFS Console → Create File System → select your VPC → Create

# 2. On BOTH EC2 instances — install NFS client:
sudo yum install -y amazon-efs-utils

# 3. Mount on both instances (replace fs-XXXXXXXX with your EFS ID):
sudo mkdir /shared
sudo mount -t efs fs-XXXXXXXX:/ /shared

# 4. On EC2-1 — write a file:
echo "Written from EC2-1" | sudo tee /shared/hello.txt

# 5. On EC2-2 — read the same file:
cat /shared/hello.txt           # "Written from EC2-1" ✅ Shared storage works!
```

**EBS vs EFS — When to use which:**
```
Use EBS when:
  ✅ Single EC2 needs fast, dedicated storage
  ✅ Running a database (MySQL, PostgreSQL)
  ✅ OS root volume

Use EFS when:
  ✅ Multiple EC2s need to share the same files
  ✅ Web server farm serving same static content
  ✅ Machine learning — multiple training nodes reading same dataset
```

---

### DAY 5 Summary

| Topic | Key Takeaway |
|-------|-------------|
| IAM Users/Groups/Policies | Never use root; use groups to manage permissions at scale |
| Security Groups | Stateful firewall at instance level; deny by default |
| EC2 Instance Role | Assign roles, never hardcode credentials on EC2 |
| Purchasing Options | On-Demand for flexibility, Reserved for savings, Spot for batch |
| IP Types | Elastic IP = static public IP you own; regular public IP changes on reboot |
| EBS vs EFS | EBS = one EC2, EFS = shared across many EC2s |

  

  ---
  Module 3: AWS Load Balancer (ELB)

  What is a Load Balancer? Distributes incoming traffic across multiple EC2 instances.

  Key Concepts

  - ALB (Application Load Balancer) → HTTP/HTTPS traffic (most common)
  - Target Group → Group of EC2 instances that receive traffic
  - Listener → Checks for connection requests (e.g., on port 80)
  - Health Check → Automatically removes unhealthy instances

  Hands-On Lab — Create an Application Load Balancer

  1. Launch 2 EC2 instances (repeat Module 2 steps) with different HTML content:
    - Server 1: <h1>Hello from Server 1!</h1>
    - Server 2: <h1>Hello from Server 2!</h1>
  2. Go to EC2 → Target Groups → Create target group
    - Type: Instances
    - Name: my-target-group
    - Protocol: HTTP, Port: 80
    - Health check path: /
    - Click Next → Select both EC2 instances → Include as pending → Create
  3. Go to Load Balancers → Create Load Balancer → Choose Application Load Balancer
    - Name: my-alb
    - Scheme: Internet-facing
    - Select at least 2 Availability Zones
    - Security group: Allow HTTP port 80
    - Listener: Forward to your target group
    - Click Create
  4. Wait for the ALB state to become Active
  5. Copy the DNS name of the ALB → Paste in browser
  6. Refresh multiple times → Traffic alternates between Server 1 and Server 2!

  ---
  Module 4: AWS Lambda

  What is Lambda? Run code WITHOUT managing servers. Pay only when code runs.

  Key Concepts

  - Function → Your code (Python, Node.js, Java, etc.)
  - Trigger → What invokes the function (API Gateway, S3 event, schedule, etc.)
  - Event → Input data passed to the function
  - Execution Role → IAM permissions for the Lambda function

  Hands-On Lab 1 — Your First Lambda Function

  1. Go to Lambda → Click Create function
  2. Choose Author from scratch
  3. Name: my-first-lambda
  4. Runtime: Python 3.12
  5. Click Create function
  6. In the code editor, replace with:
  import json

  def lambda_handler(event, context):
      name = event.get("name", "World")
      return {
          "statusCode": 200,
          "body": json.dumps(f"Hello, {name}! Welcome to Lambda!")
      }
  7. Click Deploy
  8. Click Test → Create a test event:
  {
    "name": "Alice"
  }
  9. Click Test → See the output in Execution results!

  Hands-On Lab 2 — Trigger Lambda from API Gateway

  1. In your Lambda function → Click Add trigger
  2. Select API Gateway
  3. Create a new API → Choose HTTP API → Click Add
  4. Click on the API Gateway trigger → Copy the API endpoint URL
  5. Paste in browser: https://YOUR-API-URL?name=Alice
  6. See the JSON response in the browser!

  ---
  Module 5: Putting It All Together — Architecture Overview

  User Request
       │
       ▼
  [Route 53 / DNS]
       │
       ▼
  [Application Load Balancer]
       │
     ┌─┴──────────┐
     ▼            ▼
  [EC2 Server 1] [EC2 Server 2]
     │
     ▼
  [S3 Bucket] ← Static files / images

  [Lambda] ← Background tasks / API processing

  ---
  Cleanup — Avoid Charges!

  After each lab, delete resources to stay within Free Tier:

  ┌─────────────────┬──────────────────────────────────────────────┐
  │    Resource     │                How to Delete                 │
  ├─────────────────┼──────────────────────────────────────────────┤
  │ S3 Bucket       │ Empty the bucket first → then delete         │
  ├─────────────────┼──────────────────────────────────────────────┤
  │ EC2 Instance    │ Select instance → Instance State → Terminate │
  ├─────────────────┼──────────────────────────────────────────────┤
  │ Load Balancer   │ Select ALB → Actions → Delete                │
  ├─────────────────┼──────────────────────────────────────────────┤
  │ Target Group    │ Select → Actions → Delete                    │
  ├─────────────────┼──────────────────────────────────────────────┤
  │ Lambda Function │ Select → Actions → Delete                    │
  └─────────────────┴──────────────────────────────────────────────┘

  ---
  Learning Path (Recommended Order)

  Week 1: IAM (Users, Roles, Policies) + S3
  Week 2: EC2 + Security Groups + Key Pairs
  Week 3: Load Balancer + Auto Scaling
  Week 4: Lambda + API Gateway
  Week 5: RDS (Database) + VPC (Networking)
  Week 6: CloudWatch (Monitoring) + CloudFormation (Infrastructure as Code)

  ---
  Useful Links

  - AWS Free Tier: https://aws.amazon.com/free
  - AWS Console: https://console.aws.amazon.com
  - AWS Documentation: https://docs.aws.amazon.com
  - AWS Architecture Icons: https://aws.amazon.com/architecture/icons

  ---
  Tips for Learners

  - Always choose us-east-1 (N. Virginia) — most services are available here
  - Use Free Tier instances (t2.micro) to avoid charges
  - Always delete resources after practice
  - Enable Billing Alerts in your account to avoid surprise bills
  - Use IAM users instead of the root account for daily work

  ---

  This README covers:

  - **4 core services** with concept explanations + hands-on labs each
  - **Step-by-step console instructions** a newcomer can follow
  - **Architecture diagram** showing how all services connect
  - **Cleanup steps** to avoid unexpected AWS charges
  - **6-week learning roadmap** for structured progression

  


