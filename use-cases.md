
## What ctrlplane does

`ctrlplane` excels in orchestrating an organization's _digital assets_. Digital assets 
can any software, configuration or cloud infrastucture. Examples:
* cloud managed infrastructure (databases, clusters, etc)
* custom software deployed on a server
* a code repository
* a directory of log files

## Workspaces

As an organization administrator, I must create a _workspace_ to orchestrate changes to my 
digital assets.

To affect digital assets, however, `ctrlplane` requires integrations to the outside. 

### Integrations

Two types of _integrations_ are required: Job Agents and Resource Providers.

I must create at least one _Job Agent_ to trigger updates on my assets. An example is a Github Agent that 
can trigger Github Actions which subsequently deploy software.

I must also set up at least one _Resource Provider_ to detecty what is in my infrastructure. In `ctrlplane` 
terminology these scan for available _resources_. A resource 
can be any number of things: a Kubernetes cluster in a cloud provider, a physical server, 
a Terraform workspace, a VPC or even something as small as an AWS Lambda. 

Looking at it from a very simplified level, a Resource Provider gathers the infrastructure _input_ 
for `ctrlplane` while Job Agents receive ctrlplane's _output_ to affect digital assets.




As someone responsible for a set of services and related infrastructure at a larger enterprise,
I could create a _system_ to isolate the configurations and verions of my area of responsibility.

As someone who manages infrastructure, I could create a _system_ as a place to isolate the configurations
and versions of various things I'm in charge of.


Beginning with an empty system, I need to a service pushed out to three existing Kubernetes clusters, one
each in AWS, Azure and GCP. Steps of operation:

* For AWS, Azure and GCP, ctrlplane has _managed_ Resource Providers (RP). A _managed_ RP allows a
process running _inside ctrlplane_ to find available clusters in AWS, Azure and GCP. More details of 
this configuration is discussed separately, but this is how ctrlplane knows which Kubernetes _Resources_
are available.
* I will also need to create a _Deployment_ called "My Service" for "My System".


For every job that is created, there will be new rows in release_values for each key/value config.
