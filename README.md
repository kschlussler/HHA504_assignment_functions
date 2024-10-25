# HHA504_assignment_functions
## 1. Azure Serverless Function Deployment
I successfully deployed a serverless function using Microsoft Azure. The function is a simple HTTP-triggered function that returns "Hello, World!" when called. Below are the steps I followed to deploy the function:

Steps:
1. Azure Portal: I navigated to the Azure portal and created a new Function App.
2.Function Creation: I selected an HTTP trigger and wrote a basic function in Python that outputs "Hello, World!".
3.Testing: After deploying, I tested the function by accessing its URL in my browser, and it successfully returned "Hello, World!".

Azure Function Code:
def main(req):
    return 'Hello, World!'

## 2. GitHub Actions Cron Job

I also created a cron job using GitHub Actions that runs a script every day at midnight. The cron job logs "Scheduled task executed" in the console.

GitHub Actions Workflow:
Here is the code for the workflow (cron-job.yml):

name: Cron Job Example

on:
  schedule:
    # Run daily at midnight
    - cron: '0 0 * * *'

jobs:
  run-script:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Run a script
        run: echo "Scheduled task executed"
