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
- bool 
- list (or tuple)
- map (or object) 
- number
- string 

## Resource blocks

Resource blocks define the resources you want to create, update, or manage as part of your infrastructure. Other type of block types in Terraform include provider, terraform, output, data, and resource.

## Terraform unlock

    $ terraform unlock 

The terraform force-unlock command can be used to remove the lock on the Terraform state for the current configuration. Another option is to use the "terraform state rm" command followed by the "terraform state push" command to forcibly overwrite the state on the remote backend, effectively removing the lock. It's important to note that these commands should be used with caution, as they can potentially cause conflicts and data loss if not used properly.
