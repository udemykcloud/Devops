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




  ######### Day 5 ###################################################


  # AWS Networking for Beginners — VPC Deep Dive                                                                                  
                                                                                                                                  
  ---                                                                                                                             
                                                                                                                                  
  ## 1. What is a Region and Availability Zone?

  ┌─────────────────────────────────────────────────────────┐
  │                    AWS CLOUD                            │
  │                                                         │
  │   ┌─────────────────────────────────────────────────┐   │
  │   │            REGION  (e.g. us-east-1)             │   │
  │   │                                                 │   │
  │   │  ┌──────────────┐    ┌──────────────┐           │   │
  │   │  │     AZ - 1a  │    │     AZ - 1b  │           │   │
  │   │  │  (Data Ctr1) │    │  (Data Ctr2) │           │   │
  │   │  └──────────────┘    └──────────────┘           │   │
  │   │                                                 │   │
  │   │  ┌──────────────┐                               │   │
  │   │  │     AZ - 1c  │  ← Each AZ = isolated        │   │
  │   │  │  (Data Ctr3) │    physical data center       │   │
  │   │  └──────────────┘                               │   │
  │   └─────────────────────────────────────────────────┘   │
  └─────────────────────────────────────────────────────────┘

  | Term              | Definition                                                      |
  |-------------------|-----------------------------------------------------------------|
  | **Region**        | A geographic area with multiple data centers (e.g., us-east-1) |
  | **Availability Zone (AZ)** | One or more isolated data centers within a Region    |

  > **Rule of thumb:** Deploy resources across multiple AZs for high availability.

  ---

  ## 2. What is a VPC?

  A **Virtual Private Cloud (VPC)** is your own logically isolated network inside AWS. Think of it as your own private data center
   in the cloud.

  ┌──────────────────────────────────────────────────────────────────────┐
  │                        YOUR VPC  (10.0.0.0/16)                       │
  │                                                                      │
  │   ┌────────────────────────┐    ┌────────────────────────┐           │
  │   │  PUBLIC SUBNET         │    │  PRIVATE SUBNET         │           │
  │   │  10.0.1.0/24  (AZ-1a) │    │  10.0.2.0/24  (AZ-1b)  │           │
  │   │                        │    │                         │           │
  │   │  ┌──────────────────┐  │    │  ┌──────────────────┐  │           │
  │   │  │   EC2 (Web App)  │  │    │  │   EC2 (Database) │  │           │
  │   │  │   Elastic IP     │  │    │  │   No Public IP   │  │           │
  │   │  └──────────────────┘  │    │  └──────────────────┘  │           │
  │   └──────────┬─────────────┘    └────────────┬────────────┘           │
  │              │                               │                        │
  │   ┌──────────▼─────────────────────────────────────────────────────┐ │
  │   │               ROUTER  (implicit, always present)               │ │
  │   └──────────┬─────────────────────────────────────────────────────┘ │
  │              │                                                        │
  │   ┌──────────▼─────────┐      ┌─────────────────────┐                │
  │   │  INTERNET GATEWAY  │      │     NAT GATEWAY      │                │
  │   │  (Public traffic)  │      │  (Private→Internet)  │                │
  │   └──────────┬─────────┘      └──────────────────────┘                │
  └──────────────┼───────────────────────────────────────────────────────┘
                 │
          ┌──────▼──────┐
          │  INTERNET   │
          └─────────────┘

  ---

  ## 3. VPC Components Explained

  ### 3.1 Subnet

  A **subnet** is a range of IP addresses within your VPC. It lives in one AZ.

  | Type            | Has Route to Internet? | Use Case              |
  |-----------------|------------------------|-----------------------|
  | Public Subnet   | Yes (via IGW)          | Web servers, Load balancers |
  | Private Subnet  | No (only via NAT)      | Databases, App servers |

  ---

  ### 3.2 Route Table

  A **route table** is a set of rules (routes) that determines where network traffic is directed.

  PUBLIC SUBNET Route Table:
  ┌─────────────────────────────────────────────────────┐
  │  Destination        │  Target                       │
  │─────────────────────│───────────────────────────────│
  │  10.0.0.0/16        │  local          ← VPC traffic │
  │  0.0.0.0/0          │  igw-xxxxxxxx   ← Internet    │
  └─────────────────────────────────────────────────────┘

  PRIVATE SUBNET Route Table:
  ┌─────────────────────────────────────────────────────┐
  │  Destination        │  Target                       │
  │─────────────────────│───────────────────────────────│
  │  10.0.0.0/16        │  local          ← VPC traffic │
  │  0.0.0.0/0          │  nat-xxxxxxxx   ← NAT Gateway │
  └─────────────────────────────────────────────────────┘

  ---

  ### 3.3 Router

  The **implicit router** in a VPC handles all traffic between subnets and to/from gateways. It is automatically created — you
  don't manage it directly. You control its behavior through Route Tables.

  ---

  ### 3.4 Internet Gateway (IGW)

  An **Internet Gateway** is a horizontally scaled, redundant VPC component that allows communication between your VPC and the
  internet.

  EC2 (Public Subnet) ──► Route Table (0.0.0.0/0 → IGW) ──► Internet Gateway ──► Internet

  - Attach one IGW per VPC
  - Enables inbound AND outbound internet traffic for public subnets

  ---

  ### 3.5 NAT Gateway

  A **NAT (Network Address Translation) Gateway** allows instances in a **private subnet** to initiate outbound traffic to the
  internet while blocking inbound connections.

  EC2 (Private Subnet) ──► Route Table (0.0.0.0/0 → NAT GW) ──► NAT GW (Public Subnet) ──► IGW ──► Internet

  - NAT GW lives in a **public subnet**
  - It has an **Elastic IP** attached
  - Traffic is one-way: private → internet only

  ---

  ### 3.6 Elastic IP (EIP)

  A **static, public IPv4 address** allocated to your AWS account that you can attach to EC2 instances or NAT Gateways.

  Without EIP: EC2 reboots → public IP changes
  With EIP:    EC2 reboots → same public IP always

  ---

  ### 3.7 Elastic Network Interface (ENI)

  An **ENI** is a virtual network card that you can attach to EC2 instances. Every instance has at least one (the primary ENI).

  EC2 Instance
  ├── eth0 (Primary ENI) — Private IP: 10.0.1.10, Public IP: 54.x.x.x
  └── eth1 (Secondary ENI) — Private IP: 10.0.2.20 (e.g., for dual-homing)

  ENIs carry: private IPs, public IPs, MAC address, security groups.

  ---

  ### 3.8 Customer Gateway & VPN Connection

  Used to connect your **on-premises data center** to your AWS VPC over an encrypted IPSec tunnel.

  On-Premises Data Center          AWS VPC
  ┌────────────────────┐           ┌───────────────────────┐
  │  Your Router       │           │  Virtual Private       │
  │  (Customer GW)     │◄─────────►│  Gateway (VGW)        │
  │  IP: 203.x.x.x    │  VPN       │                       │
  └────────────────────┘  Tunnel   └───────────────────────┘

  | Component           | Description                                     |
  |---------------------|-------------------------------------------------|
  | **Customer Gateway**| Represents your on-prem router in AWS           |
  | **Virtual Private Gateway** | AWS side of the VPN connection         |
  | **VPN Connection**  | Encrypted IPSec tunnel between both             |

  ---

  ### 3.9 VPC Endpoints

  A **VPC Endpoint** lets your instances access AWS services (S3, DynamoDB) **without going through the internet**.

  WITHOUT Endpoint:
  EC2 ──► NAT GW ──► Internet ──► S3    ❌ (traffic leaves AWS)

  WITH Endpoint:
  EC2 ──► VPC Endpoint ──► S3           ✅ (traffic stays in AWS)

  | Type              | Used For                       |
  |-------------------|-------------------------------|
  | **Gateway Endpoint** | S3, DynamoDB               |
  | **Interface Endpoint** | Most other AWS services  |

  ---

  ### 3.10 VPC Peering

  **VPC Peering** connects two VPCs so resources can communicate using private IPs, as if they are in the same network.

  ┌─────────────────┐         ┌─────────────────┐
  │    VPC A        │         │    VPC B        │
  │  10.0.0.0/16    │◄───────►│  172.16.0.0/16  │
  │                 │  VPC    │                 │
  │  EC2: 10.0.1.5  │ Peering │ EC2: 172.16.1.8 │
  └─────────────────┘         └─────────────────┘

  **Rules:**
  - No overlapping CIDR blocks
  - Not transitive (A↔B and B↔C does NOT mean A↔C)
  - Works cross-account and cross-region

  ---

  ## 4. Full VPC Architecture Diagram

                            INTERNET
                               │
                   ┌───────────▼────────────┐
                   │    Internet Gateway     │
                   └───────────┬────────────┘
                               │
      ┌────────────────────────▼─────────────────────────────┐
      │                  VPC  10.0.0.0/16                    │
      │                                                       │
      │   ┌──────────────────────────────────────────────┐   │
      │   │         PUBLIC SUBNET  10.0.1.0/24  (AZ-1a)  │   │
      │   │                                               │   │
      │   │   ┌──────────────┐    ┌───────────────────┐  │   │
      │   │   │  EC2 Web App │    │    NAT Gateway     │  │   │
      │   │   │  EIP attached│    │    EIP attached    │  │   │
      │   │   │  ENI: eth0   │    │                   │  │   │
      │   │   └──────────────┘    └─────────┬─────────┘  │   │
      │   └──────────────────────────────────┼────────────┘   │
      │                                      │                 │
      │   ┌──────────────────────────────────┼────────────┐   │
      │   │         PRIVATE SUBNET 10.0.2.0/24 (AZ-1b)    │   │
      │   │                                  │             │   │
      │   │   ┌──────────────┐    ┌──────────▼──────────┐  │   │
      │   │   │  EC2 DB      │    │  Route Table:        │  │   │
      │   │   │  No Public IP│    │  0.0.0.0/0 → NAT GW  │  │   │
      │   │   │  ENI: eth0   │    └─────────────────────┘  │   │
      │   │   └──────────────┘                             │   │
      │   └────────────────────────────────────────────────┘   │
      │                                                         │
      │   ┌─────────────────────────────────────────────────┐   │
      │   │        VPC Endpoint (S3 Gateway)                │   │
      │   └─────────────────────────────────────────────────┘   │
      └─────────────────────────────────────────────────────────┘
                      │
            ┌─────────▼──────────┐
            │  On-Prem (VPN)     │
            │  Customer Gateway  │
            └────────────────────┘

  ---

  ## 5. Hands-On Demo — Create VPC, Subnet, Route Table, IGW & NAT Gateway

  ### Step 1: Create a VPC

  ```bash
  # Using AWS CLI

  aws ec2 create-vpc \
    --cidr-block 10.0.0.0/16 \
    --tag-specifications 'ResourceType=vpc,Tags=[{Key=Name,Value=demo-vpc}]'

  Save the VpcId from the output (e.g., vpc-0abc123).

  ---
  Step 2: Enable DNS Hostnames on VPC

  aws ec2 modify-vpc-attribute \
    --vpc-id vpc-0abc123 \
    --enable-dns-hostnames

  ---
  Step 3: Create Subnets

  # Public Subnet (AZ: us-east-1a)
  aws ec2 create-subnet \
    --vpc-id vpc-0abc123 \
    --cidr-block 10.0.1.0/24 \
    --availability-zone us-east-1a \
    --tag-specifications 'ResourceType=subnet,Tags=[{Key=Name,Value=public-subnet}]'

  # Private Subnet (AZ: us-east-1b)
  aws ec2 create-subnet \
    --vpc-id vpc-0abc123 \
    --cidr-block 10.0.2.0/24 \
    --availability-zone us-east-1b \
    --tag-specifications 'ResourceType=subnet,Tags=[{Key=Name,Value=private-subnet}]'

  Save both subnet IDs (e.g., subnet-pub-111 and subnet-prv-222).

  ---
  Step 4: Create and Attach Internet Gateway

  # Create IGW
  aws ec2 create-internet-gateway \
    --tag-specifications 'ResourceType=internet-gateway,Tags=[{Key=Name,Value=demo-igw}]'

  # Attach IGW to VPC  (use your igw-id from above output)
  aws ec2 attach-internet-gateway \
    --internet-gateway-id igw-0xyz789 \
    --vpc-id vpc-0abc123

  ---
  Step 5: Create Public Route Table and Associate

  # Create Route Table
  aws ec2 create-route-table \
    --vpc-id vpc-0abc123 \
    --tag-specifications 'ResourceType=route-table,Tags=[{Key=Name,Value=public-rt}]'

  # Add route: all internet traffic → IGW
  aws ec2 create-route \
    --route-table-id rtb-0pub111 \
    --destination-cidr-block 0.0.0.0/0 \
    --gateway-id igw-0xyz789

  # Associate with Public Subnet
  aws ec2 associate-route-table \
    --route-table-id rtb-0pub111 \
    --subnet-id subnet-pub-111

  ---
  Step 6: Enable Auto-Assign Public IP on Public Subnet

  aws ec2 modify-subnet-attribute \
    --subnet-id subnet-pub-111 \
    --map-public-ip-on-launch

  ---
  Step 7: Create NAT Gateway (for Private Subnet)

  # Allocate an Elastic IP first
  aws ec2 allocate-address --domain vpc

  # Create NAT Gateway in the PUBLIC subnet with the EIP allocation
  aws ec2 create-nat-gateway \
    --subnet-id subnet-pub-111 \
    --allocation-id eipalloc-0aaa111 \
    --tag-specifications 'ResourceType=natgateway,Tags=[{Key=Name,Value=demo-nat-gw}]'

  Wait ~1 minute for NAT Gateway to become available.

  ---
  Step 8: Create Private Route Table and Associate

  # Create Private Route Table
  aws ec2 create-route-table \
    --vpc-id vpc-0abc123 \
    --tag-specifications 'ResourceType=route-table,Tags=[{Key=Name,Value=private-rt}]'

  # Add route: private subnet → NAT Gateway
  aws ec2 create-route \
    --route-table-id rtb-0prv222 \
    --destination-cidr-block 0.0.0.0/0 \
    --nat-gateway-id nat-0natxxx

  # Associate with Private Subnet
  aws ec2 associate-route-table \
    --route-table-id rtb-0prv222 \
    --subnet-id subnet-prv-222

  ---
  Final Architecture Summary

  You created:
    VPC            → 10.0.0.0/16
    Public Subnet  → 10.0.1.0/24 (AZ-1a)  ──► IGW ──► Internet
    Private Subnet → 10.0.2.0/24 (AZ-1b)  ──► NAT GW (in Public) ──► Internet
    IGW            → attached to VPC
    NAT GW         → in Public Subnet with Elastic IP
    Route Tables   → public-rt (IGW), private-rt (NAT GW)

  ---
  6. Quick Reference Cheat Sheet

  ┌──────────────────┬──────────────────────────────────────────────┬─────────────────┐
  │    Component     │                   Purpose                    │    Lives In     │
  ├──────────────────┼──────────────────────────────────────────────┼─────────────────┤
  │ VPC              │ Isolated virtual network                     │ Region          │
  ├──────────────────┼──────────────────────────────────────────────┼─────────────────┤
  │ Subnet           │ IP range inside VPC                          │ One AZ          │
  ├──────────────────┼──────────────────────────────────────────────┼─────────────────┤
  │ Route Table      │ Traffic routing rules                        │ VPC             │
  ├──────────────────┼──────────────────────────────────────────────┼─────────────────┤
  │ Router           │ Implicit traffic director                    │ VPC (automatic) │
  ├──────────────────┼──────────────────────────────────────────────┼─────────────────┤
  │ Internet Gateway │ VPC ↔ Internet                               │ VPC (attached)  │
  ├──────────────────┼──────────────────────────────────────────────┼─────────────────┤
  │ NAT Gateway      │ Private subnet → Internet (outbound only)    │ Public Subnet   │
  ├──────────────────┼──────────────────────────────────────────────┼─────────────────┤
  │ Elastic IP       │ Static public IP                             │ Account         │
  ├──────────────────┼──────────────────────────────────────────────┼─────────────────┤
  │ ENI              │ Virtual NIC for EC2                          │ Subnet          │
  ├──────────────────┼──────────────────────────────────────────────┼─────────────────┤
  │ Customer Gateway │ Represents your on-prem router in AWS        │ Account         │
  ├──────────────────┼──────────────────────────────────────────────┼─────────────────┤
  │ VPN Connection   │ Encrypted tunnel: on-prem ↔ VPC              │ VPC             │
  ├──────────────────┼──────────────────────────────────────────────┼─────────────────┤
  │ VPC Endpoint     │ Private access to AWS services (no internet) │ VPC             │
  ├──────────────────┼──────────────────────────────────────────────┼─────────────────┤
  │ VPC Peering      │ Private connectivity between two VPCs        │ VPC             │
  └──────────────────┴──────────────────────────────────────────────┴─────────────────┘

  ---
  Next Steps: Add Security Groups, NACLs, and deploy EC2 instances into your subnets!

  This gives you a complete, copy-paste ready README covering:
  - Region / AZ concepts with ASCII diagram
  - Full VPC architecture diagram
  - All 10 components explained with sub-diagrams
  - VPC Peering
  - Step-by-step CLI hands-on demo (Steps 1–8)
  - Quick reference cheat sheet
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


