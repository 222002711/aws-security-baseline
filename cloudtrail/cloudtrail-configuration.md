# CloudTrail Configuration Overview

## Trail Name
christian-security-trail

## Purpose
This CloudTrail configuration captures all management API activity across all AWS regions. Logs are centrally stored in the logging bucket for auditing, compliance, and forensic analysis.

## Key Settings
- Trail type: Standard trail
- Multi-region: Yes
- Applied to AWS Organizations: No
- Log file SSE-KMS encryption: Disabled (SSE-S3 used by S3 bucket)
- Log file validation: Enabled (integrity protection)
- S3 log bucket: christian-security-baseline-logs
- S3 prefix: AWSLogs/<account-id>/
- Event types logged: Management events (Read and Write)
- Data events: Disabled
- Insights: Disabled
- Network activity events: Disabled

## Notes
This configuration aligns with NIST 800-53 controls for audit logging and log integrity, including AU-2, AU-3, and AU-9.
