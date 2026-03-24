```markdown
# Splunk Queries for Brute Force Detection

## 1. Failed Login Spike
```spl
index=* EventCode=4625
| stats count by Account_Name, Source_Network_Address
| sort -count
