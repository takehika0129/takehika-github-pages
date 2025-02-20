---
title: "AWS Lambda “Hello World” Hands-On (2025/02/20)"
description: ""
---

#### [Visit (https://github.com/takehika0129/no11-aws-lambda-hands-on)](https://github.com/takehika0129/no11-aws-lambda-hands-on)


# **Concept**
This is designed to demonstrate the fundamentals of AWS Lambda, including deployment, and minimal IAM role setup.


# **📖 How to Set Up AWS Lambda**
1️⃣ Sign in to the AWS Lambda Console.
2️⃣ Click "Create function" and choose "Author from scratch".
3️⃣ Fill in the details:
- Function name: hello-world-lambda
- Runtime: Python 3.x (Choose the latest version available)
- Architecture: x86_64
- Permissions: Expand Change default execution role and select "Create a new role with basic Lambda permissions".
4️⃣ Click "Create function".
5️⃣ Replace the default code with:
```sh
import json

def lambda_handler(event, context):
    return {
        'statusCode': 200,
        'body': json.dumps('Hello, World!')
    }
```
6️⃣ Click "Deploy".
7️⃣ Clieck "Test".

   
# **Future Improvements**
- **Parameter Handling**: Extend functionality to process input parameters dynamically.
- **Connecting Lambda to API Gateway or other triggers**: Enhance the function by enabling API Gateway or multiple triggers such as S3 events, DynamoDB streams, or EventBridge.
  
---
[Back to All Prototypes](../index.md)
