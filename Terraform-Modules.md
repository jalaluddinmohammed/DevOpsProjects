# Learning Terraform Modules

Today, I delved into an intriguing topic in Terraform—Modules.

## What are Modules in Terraform?

Modules in Terraform are a way to organize and structure configuration code into reusable components. They allow you to encapsulate infrastructure resources, making your configurations modular, reusable, and easy to manage.

## Why Use Modules?

When you create resources such as EC2 instances, Azure VMs, S3 buckets, or Azure Storage accounts in the cloud, you write Infrastructure as Code (IAC) for those resources. Modules provide a mechanism for code reuse across projects. Let's say, an EC2 instance and an S3 bucket you have created in Project A. Now, if Project B has similar requirements, you can utilize pre-written code from modules (which is written by Project A).

## How to Use Modules in Terraform?

1. **Writing Code:**
   - Initially, you write the IAC code for creating a resource (e.g., EC2 instance) or a set of resources.

2. **Modularization:**
   - Identify parts of the code that can be reused in different projects.

3. **Creating a Module:**
   - Group the reusable code into a module, which is essentially a directory containing Terraform configuration files.

4. **Source Specification:**
   - When creating infrastructure in a new project (Project B), instead of writing the entire code again, specify the source location of the module containing the reusable code. This source can be a Git repository, Bitbucket, or any other location.

5. **Example Usage:**
 - This is module name which has all the code written by Project A.

![image](https://github.com/jalaluddinmohammed/DevOpsProjects/assets/145260536/dc2a84bb-bc1c-46eb-9e5b-00704dc480ab)

6. **The above code can be reused in any other projects:**
  - Now, this can be used in other Projects, Let’s Say Project B is using. We need to specify the source where the module exists

    ![image](https://github.com/jalaluddinmohammed/DevOpsProjects/assets/145260536/6ac75c9a-02f6-4a43-bca1-5d770bf17cb7)

