## Check Branch Before Deployment - Verbose

This Decorator is for Classic Release Pipelines.

#### Requirement

Allow the deployment in Production only if the sources are coming from the _master_ branch.

#### Solution

1. Execute the decorator only on Deployment Jobs
2. Check the "stage name". Continue only if it is "PRD", "Prod" or "Production".
3. Check the name of the source branch.
4. Print everything out every time
5. 
   - Continue the deployment if the source branch is _master_
   - Fail the deployment if the source branch is anything else

#### Result
The task is executed ONLY when the job is a deployment job.

It prints out _Stage Name_ and _Branch Name_ every time.

If the stage name contains "prd" or "prod", and the branch is not "master", it makes the deployment fail.
Otherwise, the deplyment continues.