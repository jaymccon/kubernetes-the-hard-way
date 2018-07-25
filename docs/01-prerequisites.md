# Prerequisites

## Amazon Web Services

This tutorial leverages the [Amazon Web Services](https://aws.amazon.com/) to streamline provisioning of the compute infrastructure required to bootstrap a Kubernetes cluster from the ground up. [Sign up](https://portal.aws.amazon.com/gp/aws/developer/registration/index.html) and take advantage of the [free tier](https://aws.amazon.com/free/).

[Estimated cost](https://calculator.s3.amazonaws.com/index.html) to run this tutorial: $0.28 per hour ($6.63 per day).

> The compute resources required for this tutorial exceed the AWS free tier.

## AWS CLI

### Install the AWS CLI

Follow the AWS CLI [documentation](https://docs.aws.amazon.com/cli/latest/userguide/installing.html) to install and configure the `aws` command line utility.

Verify the CLI version is 1.15.32 or higher:

```
aws --version
```

### Set a default region and output format

This tutorial assumes a default region has been configured and that the default output format is `json`.

```
aws config
```

## Running Commands in Parallel with tmux

[tmux](https://github.com/tmux/tmux/wiki) can be used to run commands on multiple compute instances at the same time. Labs in this tutorial may require running the same commands across multiple compute instances, in those cases consider using tmux and splitting a window into multiple panes with `synchronize-panes` enabled to speed up the provisioning process.

> The use of tmux is optional and not required to complete this tutorial.

![tmux screenshot](images/tmux-screenshot.png)

> Enable `synchronize-panes`: `ctrl+b` then `shift :`. Then type `set synchronize-panes on` at the prompt. To disable synchronization: `set synchronize-panes off`.

Next: [Installing the Client Tools](02-client-tools.md)
