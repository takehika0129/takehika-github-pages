---
title: "AWS Lambda “Hello World” Hands-On (2025/02/)"
description: ""
---

#### [Visit (https://github.com/takehika0129/no11-aws-lambda-hands-on)](https://github.com/takehika0129/no11-aws-lambda-hands-on)


# **Concept**


## Usage
Create and Deploy a Simple AWS Lambda Function

1. Sign in to the AWS Lambda Console.
2. Click "Create function" and choose "Author from scratch".
3. Fill in the details:
Function name: hello-world-lambda
Runtime: Python 3.x (Choose the latest version available)
Architecture: x86_64
Permissions: Expand Change default execution role and select "Create a new role with basic Lambda permissions".
4. Click Create function.
5. Replace the default code with:
```sh
import json

def lambda_handler(event, context):
    return {
        'statusCode': 200,
        'body': json.dumps('Hello, World!')
    }
```
6. Click "Deploy".
7. Clieck "Test".
8. 

# **Future Improvements**
- **
  
---
[Back to All Prototypes](../index.md)
