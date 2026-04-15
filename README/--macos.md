# Developer Onboarding README

## Welcome to Melbournedevelopments.com.au

Welcome to the team. This guide will help you securely access the company VPS and begin your development setup.

---

## Important Security Notice

For security reasons, **SSH usernames, server addresses, passwords, and login credentials are never shared through documentation, chat, or email**.

Your access has already been **securely pre-provisioned on your company machine**.

You should already have:

* Required access permissions assigned
* Your temporary login credential securely stored in `~/env`
* Terminal access ready to use

If access is missing, contact the internal administrator.

---

## Step 1: Connect to the Company VPS

Use the command below exactly as provided:

```bash
sshpass -p "$(cat ~/env)" ssh root@172.105.162.155
```

This command will:

* Read your temporary password from `~/env`
* Authenticate to the VPS
* Start your first login session

---

## Step 2: Mandatory Password Change on First Login

For security compliance, **your first successful login will automatically prompt you to change your password immediately**.

You must complete this step before continuing.

Typical prompts may look like:

```bash
Current password:
New password:
Retype new password:
```

Choose a strong password that meets company security standards:

* Minimum 14 characters
* Uppercase + lowercase letters
* Numbers
* Symbols
* Not used elsewhere

> Save your new password in the approved company password manager.

---

## Step 3: Confirm Successful Login

Once connected and password updated, run:

```bash
whoami
hostname
pwd
```

You should now be inside the Melbournedevelopments.com.au development environment.

---

## Step 4: Next Setup Tasks

After connecting:

* Pull latest repositories
* Install dependencies
* Configure environment files
* Start development services
* Review internal documentation

---

## Troubleshooting

### sshpass not installed

Install it first:

```bash
sudo apt install sshpass
```

or on macOS:

```bash
brew install hudochenkov/sshpass/sshpass
```

### Connection refused / timeout

The server may be restricted by firewall or VPN.

### Authentication failed

Contact the internal administrator for reprovisioning.

---

## Security Rules

Never share:

* Temporary credentials
* Root access details
* Your new password
* Internal infrastructure details

All access is provisioned directly onto approved company devices only.

---

## Welcome Aboard

You’re ready to begin building with Melbournedevelopments.com.au 🚀
