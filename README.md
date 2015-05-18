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

## 3. Setting up Java Receiver

> **[Download](https://drive.google.com/file/d/0BxLqTramfZucOGFDVkdLQmdDNHM/view?pli=1) Receiver.war file here.**

> **We need to make changes to the following files for setting up Receiver in Tomcat.**

> **Make these changes in the Receiver.war file <b>without extracting</b>.**

+ `AWSCredentials.properties` - Provide the AWS Credentials (Access Key Id and Secret Access Key)	
+ `whoami.txt` - Enter your name and Bits ID	
+ `web.xml` - Provide the Queue `URL`

> **Navigate to Elastic Beanstalk.**

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7673732/b6abe124-fd36-11e4-996c-0349b12b9103.jpg)

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7674896/8e985114-fd4e-11e4-88f3-0ccc7ff4e2c0.jpg)

***

> **Provide a name for the application.**

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7673723/b67a90ec-fd36-11e4-899b-b3b77ecc06a2.jpg)

***

> **Create a new Web Server.**

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7673725/b68500cc-fd36-11e4-9307-11e8f3a42fbd.jpg)

***

> **Choose a default profile.**

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7673724/b67c4a86-fd36-11e4-8898-8cda33e8bfff.jpg)

***

> **Choose an enviroment type.**

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7673726/b68a289a-fd36-11e4-850e-5483af72ea67.jpg)

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7673728/b693dd22-fd36-11e4-9160-fb11498a2074.jpg)

***

> **Upload your zip file.**

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7673729/b69cd3c8-fd36-11e4-9a21-2bb4e3a9666e.jpg)

***

> **Provide an environment URL.**

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7673730/b6a13d8c-fd36-11e4-88d2-231f194e78df.jpg)

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7673731/b6a5909e-fd36-11e4-9e4a-b8e128eb58dd.jpg)

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7673733/b6b7315a-fd36-11e4-8ea4-68dbb3e515bc.jpg)

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7673727/b690f6b6-fd36-11e4-9ae1-fe0724576e4a.jpg)

***

> **Click on launch to launch your enviroment and be patient as it takes some time to initialize the environment.**

***

## 4. Setting up NodeJs Sender

> **We need to make changes to the following files for setting up NodeJs**

+ `aws.credentials.json` - Provide the AWS Credentials (Access Key Id and Secret Access Key)
+ `whoami.txt` - Enter your name and Bits ID
+ `sqsendpointdetails.txt` - Provide the Queue `URL`

<b>Make sure you are compressing the 5 files without placing it in a folder. In case there is a folder named `node_modules` delete it before uploading.</b>

> **Follow the same steps similar to the previous application till choosing an environment**

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7673721/b64fe6f8-fd36-11e4-8e33-518557df4e87.jpg)

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7673728/b693dd22-fd36-11e4-9160-fb11498a2074.jpg)

***

> **Follow the steps as specified for the previous application**
