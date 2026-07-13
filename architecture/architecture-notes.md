# AWS S3 Company Backup System Architecture

## Overview

This solution provides a secure cloud backup system for ABC Financial Services.

Business reports are uploaded into Amazon S3.

Amazon S3 Versioning protects files from accidental deletion and overwriting.

Lifecycle Policies automatically transition older reports into Amazon S3 Glacier Instant Retrieval to reduce storage costs.

## Components

### User

Cloud Engineer responsible for uploading and managing reports.

### Amazon S3

Stores all company reports securely.

### Amazon S3 Versioning

Maintains previous versions of objects.

### Lifecycle Policy

Automatically moves older reports into cheaper storage.

### Amazon S3 Glacier Instant Retrieval

Stores archived reports at a lower cost while remaining retrievable.