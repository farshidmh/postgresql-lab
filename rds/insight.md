Lab: Amazon RDS Performance Insights

## Introduction

Amazon RDS Performance Insights is a powerful feature that enables you to analyze the performance of your Amazon RDS instances. It provides detailed information on database load and query performance, helping you identify and troubleshoot performance issues effectively.

## Prerequisites

Before you begin, make sure you have the following:

- An AWS account with the necessary permissions to create and manage Amazon RDS instances.
- The AWS Command Line Interface (CLI) installed on your local machine.

## Sample Dataset

To conduct the lab exercises, we will use a sample dataset with a table named `sales_data` in the MySQL RDS instance. Here's the SQL script to create the table and insert some sample data:

```sql
CREATE TABLE sales_data (
    id INT AUTO_INCREMENT PRIMARY KEY,
    product VARCHAR(50),
    quantity INT,
    price DECIMAL(10, 2)
);

INSERT INTO sales_data (product, quantity, price) VALUES
    ('Product A', 10, 50.00),
    ('Product B', 15, 30.00),
    ('Product C', 5, 75.00),
    ('Product A', 20, 48.50),
    ('Product B', 12, 28.75);
```

## Steps

### Step 1: Create an Amazon RDS DB Instance

1. Open the AWS Management Console and sign in to your AWS account.
2. Navigate to the **Amazon RDS** service.
3. Click on the **Create database** button.
4. Choose **Standard Create** as the creation method.
5. Select the **Engine type** you want to use (e.g., MySQL, PostgreSQL, etc.).
6. In the **Templates** section, choose Dev/Test and **Availability and durability** to Single instance.
7. Configure the **Settings** for your database:
    - **DB instance identifier**: Enter a unique name for your RDS instance.
    - **Master username**: Choose a master username for the database.
    - **Master password**: Enter a secure password for the master user.
    - **DB instance class**: Choose the compute and memory capacity for your instance.
    - **Storage type**: Select the storage type (e.g., General Purpose, Provisioned IOPS).
    - **Allocated storage**: Set the amount of storage you need for your database.
8. Scroll down and configure any additional settings as per your requirements.
9. Click on the **Create database** button to create the RDS instance.

### Step 2: Enable Performance Insights

1. In the AWS Management Console, navigate to the **Amazon RDS** service.
2. Select the RDS instance you created in Step 1.
3. Click on the **Modify** button.
4. Scroll down to the **Performance Insights** section.
5. Enable **Enable Performance Insights**.
6. Optionally, adjust the **Data retention period**. The default is 7 days.
7. Click on **Continue** and then **Modify DB Instance** to apply the changes.

### Step 3: View Performance Insights Metrics

1. After enabling Performance Insights, wait for some time (usually a few minutes) to gather performance data.
2. In the AWS Management Console, navigate to the **Amazon RDS** service.
3. Select the RDS instance you created.
4. Click on the **Performance insights** tab.
5. Explore the various metrics and graphs available, such as **Database load**, **Active sessions**, **Top SQL**, etc.
6. Use the graphs to analyze database performance over time and identify any performance bottlenecks.

### Step 4: Analyze Top SQL Queries

1. In the Performance Insights tab, scroll down to the **Top SQL** section.
2. View the top SQL queries sorted by various metrics like CPU, data reads, and data writes.
3. Click on a specific SQL query to see its detailed performance metrics.

### Step 5: Clean Up

1. To avoid incurring additional costs, make sure to delete the RDS instance when you're done experimenting.
2. In the AWS Management Console, navigate to the **Amazon RDS** service.
3. Select the RDS instance you created.
4. Click on the **Instance actions** dropdown and choose **Delete**.
5. Follow the on-screen instructions to confirm the deletion.

## Conclusion

Congratulations! You have successfully learned how to enable Amazon RDS Performance Insights to monitor and analyze the performance of your RDS instances. Performance Insights provides valuable insights into database performance, helping you identify and resolve performance-related issues. Don't forget to clean up the resources to avoid unnecessary costs.