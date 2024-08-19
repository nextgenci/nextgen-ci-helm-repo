# NextGen CI Helm Charts Repository

Welcome to the official Helm repository for NextGen CI. This repository contains Helm charts for deploying and managing the core components of the NextGen CI platform.


## Installation

To start using the Helm charts from this repository, add the repository to your Helm client with the following command:

```shell
helm repo add add nextgenci https://helm-nextgenci.msharbaji.com
```

To update and view all available charts in the repository, run:

```shell
helm repo update nextgenci
helm search repo nextgenci
```

From here, you can install or upgrade Helm charts as follows:

```shell
helm upgrade --install nextgenci-ci nextgenci/nextgenci-ci --namespace nextgenci --wait
```

## Local Testing 

If you want to test these helm charts on your local machine, follow the following instructions:

Prepare your system to run Kind clusters:

```shell
kind create cluster --name nextgenci
```

Install the Helm chart:

```shell
helm install nextgenci-ci ./nextgenci-ci --namespace nextgenci --wait
```

