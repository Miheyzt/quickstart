# Quickstart examples for Otomi

Quickly deploy Otomi in your public cloud of choice or install it locally on your machine (using Minikube).

**NOTE:** Intended for experimentation/evaluation ONLY.

**You will be responsible for any/all infrastructure costs incurred by these used resources.**
This repository intends to minimize costs by only provisioning the minimum required resources for a given provider.

---

### Public cloud providers

Quickstarta are available for:

- [**Google Cloud Platform** (`gcp`)](./gcp)
- [**Microsoft Azure Cloud** (`azure`)](./azure)

For a full (enterprise/production) setup, please visit [otomi.io](https://otomi.io)

We will soon make a quickstart available for:

- [**Amazon Web Services** (`aws`)](./aws)

The quickstart examples will install Otomi on a 3 nodes Managed Kubernetes cluste, as this setup provides easy access to all Otomi features.

### Local cluster using Minikube (Coming Soon)

- Next to the quickstarts for running Otomi in your public cloud of choice, you can also run Otomi locally on your machine using [Minikube](https://minikube.sigs.k8s.io/docs/start/)

----

### Requirements

- Terraform >=0.14.0
- Credentials for the cloud provider used for the quickstart

### Deploy

To begin with any of the public cloud quickstart, perform the following steps:

1. Clone or download this repository
2. Choose a cloud provider and navigate into `<cloud-provider>/<managed-k8s>` folder
3. Rename `terraform.tfvars.example` to `terraform.tfvars` and fill in all required variables
4. Run `terraform init`
5. Run `terraform apply`

Once the cluster is up and running,

1. Navigate to `otomi-install` folder
2. Rename `terraform.tfvars.example` to `terraform.tfvars` and fill in all required variables
3. Run `terraform init`
4. Run `terraform apply`

Follow the post installation instructions [here.](https://otomi.io/docs/installation/post-install-actions)

### Destroy

When you're finished exploring Otomi, use terraform to tear down all resources in the quickstart.

**NOTE: Any resources not provisioned by the quickstart are not guaranteed to be destroyed when tearing down the quickstart.**
Make sure you tear down any resources you provisioned manually before running the destroy command.

Run `terraform destroy -auto-approve` to remove all resources without prompting for confirmation.
