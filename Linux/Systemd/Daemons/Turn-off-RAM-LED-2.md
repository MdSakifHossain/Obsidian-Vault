# Automatically Turn Off RAM LED

⬅️ [Systemd](../Systemd.md)

You can automate what would normally require human interaction.

---

## How It Works

**Event:** User logs in

**Action:** Wait 5 seconds

**Then:** Run `openrgb --mode static --color 000000`

```
system boots
→ login succeeds
→ user session starts
→ systemd (user) activates default target
→ your rule is triggered
→ wait 5 seconds
→ openrgb --mode static --color 000000
→ LEDs turn off
```

---
## Before You Automate: Test It Manually

The manual flow:

```
system boots → login → terminal → command → RGB off
```

I'm using **[OpenRGB](https://openrgb.org/)** for this.

### Check Your OpenRGB Version

```sh
❯ openrgb --version
OpenRGB 0.9+ (1.0rc2), for controlling RGB lighting.
  Version:		 0.9+ (1.0rc2)
  Build Date		 Mon, 13 Apr 2020 03:57:34 +0000
  Git Commit ID		 0fca93e4544f943d4d7ec8073dba4e47c18ef54b
  Git Commit Date	 2025-09-14 14:31:57 -0500
  Git Branch		 2039027121 2039027252 master
```

### Test the Command

```sh
❯ openrgb --mode static --color 000000
Connection attempt failed
[i2c_smbus_linux] Failed to read i2c device PCI device ID
[i2c_smbus_linux] Failed to read i2c device PCI device ID
[i2c_smbus_linux] Failed to read i2c device PCI device ID
```

**Chill.** This is not an error. The motherboard is a ghost device. But the **RAM LEDs** got shut down.

This also works **without** `sudo`. So, we are **golden**.

---

## The Automation

This step is mechanical, not conceptual:

- Create a user-level systemd service
- Tell it to start on login
- Add the 5-second delay
- Put your already-working command inside

No new ideas. No new behavior.

---
