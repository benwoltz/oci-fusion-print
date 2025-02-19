# oci-fusion-print

The OCI Terraform stack for Fusion Printing allows you to create and provision OCI infrastructure components required to print security from Fusion using OCI.  

It creates the following resources outlined in this [blog] and [video] 

* VCN with a CIDR block, public subnet, and route table
* Internet gateway
* Dynamic routing gateway
* Public flexible load balancer with a single backend set and a single backend
* Network security group with appropriate rules for Fusion printing

## Prerequisites and postrequisites

There are some tasks outside of OCI and this Terraform stack that you will need in order for this solution to work.  Those tasks are outlined below, please see the [blog] and [video] 

* FastConnect or IPSec VPN Tunnel from OCI to on-premise
* Printer or print server on-premise
* Public CIDR from the region where your Fusion applications are hosted
* External/public DNS record that resolves to the public IP address of the Flexible Load Balancer

## Resource Manager Deployment

This Quick Start uses [OCI Resource Manager](https://docs.cloud.oracle.com/iaas/Content/ResourceManager/Concepts/resourcemanager.htm) to make deployment easy, sign up for an [OCI account](https://cloud.oracle.com/en_US/tryit) if you don't have one, and just click the button below:

[![Deploy to Oracle Cloud](https://oci-resourcemanager-plugin.plugins.oci.oraclecloud.com/latest/deploy-to-oracle-cloud.svg)](https://cloud.oracle.com/resourcemanager/stacks/create?region=home&zipUrl=https://github.com/oracle-quickstart/oci-fusion-print/archive/master.zip)

After logging into the console you'll be taken through the same steps described
in the [Deploy](#deploy) section below.


Note, if you use this template to create another repo you'll need to change the link for the button to point at your repo.



# Terraform for Secure On-Premise Printing from Fusion BI Publisher for OCI

The [Terraform Secure On-Premise Printing from Fusion BI Publisher][repo] for [Oracle Cloud Infrastructure][OCI] provides a reusable [Terraform][terraform] module that provisions OCI infrastructure required to allow Fusion printing to on-premise according to this [blog].

It creates the following resources:

* A VCN with a CIDR block and a public subnet
* An internet gateway and a route table
* A dynamic routing gateway
* A public load balancer with a single backend set and a single backend
* A network security group with appropriate rules for Fusion printing



#### Instructions

* [Quickstart][quickstart]
* [Reusing as a Terraform module][reuse]
* [Terraform Options][terraform_options]

## Related Documentation, Blog

* [Oracle Cloud Infrastructure Documentation][oci_documentation]
* [Terraform OCI Provider Documentation][terraform_oci]
* [Erik Berg on Networks, Subnets and CIDR][subnets]
* [Lisa Hagemann on Terraform cidrsubnet Deconstructed][terraform_cidr_subnet]

## Projects using this module

## Changelog

View the [CHANGELOG][changelog].

## Acknowledgement

Code derived and adapted from [Terraform OCI Examples][terraform_oci_examples] and Hashicorp's [Terraform 0.12 examples][terraform_oci_examples]

## Contributors

[Folks who contributed with explanations, code, feedback, ideas, testing etc.][contributors]

Learn how to [contribute][contributing].

## License

Copyright (c) 2019, 2021 Oracle and/or its associates.

Licensed under the [Universal Permissive License 1.0][license] as shown at
[https://oss.oracle.com/licenses/upl][canonical_license].

<!-- Links reference section -->
[changelog]: https://github.com/oracle-terraform-modules/terraform-oci-vcn/blob/main/CHANGELOG.adoc
[contributing]: https://github.com/oracle-terraform-modules/terraform-oci-vcn/blob/main/CONTRIBUTING.adoc
[contributors]: https://github.com/oracle-terraform-modules/terraform-oci-vcn/blob/main/CONTRIBUTORS.adoc
[docs]: https://github.com/oracle-terraform-modules/terraform-oci-vcn/tree/main/docs

[blog]: https://www.ateam-oracle.com/post/using-oci-for-secure-on-prem-printing-from-oracle-fusion-bi-publisher
[video]: https://www.youtube.com/watch?v=6xJo-njF1r0

[oci]: https://cloud.oracle.com/cloud-infrastructure
[oci_documentation]: https://docs.cloud.oracle.com/iaas/Content/home.htm

[oracle]: https://www.oracle.com
[prerequisites]: https://github.com/oracle-terraform-modules/terraform-oci-vcn/blob/main/docs/prerequisites.adoc

[quickstart]: https://github.com/oracle-terraform-modules/terraform-oci-vcn/blob/main/docs/quickstart.adoc
[repo]: https://github.com/oracle-quickstart/oci-fusion-print
[terraform]: https://www.terraform.io
[terraform_oci]: https://www.terraform.io/docs/providers/oci/index.html
<!-- Links reference section -->