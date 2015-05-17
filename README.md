# aws-eb-sqs

Instructions for setting up Sender and Receiver Application in Amazon Web Service Elastic Beanstalk and making those two applications communicate using Simple Queue Service
. 

*[Assignment](https://github.com/prabhu-durasoft/ECIII)*

**Instructions are divided as follows,**

## How-to ?

- Create AWS Credentials
- Create an SQS Queue
- Setting up NodeJs Sender
- Setting up Java Receiver

## Create AWS Credentials

> *Navigate to Security Credentials Page.*

> *Click Users Tab.8

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7671384/3084aa90-fceb-11e4-9af9-3dd8902717fd.jpg)

> *Click on Create New Users, and type in the user name*

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7671387/31317b4e-fceb-11e4-9551-a13fee233633.jpg)

> *You will be prompted given an Access Key Id and Secret Access Key. We will be using these keys in out sender and receiver application.*

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7671386/309c8a7a-fceb-11e4-9ed8-6c3188f73209.jpg)


## Create an SQS Queue

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7671382/307335d0-fceb-11e4-9203-2debb6db9612.jpg)

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7671381/306ee926-fceb-11e4-8d36-9fac88a060bf.jpg)

> *Adding Permission.*

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7671383/307ba620-fceb-11e4-8e3c-92391a9ad731.jpg)

> *Choosing options.*

![screenshot](https://cloud.githubusercontent.com/assets/6268662/7671385/30887cd8-fceb-11e4-8134-cc2235d5abe3.jpg)

> *Your Queue `URL` will be available in the details tab. We will be using this `URL` for communication.*

## Setting up NodeJs Sender

## Setting up Java Receiver

