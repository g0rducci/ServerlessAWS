# AWS Lambda Foundations

Welcome to the AWS Lambda Foundations course. AWS Lambda is an event-driven, serverless compute service that lets you run code without provisioning or managing servers. This course focuses on what you need to start building Lambda functions and serverless applications. You will learn how AWS Lambda works and how to write and configure Lambda functions. You will explore deployment and testing considerations and end with a discussion on monitoring and troubleshooting Lambda functions.

By the end of this course, you should be able to do the following:

Define Lambda and describe how it works

     Describe the benefits of using Lambda and identify use cases

     Examine Lambda function permissions and security

     Demonstrate best practices for writing Lambda functions

     Deploy and test your serverless applications

     Explore Lambda configuration considerationsbullet

     Monitor and troubleshoot Lambda functions

# Introduction to Serverless

One of the major benefits of cloud computing is its ability to abstract (hide) the infrastructure layer. This ability eliminates the need to manually manage the underlying physical hardware. In a serverless environment, this abstraction allows you to focus on the code for your applications without spending time building and maintaining the underlying infrastructure. With serverless applications, there are never instances, operating systems, or servers to manage. AWS handles everything required to run and scale your application. By building serverless applications, your developers can focus on the code that makes your business unique.

# **Serverless operational tasks**

The following chart compares the deployment and operational tasks in a traditional environment to those in a serverless environment. The serverless approach to development reduces overhead and lets you focus, experiment, and innovate faster.

| Deployment and Operational tasks | Traditional Environment | Serverless |
| --- | --- | --- |
| Configure an instance | YES | - |
| Update operating system (OS) | YES | - |
| Install application platform | YES | - |
| Build and deploy apps | YES | YES |
| Configure automatic scaling and load balancing | YES | - |
| Continuously secure and monitor instances | YES | - |
| Monitor and maintain apps | YES | YES |

# **AWS serverless platform**

The AWS serverless platform includes a number of fully managed services that are tightly integrated with AWS Lambda and well-suited for serverless applications. Developer tools, including the AWS Serverless Application Model (AWS SAM), help simplify deployment of your Lambda functions and serverless applications.

Review the services in the following image. These services are part of the AWS serverless platform and are mentioned throughout the course.

AWS Lambda is the compute service for serverless. The AWS serverless platform includes a number of fully managed services that are tightly integrated with Lambda. There are also developer tools including AWS SAM to simplify deployment of your serverless applications.

![Untitled](AWS%20Lambda%20Foundations%20fca54763749744b8b8b7e4058e60d865/Untitled.png)

# **What is AWS Lambda?**

AWS Lambda is a compute service. You can use it to run code without provisioning or managing servers. Lambda runs your code on a high-availability compute infrastructure. It operates and maintains all of the compute resources, including server and operating system maintenance, capacity provisioning and automatic scaling, code monitoring, and logging. With Lambda, you can run code for almost any type of application or backend service.

Some benefits of using Lambda include the following:

- You can **run code** without provisioning or maintaining servers.
- It **initiates functions** for you in response to events.
- It **scales** automatically.
- It provides built-in code **monitoring and logging** via Amazon CloudWatch.

# **AWS Lambda features**

The following flashcards discuss the six main features of AWS Lambda. Use the arrow <> icons to shuffle through the cards. Select the **Click to flip** icon to read the details of each feature.

Front of card

![https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1680134400/IM8HPET8i9HhAL7Ai5QhGw/tincan/674187_1676990596_p1gpq6pq781l3ntaa1fcbps6c0t4_zip/assets/X2a2fuQa5GtHjs0c_m9HU2PGh3l--pKTs-Flashcard-1_NOPROCESS_.png](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1680134400/IM8HPET8i9HhAL7Ai5QhGw/tincan/674187_1676990596_p1gpq6pq781l3ntaa1fcbps6c0t4_zip/assets/X2a2fuQa5GtHjs0c_m9HU2PGh3l--pKTs-Flashcard-1_NOPROCESS_.png)

No image alternative text

Click to flip

Back of card

You can write the code for Lambda using languages you already know and are comfortable using. Development in Lambda is not tightly coupled to AWS, so you can easily port code in and out of AWS.

Click to flip

Front of card

![https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1680134400/IM8HPET8i9HhAL7Ai5QhGw/tincan/674187_1676990596_p1gpq6pq781l3ntaa1fcbps6c0t4_zip/assets/QKWZatNhwDNtauwd_olrAuITzYWo_Jkkq-Flashcard-2_NOPROCESS_.png](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1680134400/IM8HPET8i9HhAL7Ai5QhGw/tincan/674187_1676990596_p1gpq6pq781l3ntaa1fcbps6c0t4_zip/assets/QKWZatNhwDNtauwd_olrAuITzYWo_Jkkq-Flashcard-2_NOPROCESS_.png)

No image alternative text

Click to flip

Back of card

Within your Lambda function, you can do anything traditional applications can do, including calling an AWS SDK or invoking a third-party API, whether on AWS, in your datacenter, or on the internet.

Click to flip

Front of card

![https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1680134400/IM8HPET8i9HhAL7Ai5QhGw/tincan/674187_1676990596_p1gpq6pq781l3ntaa1fcbps6c0t4_zip/assets/apEopWjmR3CFzJnI_xCNv4kLYP89fnhJ5-Flashcard-3_NOPROCESS_.png](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1680134400/IM8HPET8i9HhAL7Ai5QhGw/tincan/674187_1676990596_p1gpq6pq781l3ntaa1fcbps6c0t4_zip/assets/apEopWjmR3CFzJnI_xCNv4kLYP89fnhJ5-Flashcard-3_NOPROCESS_.png)

No image alternative text

Click to flip

Back of card

Instead of scaling by adding servers, Lambda scales in response to events. You configure memory settings and AWS handles details such as CPU, network, and I/O throughput.

Click to flip

Front of card

![https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1680134400/IM8HPET8i9HhAL7Ai5QhGw/tincan/674187_1676990596_p1gpq6pq781l3ntaa1fcbps6c0t4_zip/assets/EqiC4_v0Cc2x966n_qCRT5qk03xg2JHh7-Flashcard-4_NOPROCESS_.png](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1680134400/IM8HPET8i9HhAL7Ai5QhGw/tincan/674187_1676990596_p1gpq6pq781l3ntaa1fcbps6c0t4_zip/assets/EqiC4_v0Cc2x966n_qCRT5qk03xg2JHh7-Flashcard-4_NOPROCESS_.png)

No image alternative text

Click to flip

Back of card

The Lambda permissions model uses AWS Identity & Access Management (IAM) to securely grant access to the desired resources and provide fine-grained control to invoke your functions.

Click to flip

Front of card

![https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1680134400/IM8HPET8i9HhAL7Ai5QhGw/tincan/674187_1676990596_p1gpq6pq781l3ntaa1fcbps6c0t4_zip/assets/siMOtnYh0JH4DJ2c_pdHNjUEECplE0syB-Flashcard-5_NOPROCESS_.png](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1680134400/IM8HPET8i9HhAL7Ai5QhGw/tincan/674187_1676990596_p1gpq6pq781l3ntaa1fcbps6c0t4_zip/assets/siMOtnYh0JH4DJ2c_pdHNjUEECplE0syB-Flashcard-5_NOPROCESS_.png)

No image alternative text

Click to flip

Back of card

Because Lambda is a fully managed service, high availability and fault tolerance are built into the service without needing you to perform any additional configuration.

Click to flip

Front of card

![https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1680134400/IM8HPET8i9HhAL7Ai5QhGw/tincan/674187_1676990596_p1gpq6pq781l3ntaa1fcbps6c0t4_zip/assets/tXsyoGa5kr8o108H_8-CpdcZFjBPUysLH-Flashcard-6_NOPROCESS_.jpg.png](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1680134400/IM8HPET8i9HhAL7Ai5QhGw/tincan/674187_1676990596_p1gpq6pq781l3ntaa1fcbps6c0t4_zip/assets/tXsyoGa5kr8o108H_8-CpdcZFjBPUysLH-Flashcard-6_NOPROCESS_.jpg.png)

No image alternative text

Click to flip

Back of card

Lambda functions only run when you initiate them. You pay only for the compute time that you consume. When the code is invoked, you are billed in 1-millisecond (ms) increments.

Click to flip

*1 of 6*

# **Event-driven architectures**

An event-driven architecture uses events to initiate actions and communication between decoupled services. An event is a change in state, a user request, or an update, like an item being placed in a shopping cart in an e-commerce website. When an event occurs, the information is published for other services to consume it. In event-driven architectures, events are the primary mechanism for sharing information across services. These events are observable, such as a new message in a log file, rather than directed, such as a command to specifically do something.

# **Producers, routers, consumers**

AWS Lambda is an example of an event-driven architecture. Most AWS services generate events and act as an event source for Lambda. Lambda runs custom code (functions) in response to events. Lambda functions are designed to process these events and, once invoked, may initiate other actions or subsequent events.

For more information on each piece of an event driven architecture, select each of the following numbered markers.

![Untitled](AWS%20Lambda%20Foundations%20fca54763749744b8b8b7e4058e60d865/Untitled%201.png)

# **What is a Lambda function?**

The code you run on AWS Lambda is called a *Lambda function*. Think of a function as a small, self-contained application. After you create your Lambda function, it is ready to run as soon as it is initiated. Each function includes your code as well as some associated configuration information, including the function name and resource requirements. Lambda functions are *stateless*, with no affinity to the underlying infrastructure. Lambda can rapidly launch as many copies of the function as needed to scale to the rate of incoming events.

After you upload your code to AWS Lambda, you can configure an event source, such as an Amazon Simple Storage Service (Amazon S3) event, Amazon DynamoDB stream, Amazon Kinesis stream, or Amazon Simple Notification Service (Amazon SNS) notification. When the resource changes and an event is initiated, Lambda will run your function and manage the compute resources as needed to keep up with incoming requests.

To learn more about the actions you can take with AWS Lambda, select each of the following markers:

Serverless provides speed and innovation in your business applications. To see how much you've learned, answer the following question.

![Untitled](AWS%20Lambda%20Foundations%20fca54763749744b8b8b7e4058e60d865/Untitled%202.png)