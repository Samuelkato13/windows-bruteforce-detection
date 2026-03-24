```markdown
# Splunk Queries for Brute Force Detection

## 1. Failed Login Spike
```spl
index=* EventCode=4625
| stats count by Account_Name, Source_Network_Address
| sort -count

##2. Timeline 
```spl
index=* (EventCode=4625 OR EventCode=4624)
| transaction Account_Name Source_Network_Address maxspan=10m
| search eventcount>5
| table Account_Name, Source_Network_Address, eventcount, duration, _time
| sort - eventcount
