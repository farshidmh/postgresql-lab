# Lab: Basics of Amazon RDS

## Introduction

Amazon RDS is a managed relational database service provided by AWS that simplifies the setup, operation, and scaling of relational databases in the cloud. In this lab, you will learn how to create an Amazon RDS instance and perform basic database operations.

## Prerequisites

- An AWS account with appropriate permissions to create resources like RDS instances.
- The AWS Command Line Interface (CLI) installed on your local machine.

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

### Step 2: Wait for the Database to Be Available

1. After creating the RDS instance, wait for it to be in the **available** state. This may take a few minutes.

2. Once the status is **available**, note down the **Endpoint** URL. This will be used to connect to the database.

### Step 3: Connect to the RDS Instance

1. Open your terminal or command prompt.

2. Use the AWS CLI to connect to the RDS instance using the following command (replace `<ENDPOINT>` with your actual Endpoint URL):

   ```bash
   mysql -h <ENDPOINT> -u <MASTER_USERNAME> -p
   ```

3. Enter the master password when prompted.

4. If successful, you should now be connected to the RDS database.

### Step 4: Perform Basic Database Operations

1. Once connected to the database, create a new database by executing the following SQL command:

   ```sql
   CREATE DATABASE mydb;
   ```

2. Switch to the newly created database:

   ```sql
   USE mydb;
   ```

3. Create a new table in the database:

   ```sql
   CREATE TABLE users (
       id INT AUTO_INCREMENT PRIMARY KEY,
       name VARCHAR(50),
       email VARCHAR(100)
   );
   ```

4. Insert some data into the table:

   ```sql
   INSERT INTO users (name, email) VALUES
       ('John Doe', 'john@example.com'),
       ('Jane Smith', 'jane@example.com');
   ```

5. Query the data from the table:

   ```sql
   SELECT * FROM users;
   ```

6. You should see the data you inserted displayed in the query result.

### Step 5: Clean Up

1. To avoid incurring additional costs, make sure to delete the RDS instance when you're done experimenting.

2. In the AWS Management Console, navigate to the **Amazon RDS** service.

3. Select the RDS instance you created.

4. Click on the **Instance actions** dropdown and choose **Delete**.

5. Follow the on-screen instructions to confirm the deletion.

## Conclusion

Congratulations! You have successfully learned the basics of Amazon RDS, including creating an RDS instance, connecting to it, and performing basic database operations. Remember to delete your RDS instance to avoid unnecessary costs.