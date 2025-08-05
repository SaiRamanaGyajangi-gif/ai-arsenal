AI Coding Assistants: A Deep Dive into Sourcegraph Cody and Amazon CodeWhisperer
AI coding assistants are revolutionizing software development by automating repetitive tasks, enhancing code understanding, and boosting productivity. This guide explores two powerful tools—Sourcegraph Cody and Amazon CodeWhisperer—detailing their features, installation, usage, benefits, and real-world scenarios with examples. Whether you're a solo developer or part of a large team, these tools can streamline your workflow.
1. Sourcegraph Cody
What is Sourcegraph Cody?
Sourcegraph Cody is an AI-powered coding assistant developed by Sourcegraph, designed to help developers navigate, understand, and interact with large codebases. It leverages Sourcegraph’s code graph and advanced large language models (LLMs) to provide context-aware code suggestions, explanations, and answers to natural language queries. Cody excels in scenarios requiring deep codebase understanding, making it ideal for teams working on complex or legacy projects.
How to Use Sourcegraph Cody
Installation
Cody is available as an extension for popular IDEs and integrates with Sourcegraph’s web platform. Follow these steps to install:

VS Code:
Open VS Code, go to the Extensions view (Ctrl+Shift+X or Cmd+Shift+X on macOS).
Search for “Cody AI” by Sourcegraph.
Click “Install” and authenticate with your Sourcegraph account.
Link: Cody VS Code Extension


JetBrains IDEs (e.g., IntelliJ, PyCharm):
Navigate to File > Settings > Plugins in your JetBrains IDE.
Search for “Cody” and install the plugin.
Authenticate with Sourcegraph.


Sourcegraph Web:
Sign up at sourcegraph.com.
Connect your repository (GitHub, GitLab, etc.) to enable Cody’s codebase-aware features.


Verify Installation:
Open a project in your IDE, select a code file, and check for the Cody icon or chat interface.



Configuration

Authentication: Sign in with a Sourcegraph account (free tier available) or enterprise credentials.
Codebase Connection: Link your repository to enable context-aware suggestions.
Custom Prompts: Create reusable prompts for tasks like code documentation or unit test generation.

Basic Usage

Autocomplete: Cody suggests code completions as you type, tailored to your codebase.
Chat Interface: Ask questions about your code (e.g., “What does this function do?”) via the Cody chat panel.
Commands: Use predefined or custom commands to generate tests, refactor code, or detect issues.

Where to Install

Supported Platforms: VS Code, JetBrains IDEs (IntelliJ, PyCharm, etc.), Neovim, and Sourcegraph Web.
Operating Systems: Windows, macOS, Linux.
Free Tier: Available with a generous limit for individual developers; Pro ($9/month) and Enterprise ($15/user/month) plans offer advanced features.

Benefits

Deep Codebase Understanding: Cody indexes entire repositories, providing context-aware suggestions and answers, ideal for large or complex projects.
Code Explanation: Breaks down complex code line-by-line, helping onboard new developers or understand legacy code.
Customizable Prompts: Allows teams to create reusable prompts for consistent coding practices.
Security and Privacy: Implements a zero-retention policy and respects code host permissions, making it suitable for enterprise use.
Multi-Language Support: Supports TypeScript, Go, Python, Java, JavaScript, and more, with strong performance across diverse codebases.

Scenarios and Examples
Scenario 1: Explaining Legacy Code
Context: You’re working on a legacy JavaScript project and encounter an unfamiliar function.Example:
function isPrime(num) {
  for (let i = 2; i < num; i++) {
    if (num % i === 0) return false;
  }
  return true;
}


Prompt to Cody: “Explain this function.”
Cody Response: “This function, isPrime, checks if a number (num) is prime by testing divisibility from 2 to num - 1. If any number divides num evenly (remainder is 0), it returns false (not prime). If no divisors are found, it returns true (prime). Note: It doesn’t handle edge cases like num <= 1.”
Benefit: Quickly understand unfamiliar code without manual debugging.

Scenario 2: Generating Unit Tests
Context: You need unit tests for a Python function.Example:
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)


Prompt to Cody: “Generate unit tests for this function.”
Cody Response:

import unittest

class TestFactorial(unittest.TestCase):
    def test_factorial_zero(self):
        self.assertEqual(factorial(0), 1)
    
    def test_factorial_positive(self):
        self.assertEqual(factorial(5), 120)
    
    def test_factorial_one(self):
        self.assertEqual(factorial(1), 1)

if __name__ == '__main__':
    unittest.main()


Benefit: Automates test generation, saving time and ensuring code reliability.

Scenario 3: Refactoring Code
Context: Improve a function to handle edge cases.Example:
function isPrime(num) {
  for (let i = 2; i < num; i++) {
    if (num % i === 0) return false;
  }
  return true;
}


Prompt to Cody: “Refactor this function to handle edge cases.”
Cody Response:

function isPrime(num) {
  if (!Number.isInteger(num) || num <= 1) return false;
  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) return false;
  }
  return true;
}


Explanation: “This refactored version checks if num is an integer and greater than 1, and optimizes the loop to check only up to the square root of num, improving performance.”
Benefit: Enhances code quality and performance with minimal effort.

2. Amazon CodeWhisperer
What is Amazon CodeWhisperer?
Amazon CodeWhisperer is an AI-powered coding assistant developed by AWS, designed to provide real-time code suggestions, autocompletion, and security scanning. Trained on public code repositories and AWS SDKs, it excels in generating code snippets, especially for AWS-related development, and is free for individual developers with an AWS Builder ID.
How to Use Amazon CodeWhisperer
Installation

VS Code:
Install the AWS Toolkit extension from the VS Code Marketplace.
Search for “AWS Toolkit” and click “Install.”
Authenticate with an AWS Builder ID or AWS account.
Enable CodeWhisperer in the AWS Toolkit settings.
Link: AWS CodeWhisperer


JetBrains IDEs:
Go to File > Settings > Plugins, search for “AWS Toolkit,” and install.
Configure with your AWS credentials.


AWS Cloud9:
CodeWhisperer is natively integrated; enable it in the Cloud9 settings.


Verify Installation:
Start typing in a supported language (e.g., Python, Java), and CodeWhisperer will display suggestions.



Configuration

AWS Credentials: Use an AWS Builder ID for free access or an AWS account for enterprise features.
Security Scanning: Enable security scans to detect vulnerabilities based on OWASP guidelines.
Language Support: Configure for Python, Java, JavaScript, TypeScript, C++, and more.

Basic Usage

Autocomplete: CodeWhisperer suggests code as you type, from single lines to full functions.
Natural Language Comments: Write comments (e.g., “# Create a Lambda handler”), and CodeWhisperer generates corresponding code.
Security Scanning: Automatically scans code for vulnerabilities and suggests fixes.

Where to Install

Supported Platforms: VS Code, JetBrains IDEs, AWS Cloud9, Eclipse.
Operating Systems: Windows, macOS, Linux.
Free Tier: Available for individuals with an AWS Builder ID; professional plan starts at $15/month for advanced features.

Benefits

Real-Time Suggestions: Generates code snippets, functions, or entire classes, reducing coding time.
AWS Integration: Optimized for AWS services (e.g., Lambda, S3), providing accurate, context-aware suggestions for cloud development.
Security Scanning: Detects vulnerabilities and suggests fixes, enhancing code safety.
Free for Individuals: Accessible to solo developers at no cost with an AWS Builder ID.
Broad Language Support: Supports Python, Java, JavaScript, TypeScript, C++, and more, with strong AWS SDK integration.

Scenarios and Examples
Scenario 1: AWS Lambda Development
Context: Writing an AWS Lambda function in Python.Example:
# Start typing
def lambda_handler(event, context):


CodeWhisperer Suggestion:

def lambda_handler(event, context):
    response = {
        'statusCode': 200,
        'body': json.dumps('Hello from Lambda!')
    }
    return response


Benefit: Speeds up AWS-specific development with ready-to-use, idiomatic code.

Scenario 2: Security Scanning
Context: Writing a function that handles user input.Example:
def process_input(user_data):
    return eval(user_data)  # Unsafe code


CodeWhisperer Response: Flags eval as a security risk, suggesting:

def process_input(user_data):
    # Use safer parsing, e.g., json.loads for JSON data
    import json
    return json.loads(user_data)


Benefit: Improves code security by identifying and mitigating vulnerabilities.

Scenario 3: Generating Boilerplate Code
Context: Creating a REST API endpoint in Java.Example:
// Handle HTTP GET request


CodeWhisperer Suggestion:

import com.amazonaws.services.lambda.runtime.Context;
import com.amazonaws.services.lambda.runtime.RequestHandler;

public class ApiHandler implements RequestHandler<APIGatewayProxyRequestEvent, APIGatewayProxyResponseEvent> {
    public APIGatewayProxyResponseEvent handleRequest(APIGatewayProxyRequestEvent input, Context context) {
        APIGatewayProxyResponseEvent response = new APIGatewayProxyResponseEvent();
        response.setStatusCode(200);
        response.setBody("{\"message\": \"Hello from API!\"}");
        return response;
    }
}


Benefit: Automates boilerplate code creation, saving time on repetitive tasks.

When to Use Which Tool?



Tool
Best Use Case
IDE Support
Free Tier



Cody
Understanding and navigating large codebases, explaining legacy code, team collaboration
VS Code, JetBrains, Sourcegraph Web, Neovim
Yes


CodeWhisperer
Fast coding, AWS-specific development, security-focused projects
VS Code, JetBrains, AWS Cloud9, Eclipse
Yes



Cody: Choose for projects requiring deep codebase context, such as onboarding new developers or maintaining complex monorepos. Its strength lies in explaining and analyzing existing code.
CodeWhisperer: Ideal for rapid development, especially in AWS environments, or when security scanning is a priority. It shines in generating code quickly for cloud-based applications.

Best Practices for Using AI Coding Assistants

Configure Your Environment: Ensure proper IDE setup to avoid compatibility issues.
Review Suggestions: Always validate AI-generated code for accuracy and alignment with project standards.
Leverage Documentation: Use official documentation for Cody (sourcegraph.com/docs) and CodeWhisperer (aws.amazon.com/codewhisperer) to maximize features.
Integrate into Workflow: Use Cody for codebase exploration and CodeWhisperer for rapid coding to complement your workflow.
Check Security: For CodeWhisperer, enable security scans to catch vulnerabilities early.

Conclusion
Sourcegraph Cody and Amazon CodeWhisperer are powerful AI coding assistants with distinct strengths. Cody excels in understanding and navigating large codebases, making it perfect for complex projects and team collaboration. CodeWhisperer accelerates coding with real-time suggestions and AWS integration, ideal for cloud developers and security-conscious projects. By incorporating these tools into your workflow, you can boost productivity, reduce errors, and enhance code quality. Explore the examples in this repository’s examples/ folder for hands-on demonstrations.
Repository Structure
📁 ai-code-assistants/
├── README.md                    # This file
├── examples/
│   ├── cody-code-explanation.md # Cody examples for code explanation and refactoring
│   ├── codewhisperer-completion.py # CodeWhisperer examples for code completion

For more details, check out the examples/ folder in this repository, and visit my GitHub for additional resources!
