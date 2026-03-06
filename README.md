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

1. Basic Navigation Commands
Command	Description	Example
pwd	Print current working directory	pwd
ls	List files and directories	ls -l
cd	Change directory	cd /var/log
tree	Display directory structure	tree
pwd
ls -la
cd /etc
tree
2. File and Directory Management
Command	Description	Example
touch	Create empty file	touch file.txt
mkdir	Create directory	mkdir logs
cp	Copy files/directories	cp file.txt backup/
mv	Move or rename files	mv file.txt newfile.txt
rm	Delete files/directories	rm file.txt
mkdir project
touch app.log
cp app.log backup/
mv app.log app-old.log
rm app-old.log
3. File Viewing Commands
Command	Description	Example
cat	Display file content	cat file.txt
less	View large files	less logfile.log
head	View first lines	head -n 10 file.txt
tail	View last lines	tail -n 20 file.txt
tail -f	Follow live logs	tail -f app.log
cat config.yaml
less /var/log/syslog
tail -f application.log
4. Search and Text Processing
Command	Description	Example
grep	Search text in files	grep error app.log
find	Find files	find / -name file.txt
awk	Pattern scanning	awk '{print $1}' file.txt
sed	Stream editor	sed 's/old/new/g' file.txt
wc	Count lines/words	wc -l file.txt
grep ERROR app.log
find /var -name "*.log"
wc -l access.log
5. Process Management
Command	Description	Example
ps	Show running processes	ps aux
top	Monitor processes	top
htop	Interactive process viewer	htop
kill	Kill process	kill 1234
kill -9	Force kill process	kill -9 1234
ps aux | grep nginx
top
kill 4567
6. System Monitoring
Command	Description	Example
df	Disk usage	df -h
du	Directory size	du -sh /var/log
free	Memory usage	free -m
uptime	System uptime	uptime
vmstat	System performance	vmstat
df -h
free -m
du -sh *
uptime
7. Networking Commands
Command	Description	Example
ping	Test connectivity	ping google.com
curl	Test HTTP endpoints	curl http://localhost:8080
wget	Download files	wget https://example.com/file
netstat	Network connections	netstat -tulnp
ss	Socket statistics	ss -tulnp
ping 8.8.8.8
curl http://localhost:8080/health
ss -tulnp
8. Permissions and Ownership
Command	Description	Example
chmod	Change file permissions	chmod 755 script.sh
chown	Change ownership	chown ubuntu:ubuntu file.txt
whoami	Show current user	whoami
chmod +x deploy.sh
chown ec2-user:ec2-user app.log
9. Compression and Archiving
Command	Description	Example
tar	Archive files	tar -cvf archive.tar folder
tar -xvf	Extract archive	tar -xvf archive.tar
gzip	Compress file	gzip file.txt
gunzip	Decompress file	gunzip file.txt.gz
tar -cvf logs.tar logs/
tar -xvf logs.tar
gzip file.txt
10. Useful DevOps Commands
Command	Description
history	Show command history
watch	Run command repeatedly
crontab -l	View scheduled jobs
crontab -e	Edit cron jobs
history
watch df -h
crontab -l
11. Log Troubleshooting (Very Important for DevOps)
tail -f /var/log/syslog
tail -f /var/log/messages
journalctl -u nginx
journalctl -xe
Quick DevOps Troubleshooting Workflow
1. Check pod/server status
2. Check logs
3. Check CPU/Memory
4. Check disk usage
5. Check network connectivity

Example:

top
df -h
free -m
ping service
tail -f /var/log/app.log

If you want, I can also create a much better DevOps GitHub README like senior engineers use, including:

Kubernetes troubleshooting commands

Docker commands

SSH & server debugging

Disk cleanup

Real production debugging workflow

That version looks much more professional in GitHub repos and is great for training your students.


