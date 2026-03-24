```markdown
# Windows Brute Force Detection - Attack Steps

1. **Prepare Target:**
   - Windows VM with Administrator account
   - Ensure Security logging enabled
   ```bash
   auditpol /set /category:"Logon/Logoff" /success:enable /failure:enable
