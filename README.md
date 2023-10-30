# Exploring-AWS-IAM
Aim of the project: Exploring pre-created IAM Users and Groups, Inspecting IAM policies as applied to the pre-created groups, Following a real-world scenario, adding users to groups with specific capabilities enabled, Locating and using the IAM sign-in URL, Experimenting with the effects of policies on service access

Task 1: Explore the IAM Dashboard (Users and Groups)

![image](https://github.com/ParthHBhimani/Exploring-AWS-IAM/assets/101561352/e628059f-d2c8-45a2-bda0-d7e1431ea61a)

The following groups were already created for the lab:
EC2-Admin
EC2-Support
S3-Support
Currently there are no users added to any user groups.

As we select a user group we can see the permissions for that group
![image](https://github.com/ParthHBhimani/Exploring-AWS-IAM/assets/101561352/0e47b98f-d207-493c-9532-d62a4466b05b)

This policy is granting permission to List and Describe information about EC2, Elastic Load Balancing, CloudWatch and Auto Scaling. This ability to view resources, but not modify them, is ideal for assigning to a Support role.
The basic structure of the statements in an IAM Policy is:
Effect says whether to Allow or Deny the permissions.
Action specifies the API calls that can be made against an AWS Service 
Resource defines the scope of entities covered by the policy rule (eg a specific Amazon S3 bucket or Amazon EC2 instance, or * which means any resource).

Given Business Scenario : Your company is growing its use of Amazon Web Services, and is using many Amazon EC2 instances and a great deal of Amazon S3 storage. You wish to give access to new staff depending upon their job function

![image](https://github.com/ParthHBhimani/Exploring-AWS-IAM/assets/101561352/6996c06b-76b2-451c-874d-d1d2ef0f0779)

Task 2: Add Users to Groups
![image](https://github.com/ParthHBhimani/Exploring-AWS-IAM/assets/101561352/6deca7fa-43e5-4a36-9272-9e758df62012)

I added all the users to their respective groups.

Task 3: Sign-In and Test Users
![image](https://github.com/ParthHBhimani/Exploring-AWS-IAM/assets/101561352/f2a44ca1-efb7-4251-b6a2-8a08098c006e)

Now I have signed in as user-1 belonging to group S3-support
I tested if user-1 has access to view the S3 buckets
![image](https://github.com/ParthHBhimani/Exploring-AWS-IAM/assets/101561352/f65d345c-80d9-4128-bebf-ee518a307028)

I tested if the user-1 has access to view EC2 instances for which the access has only been granted to user-2 and user-3.
![image](https://github.com/ParthHBhimani/Exploring-AWS-IAM/assets/101561352/9c8459d3-c5a3-4f13-aa07-612fb3cb4dac)

I conducted a test to determine if a user, specifically "user-2," possessing limited permissions that grant them the ability to view instances, has the capability to stop an EC2 instance.
![image](https://github.com/ParthHBhimani/Exploring-AWS-IAM/assets/101561352/cb01634a-4ab4-4341-8ea3-7e9e5583cef9)

Now I signed in as user-3 to check if the above action can be performed by someone who has been granted the access to do so.
![image](https://github.com/ParthHBhimani/Exploring-AWS-IAM/assets/101561352/3ad89768-2329-44be-a356-9e678195e5b4)


Conclusion
Explored pre-created IAM users and groups
Inspected IAM policies as applied to the pre-created groups
Followed a real-world scenario, adding users to groups with specific capabilities enabled
Located and used the IAM sign-in URL
Experimented with the effects of policies on service access
























