
---

### **splunk_queries.md (Day 2)**

```markdown
# Splunk Queries – Day 2 Privilege Escalation

## 1. Detect admin privilege assignment
```spl
index=* sourcetype="WinEventLog:Security" (EventCode=4672 OR EventCode=4728 OR EventCode=4732)
| table _time, Account_Name, EventCode, host
