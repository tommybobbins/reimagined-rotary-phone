# Terraform revision notes

## Migrating to Terraform cloud from OSS

The same tf version that was used to perform the migration would be used.

## Workspaces

    $ terraform workspace new bobbins
    $ terraform workspace select bobbins
    $ terraform workspace delete bobbins


Where does local state for workspaces get stored ?

terraform.tfstate.d/<workspace>

## Values

The Terraform language uses the following types for its values: 
bool 
list (or tuple)
map (or object) 
number
string 

## Resource blocks

Resource blocks define the resources you want to create, update, or manage as part of your infrastructure. Other type of block types in Terraform include provider, terraform, output, data, and resource.

## Terraform unlock

$ terraform unlock 
Rmemove the lock on the state for the current configuration
