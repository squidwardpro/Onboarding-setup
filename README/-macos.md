
# Melbournedevelopments.com.au VPS Access

## Login

SSH access is pre-provisioned on your company machine.

Do not copy, export, or share credentials.

Run:

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa < ~/env
ssh root@172.105.162.155
```

This will:

* start `ssh-agent`
* load your SSH key using the passphrase stored in `~/env`
* connect to the VPS without manually pasting the passphrase

This avoids entering the SSH key passphrase directly into your terminal.

---

## First Login

On first login, you will be required to change your password.

You will see prompts like:

```bash
Current password:
New password:
Retype new password:
```

Complete that step before doing anything else.

---

## Verify Access

After login:

```bash
whoami
hostname
pwd
```

---

## Troubleshooting

If the key file is different from `~/.ssh/id_rsa`, replace it with the correct path.

Example:

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/<your-key-name> < ~/env
ssh root@172.105.162.155
```

If access fails, provisioning may be incomplete. Contact admin.

---

## Security

Do not share:

* `~/env`
* SSH private keys
* server credentials
* internal access details

If you want, I can turn this into a polished full README block with proper markdown headings and a short prerequisites section.
