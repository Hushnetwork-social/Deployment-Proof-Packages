# FEAT-162 Reviewer Guide

Source id: `DEPLOYMENT-ROLLBACK-REHEARSAL-v0.1.0`

Validate without writes:

```powershell
cd hush-server-node
powershell -ExecutionPolicy Bypass -File Node/scripts/promote-deployment-rollback-rehearsal.ps1 -WorkspaceRoot C:\myWork\HushNetworkOrg -Mode validate-only
```

Generate package:

```powershell
cd hush-server-node
powershell -ExecutionPolicy Bypass -File Node/scripts/promote-deployment-rollback-rehearsal.ps1 -WorkspaceRoot C:\myWork\HushNetworkOrg -Mode package
```

Check generated package:

```powershell
cd hush-server-node
powershell -ExecutionPolicy Bypass -File Node/scripts/promote-deployment-rollback-rehearsal.ps1 -WorkspaceRoot C:\myWork\HushNetworkOrg -Mode check-only
```

Public-only validation for CI:

```powershell
cd hush-server-node
powershell -ExecutionPolicy Bypass -File Node/scripts/promote-deployment-rollback-rehearsal.ps1 -WorkspaceRoot C:\myWork\HushNetworkOrg -Mode check-only -PublicOnly
```
