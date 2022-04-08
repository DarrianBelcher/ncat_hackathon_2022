# Team DECK North Carolina Agricultural and Technical State University 2022 Amazon Hackathon Solution 
## Problem Statement
What’s the new service (i.e new Amazon Prime Benefit ) that you can provide to Prime Student Members to make their/your lives better?
###  Background
Prime Student benefits comes with many benefits that’s provided exclusively by Amazon as well as by partnering with other companies such as GrubHub, Course Hero, Student Universe etc- Please review [this link](https://www.amazon.com/Amazon-Student/b?ie=UTF8&node=668781011) to learn more about all the benefits. 

You are welcome to think along these lines to figure out a problem that you face as a student on or off campus and how to best solve it either as a new service by Amazon or with the new partnership with any entity. We highly recommend you to start thinking from Customer/user (i.e Student) stand point to understand the real pain points and validate your assumptions before moving on to build the solution. We highly encourage you to think Big and Bold (the Amazon way!!!) and don’t be restricted by any new constraints. Problems can also range anywhere from solving environmental crisis, food wastage, homelessness, or using technologies like Alexa, AI/VR to solve any problems that may interest you. 

## Evaluation Criteria
We will be scoring your problem solutions along two axes: 1) problem statement evaluation and business idea and 2) implementation details.

We want to encourage you to really **Think Big** and be creative with your solutions.  We’re looking for business ideas that are outside the box and that would excite us both as consumers of Prime (Amazon employees are Prime members!) and as employees within Prime looking to delight our customers.  Additionally, we have basic milestones for the actual implementation, but will reward solutions that are technically challenging and inventive.  

Below you will find the specific implementation milestones we will be looking for.  We will be asking you to build a landing page and an email notification system that emails new Prime members that elect to sign up for Prime via your landing page.  Further details about how to build your landing page and how to implement the email notification system can be found in the **Problem Statement Instructions Section**


**Milestone 1: Functional Landing page**

* You should build a static web page, hosted in S3, that we can navigate to and sign up from. Extra points will be awarded for creative HTML/CSS content and styling! We want an experience that delights the customer!

**Milestone 2: Email Form Submission**

* Your landing page should include a signup form where a visitor can enter their email. This create an HTTP POST request that will invoke the backend processing for sending the email.

**Milestone 3: Lambda**

* Your email form should trigger a Lambda workflow (starter code for this has been provided), that will parse the user’s email from the event input and send the email via SES. Extra points will be rewarded here for extra functionality! Ideas include using DynamoDB to store the emails of users that are already signed up, or personalizing emails with user’s first names. **Think Big!**

**Milestone 4: SES**

* Lambda should invoke SES (Simple Email Service) to actually send the email. You will need to register your team emails and your mentor’s email.

**Presentation:**

* Your presentation will consist of a demo of your website and email workflow. Be sure to showcase how your idea works to *Invent and Simplify* on behalf of customers!

## Working with Mentors
Once you join the zoom meeting provide to you by the hackathon committee, we will guide you to the right break out rooms where you will work with Amazonians throughout the session. 

Mentors are your valuable resource and don’t hesitate to ask any question or help- we are here to work and build with you!

## Problem Solution Instructions
To assist you in implementing your solution to the problem statement, we have provided files that you will edit to build your landing page.  Please review the **Evaluation Criteria** section for further information around what kind of content we expect to see on your landing pages.  We are also asking that students implement an “email notification” feature on their landing page that will send a welcome email to new users that decide to sign up for Amazon Prime as a result of the new service offering you have come up with.  This is to give you exposure to cloud technologies that Amazon Software Development Engineers use in their everyday work, and to help you think with **Customer Obsession,** an Amazon Leadership Principle that’s at the core of our business and influences the way we approach all problems we work on. This is also the way we welcome new customers who visit our Amazon Prime landing page and decide to enroll in Prime today!


# Proposed Solution at Hackathon: 3rd Place Winners: Team DECK
## Team DECK Members: Darrian Belcher, Kyandre’ Roberts, Chanslor Green, Evan Smith

## Product Name:  Amazon Student Prime Package. Includes Amazon Success and Amazon City

### Amazon Success: 
As college students, two time-consuming tasks that we all generally participate in are the tedious scholarship and internship search processes. Affordability is a crucial aspect of earning a college degree. In addition, the importance of professional development and internship opportunities to the evolution of career aspirations can’t be overstated. Amazon success offers students direct access to scholarships, internships, and mentorship from Amazon and partner companies’ employees.

Includes: 
* Scholarships
* Internship opportunities
* Mentorship from Amazon + partner company employees 
* Resume Reviews


### Amazon City: 
We can all admit that the idea of attending college in a city that you know nothing about is scary. Some common questions that may plague your mind include: Where will I meet friends? What types of events will occur on and off-campus? With so many social events available in your city, you could potentially be overwhelmed. Amazon City acts as a hub of social, sports, and overall nightlife events within a 30 mile radius of the user’s zip-code, that will not only allow you to make friends and have amazing experiences, but also enable and promote the prioritization of mental health and self-care. Don’t burn yourself out with your academics and professional development events. Use Amazon city to ensure that you have a well-rounded college experience. 

Includes: 
* Nightlife
* Local restaurants
* Campus Events
* Sports Events 


## Valuable Benefits 
* Students have access to an all-in-1 bundle that is catered to the needs of young college students.
* A platform that encourages professional development.
* Helps students find a social life in a new environment.
* Encourages a balanced lifestyle between academic/career success and social engagement.



### Problem Solution Architecture

At Amazon we love architecture diagrams.  Our engineers use them to illustrate how our services are deployed and how they interact with existing services within the Amazon ecosystem.  Below you will find an architecture diagram illustrating how we want you to deploy your landing page and email notification system.  In this section we’ll explain what each component is, what it does, and provide resources for further reading.  We want to note that this **is not the only way** to implement your solution, but is just one way that you can get things working.  If you have other ideas on how you might implement your solution, we encourage them!  Talk to your mentor for guidance or to talk through your ideas.  At Amazon we encourage diversity of thought and **Bias for Action**.  Solutions to problems are varied and come with pros and cons.  As Software Development Engineers we must consider the various alternatives for implementing solutions, and choose the one that is cost effective, efficient, scalable, and most importantly, one that will **Earn Trust** and **Delight our Customers.**  The intention of this diagram is to introduce you to **Cloud Computing** concepts and **AWS**.  If you have any additional questions, your mentors are your first resource!


![NCAT Hackathon 2022 Solution Architecture(1)](https://user-images.githubusercontent.com/11414055/161352436-7c74f6e5-5b26-4401-89a3-fa12f2388263.jpg)


1. **Client** - the “client” is simply someone on the internet visiting your landing page!  They can access your landing page from a mobile phone with internet access, a desktop computer, an iPad, etc.
2. **Amazon S3** - S3 (Simple Cloud Storage)  is an AWS service that allows customers to store “objects” securely and effectively.  Like many cloud services offered by AWS, S3 is designed with scalability, availability, security and performance in mind.  For the purposes of your solution you don’t really need to worry about the full suite of features of S3, and why they are advantageous to our customers.  Your biggest takeaway is that the “assets” of your landing page will be hosted here, and AWS will provide the infrastructure needed so that these assets can be used to display your landing page, accessible by anyone on the web!
    1. https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html
3. **Amazon API Gateway** - is used to define the entrypoint for services to communicate.  In this context, APIs act as the “front door” for applications (your landing page!) to access data, business logic and functionality from backend services.  In the context of your solution, API Gateway is used to provide your landing page “access” to the “send email” functionality that it will use to send welcome emails to new customers signing up for Amazon Prime.  
    1. https://aws.amazon.com/api-gateway/
4. **Amazon Lambda** - is a “compute” service that let’s you run code without provisioning or managing servers.  In the context of your solution, Lambda will be the compute environment where you define your “send email” function, which is “fronted” by API Gateway.  Much like a road is the “environment” required to drive a car, Lambda provides the “environment” needed to run a piece of code, and abstracts a way a lot of the nuance that typically comes along with having to configure “your own” environment to get a piece of code to execute
    1. https://docs.aws.amazon.com/lambda/latest/dg/welcome.html
5. **Amazon Simple Email Service** - “SES” (Simple Email Service) is an AWS service that allows developers to send email from within any application.  In the context of your solution, SES is used by Lambda to actually send your welcome email to new Prime customers signing up for Prime on your landing page.  You can think of SES in the same way you think of “gmail” (although SES is functionally different) in that SES provides the infrastructure to physically send an email from a sender to a recipient
    1. https://aws.amazon.com/ses/
6. **3rd party email service** - this is the resource that SES interacts with to actually send your email.  If your email account is with “gmail”, for example, SES will interact with gmail’s email servers to send your email for you



