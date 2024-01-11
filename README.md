# AWS cost optimization and remove unused resources

## Introduction

In this project,  I create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

## Services Used

* AWS Lambda
* Ec2
* EBS(Elastic Block Storage)
* EBS Snapshots

## Code

Using  Python language to run a code on Lambda function

## Description

The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.


