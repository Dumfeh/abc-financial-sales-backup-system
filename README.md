# AWS S3 Company Backup System

## Project Overview

This project demonstrates how Amazon S3 Versioning can be used to protect business files from accidental deletion or overwriting.

## Business Case

ABC Financial Services needed a reliable cloud storage solution to ensure previous versions of important reports could be recovered whenever mistakes occurred.

## AWS Services

- Amazon S3
- S3 Versioning

## Implementation Progress

### Step 1: Created Amazon S3 Bucket

A private S3 bucket was created to store company backup files.

### Step 2: Uploaded Company Reports

Sample financial reports were uploaded:

- January Sales Report
- February Sales Report
- March Sales Report

These files simulate business documents that require secure cloud backup.

## Data Loss Simulation

Before enabling S3 Versioning, I simulated an accidental file overwrite scenario.

Original file:

January-Sales-Report.txt

Original revenue:

$25,000


A new incorrect version was uploaded with:

Revenue: $0


Because Versioning was disabled, the previous file version could not be recovered.

This demonstrates the importance of backup strategies in cloud environments.

## Enabling Amazon S3 Versioning

Versioning was enabled on the S3 bucket to protect company reports from accidental overwrites.

After enabling Versioning:

- Every upload creates a new object version.
- Previous versions remain stored.
- Each version receives a unique Version ID.
- Business files can be recovered if mistakes occur.

This feature is commonly used in production environments to improve data durability and support disaster recovery.

## Recovering Deleted Files with S3 Versioning

To test Amazon S3 Versioning, I simulated the accidental deletion of the January Sales Report.

Although the file appeared to be deleted, Amazon S3 created a Delete Marker instead of permanently removing the object.

By deleting the Delete Marker, I successfully restored the latest version of the report without using an external backup.

### Key Learning

S3 Versioning protects business data from accidental deletions by preserving previous object versions and allowing rapid recovery.

## Cost Optimization with Amazon S3 Lifecycle Policies

To reduce long-term storage costs, I created an Amazon S3 Lifecycle Rule that automatically transitions objects from the S3 Standard storage class to S3 Glacier Instant Retrieval after 30 days.

### Business Value

This automation reduces storage costs while ensuring that older company reports remain securely stored and can still be retrieved when needed.