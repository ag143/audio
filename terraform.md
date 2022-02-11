## Terraform Basics

### Tutorials: https://learn.hashicorp.com/terraform
### GIthub Link:https://github.com/orgs/hashicorp/repositories?q=learn-terraform-&type=&language=&sort=

####Terraform Registry Template for different cloud providers

# https://registry.terraform.io/namespaces/hashicorp
# https://registry.terraform.io/providers/hashicorp/aws/latest/docs
# https://github.com/terraform-provider-openstack/terraform-provider-openstack
# https://registry.terraform.io/providers/hashicorp/kubernetes/latest/docs
# https://registry.terraform.io/providers/hashicorp/google/latest/docs



### What is Terraform
Terraform is an infrastructure as code (IaC) tool that allows you to build, change, and version infrastructure safely and efficiently. This includes low-level components such as compute instances, storage, and networking, as well as high-level components such as DNS entries, SaaS features, etc.

### Usage: terraform [-version] [-help] <command> [args]

<p> The available commands for execution are listed below.
The most common, useful commands are shown first, followed by
less common or more advanced commands. If you're just getting
started with Terraform, stick with the common commands. For the
other commands, please read the help and docs before usage.</p>

### Common commands:
-    apply              -->Builds or changes infrastructure
-    console            -->Interactive console for Terraform interpolations
-    destroy            -->Destroy Terraform-managed infrastructure
-    env                -->Workspace management
-    fmt                -->Rewrites config files to canonical format
-    get                -->Download and install modules for the configuration
-    graph              -->Create a visual graph of Terraform resources
-    import             -->Import existing infrastructure into Terraform
-    init               -->Initialize a Terraform working directory
-    output             -->Read an output from a state file
-    plan               -->Generate and show an execution plan
-    providers          -->Prints a tree of the providers used in the configuration
-    push               -->Upload this Terraform module to Atlas to run
-    refresh            -->Update local state file against real resources
-    show               -->Inspect Terraform state or plan
-    taint              -->Manually mark a resource for recreation
-    untaint            -->Manually unmark a resource as tainted
-    validate           -->Validates the Terraform files
-    version            -->Prints the Terraform version
-    workspace          -->Workspace management

### All other commands:
-    debug              Debug output management (experimental)
-    force-unlock       Manually unlock the terraform state
-    state              Advanced state management
