
---

### **attack_steps.md (Day 2)**

```markdown
# Day 2 – Privilege Escalation Attack Steps

1. Use the compromised user from Day 1 (`hacker`).
2. Open CMD as Admin.
3. Run:
```bat
net localgroup administrators hacker /add
