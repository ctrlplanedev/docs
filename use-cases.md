
As an administrator, I create a _workspace_ to create a place to manage my infrastructure and deployments.

As someone who manages infrastructure, I could create a _system_ as a place to isolate the configurations
and versions of various things I'm in charge of.

After creating a workspace, I can create a Job Agent to tigger Github Actions 

As someone responsible for a set of services and related infrastructure at a larger enterprise,
I could create a _system_ to isolate the configurations and verions of my area of responsibility.


Beginning with an empty system, I need to a service pushed out to three existing Kubernetes clusters, one
each in AWS, Azure and GCP. Steps of operation:
* For AWS, Azure and GCP, ctrlplane has _managed_ Resource Providers (RP). A _managed_ RP allows a
process running _inside ctrlplane_ to find available clusters in AWS, Azure and GCP. More details of 
this configuration is discussed separately, but this is how ctrlplane knows which Kubernetes _Resources_
are available.
* I will also need to create a _Deployment_ called "My Service" for "My System".


For every job that is created, there will be new rows in release_values for each key/value config.
