# 🧹 AWS Cloud Cost Optimization - Identifying Stale EBS Snapshots

This AWS Lambda function helps **optimize your AWS cloud storage costs** by identifying and deleting **stale EBS snapshots** that are no longer associated with any **active EC2 instances** (either running or stopped).

## 📌 Overview

Amazon EBS snapshots can accumulate over time, especially when instances or volumes are terminated. These unused snapshots continue to incur costs if not manually managed.

This Lambda function:
- Retrieves all **EBS snapshots** owned by the AWS account.
- Gathers all active EC2 instances (both `running` and `stopped`).
- Checks if each snapshot is associated with a volume that belongs to any active instance.
- **Deletes stale snapshots** that are no longer linked to any active EC2 instance or the volume.

## 🚀 Features

- ✅ Identifies unused EBS snapshots
- 🔄 Automates snapshot cleanup
- 💸 Reduces unnecessary AWS storage costs
- ☁️ Serverless and lightweight (AWS Lambda)


