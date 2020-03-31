## Advanced Decorators

The Decorators in this folder contain different implementation of useful tasks.

The folders follow the following naming convention:

`
<TARGET>-<TYPE>-<TASK>
`

Where:
- __TARGET__ is the pipeline type where the decorator will run
  - _Build_: for Classic Build or YAML pipelines
  - _Release_: for Classic Release pipelines
  - _DeploymentJob_: for Deployment Jobs in YAML pipelines
- __TYPE__
  - _Pre_: this decorators run before any other task in the pipeline
  - _Post_: this decorators run after any other task in the pipeline
  - _PrePost_: this decorators run before and after any other task in the pipeline 
- __TASK__: the actual operation(s) that the decorator performs

### Decorator-specific information

Check the README in each Decorator folder to know more about what each Decorator does.
