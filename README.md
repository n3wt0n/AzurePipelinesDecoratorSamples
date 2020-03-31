# Azure Pipelines Decorator Samples

[![License](https://img.shields.io/github/license/n3wt0n/AzurePipelinesDecoratorSamples.svg)](https://github.com/n3wt0n/AzurePipelinesDecoratorSamples/blob/master/LICENSE)

A series of sample Decorators for Azure Pipelines (Build and Release).

Decorators in this repo work with both Azure DevOps and Azure DevOps Server.

## About this repo structure

There are 2 types of Basic Decorators in this repo:

- __Build__: The Decorators in this folder work with ___both___ the Classic Build pipelines and the Multistage (_YAML_) pipelines.
- __Release__: The Decorators in this folder work ___only___ with the Classic Release pipelines.

In each of the previous folder, there are three other folders:
- __Pre__: this decorators run ___before___ any other task in the pipeline
- __Post__: this decorators run ___after___ any other task in the pipeline
- __PrePost__: this decorators run ___both before and after___ any other task in the pipeline

The __Advanced__ folder instead contains some different examples of slightly more advanced decorators, with specific implementations.

## Getting Started

To keep things simple, each folder is a standalone decorator extension. 

Pick the one you want to use and follow the steps below.

For basic prerequisites take a look [here](https://docs.microsoft.com/en-us/azure/devops/extend/get-started/node?view=azure-devops#prerequisites)

### Build and Package the extension

First you need to install all the Node.js dependencies:

```cmd
npm install
```

Then you need to actually create the extension:

```cmd
tfx extension create
```

This will generate the _.vsix_ package file

> Remember to change the Publisher in the _vss-extension.json_ file with your publisher

### Publish the extension

When you have the extension file, head to [the marketplace management portal](https://marketplace.visualstudio.com/manage) and add the new extension.

You will also need to _share_ the extension to your organization.

> Only private extensions can contain Decorators, so be sure not to make it public.

For more info take a look at: https://docs.microsoft.com/en-us/azure/devops/extend/get-started/node?view=azure-devops#package-and-publish-your-extension

### Install the extension

Once shared with your Azure DevOps Organization, you can head to the _Manage Extensions_ tab under _Organization Settings_, go to _Shared_ and finally install your Decorato Extension.

For more info take a look at: https://docs.microsoft.com/en-us/azure/devops/extend/get-started/node?view=azure-devops#install-your-extension
