# aws-eb-sqs

Instructions for setting up Sender and Receiver Application in Amazon Web Service Elastic Beanstalk and making those two applications communicate using Simple Queue Service
. 

*[Assignment link.](https://github.com/prabhu-durasoft/ECIII)*

**Instructions are divided as follows,**

## How-to ?

- Create AWS Credentials
- Create an SQS Queue
- Setting up Java Receiver
- Setting up NodeJs Sender

## 1. Creating AWS Credentials

> **Navigate to Security Credentials Page.**

> **Click Users Tab.**

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7671384/3084aa90-fceb-11e4-9af9-3dd8902717fd.jpg)

***

> **Click on Create New Users, and type in the user name**

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7671387/31317b4e-fceb-11e4-9551-a13fee233633.jpg)

***

> **You will be prompted given an Access Key Id and Secret Access Key. We will be using these keys in out sender and** **receiver application.**

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7671386/309c8a7a-fceb-11e4-9ed8-6c3188f73209.jpg)




***




## 2. Creating an SQS Queue

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7671382/307335d0-fceb-11e4-9203-2debb6db9612.jpg)

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7671381/306ee926-fceb-11e4-8d36-9fac88a060bf.jpg)



***



> **Adding Permission.**

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7671383/307ba620-fceb-11e4-8e3c-92391a9ad731.jpg)



***



> **Choosing options.**

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7671385/30887cd8-fceb-11e4-8134-cc2235d5abe3.jpg)



***



> **Your Queue `URL` will be available in the details tab. We will be using this `URL` for communication.**




***




## 4. Setting up Java Receiver

> [Download](https://drive.google.com/file/d/0BxLqTramfZucOGFDVkdLQmdDNHM/view?pli=1) Receiver.war file here.

> We need to make changes to the following files for setting up Receiver in Tomcat.

> Make these changes in the Receiver.war file without extracting.

+ `AWSCredentials.properties` - Provide the AWS Credentials (Access Key Id and Secret Access Key)	
+ `whoami.txt` - Enter your name and Bits ID	
+ `web.xml` - Provide the Queue `URL`




***




## 3. Setting up NodeJs Sender

> We need to make changes to the following files for setting up NodeJs

+ `aws.credentials.json` - Provide the AWS Credentials (Access Key Id and Secret Access Key)
+ `whoami.txt` - Enter your name and Bits ID
+ `sqsendpointdetails.txt` - Provide the Queue `URL`
