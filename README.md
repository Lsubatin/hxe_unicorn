# Unicorn's HANA Express
This repository is part of a set of internal instructions, so some pieces of it will make no sense.

Sample terraform setup for pre-built image of HANA express and Windows VM, to be used in a VPC. This works if the network and subnetwork have been setup already.

Sorry, I cannot distribute the pre-built iamge, but you can take one yourself in Google Cloud console > Compute Engine > Images.

## Dependencies

Create the network using something like fromt he Google Cloud shell:

```
gcloud config set project <<SET YOUR PROJECT ID HERE>>
gcloud compute networks create hananw --subnet-mode=custom
gcloud compute networks subnets create hananw-subnet --enable-private-ip-google-access --network=hananw --region=us-central1 --range=10.12.0.0/20
```
