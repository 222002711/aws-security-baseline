# IAM Least Privilege Role

## Role Name
christian-s3-readonly-role

## Purpose
This role grants read-only access to the `christian-security-baseline-main` S3 bucket according to least-privilege best practices.

## Attached Policy
- christian-least-privilege-s3-readonly

## Key Permissions
- s3:ListBucket
- s3:GetObject

## Security Notes
- No write, delete, or modify permissions granted.
- Policy scope is restricted to a single bucket and no wildcard access.
