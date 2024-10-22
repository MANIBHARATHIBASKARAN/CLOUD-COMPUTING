# CLOUD-COMPUTING


### AWS Cloud Services: Step-by-Step Process

#### 1. **EC2 (Linux & Windows Instances)**

**Steps to Create and Manage EC2 Instances:**

- **Step 1**: Click on the **Server** option in the AWS Management Console.
- **Step 2**: Click on **EC2**.
- **Step 3**: Click on **Instances**.
- **Step 4**: Create a **Server Name**.
- **Step 5**: Select **Amazon Linux** as the operating system.

**For Key Pair Creation:**
- **Step 6**: Create a **Key Pair** with the following:
  - Create a **Key Pair Name**.
  - Choose **Key Pair Type**.
  - Choose the **Private Key File Format**.

**For Windows EC2 Instance Setup:**
- **Step 7**: Click on **Create Key Pair for Windows**.
- **Step 8**: Open **Remote Desktop Connection (RDC)**.
- **Step 9**: Enter your **User Name** and **Password**.
- **Step 10**: Retrieve the password by selecting **Get Password**.
- **Step 11**: Open **RDC** again to access the Windows instance.
- **Step 12**: Click **Add Roles and Features** to configure server roles.
- **Step 13**: Wait for the **Install Progress** to complete.
- **Step 14**: Test the server using the **default Test Page**.
- **Step 15**: Access the new web page via the **IP Address**.

**For Linux EC2 Instance Setup:**
- **Step 16**: Click on the **Linux Instance** and retrieve the **IP Address**.
- **Step 17**: Open **Putty** and enter the **ec-user** username.
- **Step 18**: Confirm the successful installation and access of the Linux server.
- **Step 19**: Start the **Apache server** to enable web hosting.
- **Step 20**: Open **WinSCP** to transfer files securely between your computer and the server.
- **Step 21**: Ensure the correct **path for downloads** is set up.
- **Step 22**: Confirm that **Linux runs successfully** and the web server is functional.

**Final Step**: **Terminate** the EC2 instances after the tasks are completed to avoid additional charges.


#### 2. **SQS (Simple Queue Service)**

**Steps to Create and Use SQS:**

- **Step 1**: Click on the **SQS** service in the AWS Console.
- **Step 2**: Click **Create SQS**.
- **Step 3**: Confirm that the **SQS service** is created successfully.
- **Step 4**: Send and receive messages in the queue.
- **Step 5**: Confirm that your message size is **17 bytes**.
- **Step 6**: Verify that the message is successfully **received** in the queue.



#### 3. **SNS (Simple Notification Service)**

**Steps to Set Up SNS Notifications:**

- **Step 1**: Create an **IAM Role** with the necessary permissions for SNS.
- **Step 2**: Navigate to **SNS** and create a topic by going to **Amazon SNS > Topics > EC2**.
- **Step 3**: Ensure that the **Subscription** is created successfully.
- **Step 4**: Confirm the subscription by clicking the link sent to your email.
- **Step 5**: Publish a **message** to the SNS topic.
- **Step 6**: Check your email to verify that you’ve received the SNS notification.
- **Step 7**: Create a new **EC2 instance** monitored by the SNS topic.
- **Step 8**: Monitor **14 metrics** for the EC2 instance.
- **Step 9**: Create an **alarm** for the EC2 instance and confirm that the alarm is displayed under “Alarms.”
- **Step 10**: Stop the EC2 instance to trigger the alarm.
- **Step 11**: Receive the **alarm notification** via email when the instance stops.


### 4. **Creating CloudFront (Content Delivery Network)**

**Step 1**: Log in to the **AWS Management Console**.
**Step 2**: In the search bar, type **CloudFront** and click on **CloudFront** under Services.
**Step 3**: Click **Create Distribution**.
**Step 4**: Select **Web** as the delivery method.
**Step 5**: Under **Origin Settings**, do the following:
- For **Origin Domain Name**, select the S3 bucket or custom origin (e.g., your website) that you want CloudFront to use as the source of the content.
- Set **Origin Path** if required.
- Leave the other fields as default unless you need specific settings for headers or cookies.
**Step 6**: Under **Default Cache Behavior Settings**:
- Set **Viewer Protocol Policy** to either **Redirect HTTP to HTTPS** or **HTTPS Only** for better security.
- Adjust **Cache Based on Selected Request Headers**, **Object Caching**, and other options depending on your caching strategy.
**Step 7**: Under **Distribution Settings**:
- Set the **Price Class** based on your geographic requirements.
- Enable **Logging** if you need detailed usage logs.
**Step 8**: Click **Create Distribution**.  
You will see the status as **In Progress**. Once it's deployed, you’ll receive a **CloudFront domain name** (e.g., `dxxxxxxxxxxx.cloudfront.net`) that you can use to access your content.



### 5. **Creating CloudFormation Stack**

**Step 1**: Log in to the **AWS Management Console**.
**Step 2**: In the search bar, type **CloudFormation** and click on **CloudFormation** under Services.
**Step 3**: Click **Create Stack**.
**Step 4**: Select the **Template Source**. You can either upload a **template file** from your computer or use an existing template from an **S3 URL**.
**Step 5**: Choose **Next**.
**Step 6**: Configure the **Stack Name** and provide **Parameter Values** (if required by the template).
**Step 7**: Under **Configure Stack Options**, you can add **Tags**, **Permissions**, and configure **Stack Policies** as needed.
**Step 8**: Review the configuration, then click **Create Stack**.
**Step 9**: CloudFormation will start creating the stack, deploying all the resources defined in the template. You can monitor the progress in the **Events** tab.

