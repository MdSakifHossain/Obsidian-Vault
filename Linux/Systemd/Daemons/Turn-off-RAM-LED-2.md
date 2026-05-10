# Automatically Turn Off RAM LED

⬅️ [Systemd](../Systemd.md)

You can automate what would normally require human interaction.

---

## How It Works

**Event:** User logs in
**Action:** Wait 5 seconds
**Then:** Run `openrgb --mode off`

```
system boots
→ login succeeds
→ user session starts
→ systemd (user) activates default target
→ your rule is triggered
→ wait 5 seconds
→ openrgb --mode off
→ LEDs turn off
→ rule exits
```

---
