## Tag Sources After Build

This decorator requires the Pipeline to be able to operate on the Repo.

To do so, you need to:
- Grant version control permissions to the build servic
- Allow scripts to access the system token:
  - YAML: Make sure checkout has _persistCredentials_ set to _true_ in your pipelies.
  ```yaml
  steps:
   - checkout: self
     persistCredentials: true
  ```
  - Classic: On the options tab select _Allow scripts to access OAuth token_.

#### Requirement

Tag the sources with the BuildID if the Build is succesfull

#### Solution

1. Check that the source control is Git.
2. Tag the latest commit included in the Build with the BuildId

#### Result
The task is executed ONLY when the originating source control is Git, the commit is tagget with the BuildID
