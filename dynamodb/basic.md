Understood, I'll keep the dataset simple.

## Lab 1: Introduction to Amazon DynamoDB and Creating Your First Table

### Objective
By the end of this lab, you will be familiar with the basic concepts of DynamoDB, and you will have created your first table.

### Prerequisites
- An AWS account
- Basic understanding of databases

### Background
Amazon DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability. DynamoDB lets you offload the administrative burdens of operating and scaling a distributed database so that you don't have to worry about hardware provisioning, setup and configuration, replication, software patching, or cluster scaling.

### Step 1: Sign into the AWS Management Console and Open the DynamoDB Console
- Navigate to the AWS Management Console and click `Sign In to the Console`.
- In the AWS Management Console, choose `Services` then select `DynamoDB` under `Database`.

### Step 2: Creating a DynamoDB Table
- In the DynamoDB dashboard, choose `Create table`.
- For `Table name`, enter `Students`.
- For `Primary key`, enter `student_id` and select `Number` for the key type.
- Leave the `Sort key` blank.
- Leave `Use default settings` selected and choose `Create`.

### Step 3: Populating the Table
- In the `Overview` tab of your new table, choose `Items`.
- Choose `Create item`.
- Fill in `student_id` with `1`.
- Choose `Append`, then `String` and add a new attribute `name` with value `John Doe`.
- Choose `Append`, then `Number` and add a new attribute `age` with value `20`.
- Choose `Save`.

We will use a simple dataset with the following fields for our `Students` table:

```json
{
    "student_id": 1,
    "name": "John Doe",
    "age": 20
}
```

### Step 4: Query the Table
- Choose `Start query`.
- In the `student_id` box, enter `1`, then choose `Start search`.
- Observe that your recently added item is returned.

### Step 5: Deleting the Table
- In the `Overview` tab of your table, choose `Delete table`.
- In the `Delete table` dialog box, choose `Delete`.

### Wrap up
This lab familiarized you with the basic concepts of DynamoDB. You created a table, added an item to it, queried for the item, and then deleted the table.

Let me know when you are ready for the next lab.