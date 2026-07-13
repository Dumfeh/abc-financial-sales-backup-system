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