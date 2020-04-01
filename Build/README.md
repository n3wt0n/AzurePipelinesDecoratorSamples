## Build Decorators

The Decorators in this folder work with ___both___ the Classic Build pipelines and the Multistage (_YAML_) pipelines.

When running in YAML pipelines, they are applied to ___both___ __Jobs and Deployment Jobs__

- __Pre__: this decorators run ___before___ any other task in the pipeline
- __Post__: this decorators run ___after___ any other task in the pipeline
- __PrePost__: this decorators run ___both before and after___ any other task in the pipeline