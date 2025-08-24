# S3-File-Upload-Notification-System-Using-SNS


Overview
This project demonstrates an automated notification system using Amazon S3 and Amazon SNS. Whenever a new file is uploaded to a designated S3 bucket, Amazon SNS sends an email alert to subscribed users. This automation enhances visibility and removes the need for manual monitoring in file management workflows.

Objective
Send automated email notifications every time a new file is uploaded to a specified S3 bucket.

Improve workflow automation and visibility into file uploads.

AWS Services Used
Amazon S3 (Simple Storage Service)

Stores user-uploaded files.

Acts as the source for object creation events to trigger notifications.

Amazon SNS (Simple Notification Service)

Sends notifications via email (can also support SMS, HTTP).

Used to alert users/administrators about new uploads in the S3 bucket.

Architecture
File uploaded to S3 bucket.

S3 triggers an event for the object creation.

SNS topic receives the event and distributes notifications to email subscribers.

Setup Guide
Create an S3 bucket

Used to store files and generate upload events.

Create an SNS topic

Configure email subscriptions for recipients.

Set S3 Event Notification

Link the S3 bucket to the SNS topic for "ObjectCreated" events.

In S3 bucket: Properties > Event Notifications > Add Notification.

Verify email subscriptions

All endpoints must confirm subscription to receive notifications
