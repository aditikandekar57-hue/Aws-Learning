# Aws-Learning
## CloudWatch Monitoring – EC2

### Steps Performed
 Used EC2 default CloudWatch metrics
 Monitoring Setup

The following CloudWatch features were configured:

Service Used: AWS CloudWatch

Resource Monitored: EC2 Instance

Metric: CPUUtilization

Namespace: AWS/EC2

Statistic: Average

Period: 5 minutes

CloudWatch continuously collects metrics from the EC2 instance to monitor resource usage.

 Alarm Configuration
 A CloudWatch alarm was created with the following settings:

Alarm Name: EC2-CPU-Utilization-Alarm

Threshold: CPU Utilization > 70%

Evaluation Periods: 2 consecutive periods

Action: Trigger SNS notification

Alarm State: OK / ALARM (based on CPU load)

This alarm helps detect high CPU usage and prevents performance issues.

 Alerting with SNS

To receive alerts, Amazon SNS (Simple Notification Service) was integrated:

SNS Topic: CloudWatch-Alarms-Topic

Subscription Type: Email

Confirmation: Subscription confirmed via email

Once the alarm enters the ALARM state, an email notification is sent automatically.
 


### Screenshots
[EC2 Metrics](cloudwatch-ec2-metrics.png)
[CPU Alarm](cloudwatch-cpu-alarm.png)

