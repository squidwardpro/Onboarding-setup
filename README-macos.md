# Developer Onboarding README

## Melbournedevelopments.com.au

## Security Notice

SSH usernames, hostnames, IP addresses, private keys, and login credentials are **not shared in documentation, chat, or email**.

Your access has already been pre-provisioned on your company device.

If access is missing, contact the administrator.

---

## 1. Retrieve Passphrase

The local passphrase is stored on your machine:

```bash
~/env
```

View it:

```bash
cat ~/env
```

Use this when prompted during login.

---

## 2. Connect to the VPS

Use the assigned host or configured alias:

```bash
ssh <assigned-host>
```

Example:

```bash
ssh company-vps
```

On first connection:

* Accept the host fingerprint if prompted
* Enter the passphrase from `~/env`

---

## 3. Change Password Immediately

On first login, the system will force a password change.

Complete the prompts:

```bash
Current password:
New password:
Retype new password:
```

Use a strong password and store it in the approved password manager.

---

## 4. Verify Access

Run:

```bash
whoami
hostname
pwd
```

---

## 5. Next Steps

* Clone required repositories
* Install dependencies
* Configure environment files
* Start services
* Review internal docs

---

## Troubleshooting

### Permission denied (publickey)

Provisioned key missing or incorrect. Contact administrator.

### Connection refused / host unreachable

VPN may be required or host details may have changed.

### Incorrect passphrase

Recheck:

```bash
cat ~/env
```

---

## Security Rules

Do not share:

* SSH access details
* Private keys
* Passphrases
* Passwords
* Internal hostnames
* Production access information
