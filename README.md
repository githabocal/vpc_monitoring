# VPC_Monitoring

- How do you monitor your VPC? --> VPC Flow logs
- 2(two) destination types --> S3 and CloudWatch
**_Note: Before you create flow log, make sure you have created s3 bucket and have ARN ready to use in flow log!_**


# <h3>Create flow log:
- Head to VPC and select the created `VPC` and choose `Flow logs` and click on `Create flow log`
- Then follow the steps stated below;
    - Set a name (ex: flowlog_to_s3)
    - Choose `1 minute` for `Maximum aggregation interval`
    - Choose `Send to Amazon S3 bucket` for `Destination`
    - Paste the `ARN` for `S3 bucket ARN` 
    - Choose `Every 1 hour(60 minutes)` for `Partition logs by time`
    - Then click on **`Create flow log`**
    - **_`Verify bucket policy has been attached to s3 bucket`_**

# <h3>CloudWatch(AWS monitoring tool):
- Head to `CloudWatch` in AWS and click on `Logs` dropdown on the left panel then click on **`Log groups`** then click on **`Create log group`**
- Set a log group name (ex: vpcflowlog) then click on **`Create`**
- 