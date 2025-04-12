## Script: List Logins with sysadmin Server Role

**Description**:
This script retrieves all SQL Server logins that are members of the built-in `sysadmin` server role. It includes login name, login type (SQL, Windows, etc.), and whether the login is disabled.

**What It Shows**:
- `name`: Login name
- `type_desc`: Login type (SQL login, Windows login, etc.)
- `is_disabled`: Whether the login is disabled (1 = Yes, 0 = No)

**Use Case**:
- Audit who has full administrative access to SQL Server
- Detect unexpected or unnecessary `sysadmin` logins
- Validate access before promoting or migrating environments

**Requirements**:
- SQL Server 2005 or later
- `VIEW SERVER STATE` or `sysadmin` permission

**Notes**:
- Uses the built-in `IS_SRVROLEMEMBER` function.
- If you want to find `sysadmin` **group members** at the Windows level, check via Active Directory or use extended tools like PowerShell or xp_logininfo.
