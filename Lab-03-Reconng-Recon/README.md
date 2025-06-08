# ✅ Lab 03: Reconnaissance using Recon-ng Framework

## 🎯 Objective

Perform passive reconnaissance and footprinting on a target domain using the Recon-ng framework.

## 🛠 Tools Used

- Recon-ng
- Nmap (for setup)
- Git, Python, Curl (dependencies)

## 🔄 Task Summary

- Install Recon-ng and dependencies.
- Load and run reconnaissance modules (e.g., hackertarget).
- Collect subdomains, IPs, and host data.

## 🧪 Steps

### 🔹 Step 1: Install Recon-ng

```bash
sudo apt update
sudo apt install -y python3 python3-pip git nmap curl
git clone https://github.com/lanmaster53/recon-ng.git
cd recon-ng
pip install -r REQUIREMENTS
./recon-ng
```

### 🔹 Step 2: Use the hackertarget module inside Recon-ng

```bash
marketplace install hackertarget
modules load hackertarget
options set SOURCE tesla.com
run
show hosts
```

## 👀 Observations

- Recon-ng automates OSINT-based reconnaissance.
- Provides CLI experience similar to Metasploit.
- Useful for collecting domain info before active testing.

## ✅ Expected Output

- List of discovered subdomains, IPs, and other passive intel about the target domain.
- Structured output in Recon-ng workspace.
