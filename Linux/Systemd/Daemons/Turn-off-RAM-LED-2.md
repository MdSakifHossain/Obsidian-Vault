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
→ rule exit
```

---
