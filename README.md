AWS Security Baseline Project

This project demonstrates the implementation of a cloud security baseline using AWS services, aligned with security best practices and mapped to NIST 800-53 controls. It includes S3 hardening, IAM least-privilege configurations, CloudTrail auditing, access logging, and governance documentation. The goal is to showcase hands-on GRC, cloud security, and architecture skills in a real-world style project.

Project Overview

This repository contains a structured, end-to-end AWS security baseline designed to:

Secure cloud storage (S3)

Enforce least-privilege IAM policies

Enable auditing and traceability (CloudTrail)

Capture access logs for accountability

Map implemented settings to NIST 800-53 controls

Document risks, mitigations, and governance decisions

This reflects the type of work performed by GRC Analysts, Cloud Security Analysts, and Security Engineers.

Architecture Summary

The baseline includes the following components:

1. Secure S3 Bucket

Versioning enabled

Default encryption (SSE-S3 / AES-256)

Public access fully blocked

Server access logging enabled

Logs delivered to a separate logging bucket

2. Logging Bucket

Stores S3 access logs

Stores CloudTrail logs (once configured)

Versioned and encrypted

3. IAM Least-Privilege Role

A custom IAM policy restricting access only to:

s3:ListBucket

s3:GetObject

Scope is limited to the main S3 bucket.

4. CloudTrail Auditing (pending)

Logs all API activity

Log file validation will be enabled

Logs stored in the logging bucket

Repository Structure
aws-security-baseline/
│
├── README.md
│
├── iam/
│   ├── least-privilege-policy.json
│   └── role-description.md
│
└── s3/
    (Will include bucket policy documentation, encryption configs, and access logging notes)


More directories will be added as the project progresses, including:

cloudtrail/

nist-control-mapping/

risk-register/

Security Controls Implemented
Control	Description	Status
AC-6	Least Privilege	Implemented
SC-13	Cryptographic Protection	Implemented
SC-28	Data at Rest Protection	Implemented
AU-2	Auditable Events	Implemented
AU-9	Log Integrity	Pending
AC-3	Access Enforcement	Implemented
Tools and Technologies

AWS S3

AWS IAM

AWS CloudTrail

NIST 800-53

GitHub

Purpose of This Project

The project demonstrates practical skills in the following areas:

Cloud security fundamentals

Governance, risk, and compliance

Documentation and architectural decision-making

Policy writing and access control

Audit and monitoring configuration

Framework alignment (NIST 800-53)

This project is intended for GRC internships, Cloud Security internships, entry-level Security Analyst roles, and students gaining exposure to cloud governance.

Project Roadmap

Completed:

S3 secure bucket

Logging bucket

Encryption and versioning

IAM least-privilege policy

Initial repository structure

Upcoming:

CloudTrail configuration

NIST control mapping spreadsheet

Risk register creation

Architecture diagram

Audit summary report

The README will be updated as the project progresses.

Author

Christian Anderson
Cybersecurity student at Purdue University Indianapolis
Security+ certified
Focused on GRC, cloud security, and threat modeling
