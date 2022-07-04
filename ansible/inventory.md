# Inventory file

1. [Example ini file](#ini)
1. [Example yaml file](#yaml)

Inventory file contains hosts to control and also could contain some variables.

Yaml or ini files could be used. Ansible docs prefers yaml.

## Inı

> ```ini
> # Comments starts with hash
> 
> # you can put hosts straight into here
> 10.1.1.100
> 10.1.1.101
> 
> # could group them too
> [group1]
> 10.1.1.102
> 10.1.1.103
> 
> # specify range for many hosts
> [group2]
> 10.1.1.10[4:5] # this means 104 and 105 is among hosts
> 10.1.1.10[6:8:2] # last digit is step. only 106 and 108 is in hosts
> 
> # you can use dns records 
> # and can use brackets with digits or chars
> [group3]
> web[1:5].example.com
> web[a:z].example.com
> 
> # specify variables for hosts
> 10.1.1.107 http_port=80
> 
> # specify variables for groups
> [group3:vars]
> http_port=80
> 
> # you can rename a host to your needs like that
> [group4]
> tomato ansible_host=10.1.1.109
> 
> # can make group of groups this way
> [groups:children]
> group1
> group2
> group[3:4]
> 
> ```
## Yaml

> ```yaml
> ---
> # yaml file starts with three dashes
> # be carefull for indentation
> 
> all: 
>   hosts:
>     10.1.1.100: # can put hosts straight into here
>     10.1.1.101:
>       http_port: 80 # specify host variables
>   children: # all groups are children of "all" group
>     groups: # this is group of groups
>       children: # finally children groups of "groups" group comes
>         group1:
>           hosts:
>             10.1.1.102: # hosts member of group1
>             10.1.1.103:
>         group2:
>           hosts:
>             10.1.1.10[4:5]: # range of hosts
>             10.1.1.10[6:8:2]: # range and step of hosts
>         group3:
>           hosts:
>             web[1:5].example.com: # dns record
>             web[a:z].example.com: # with digits or chars
>           vars:
>             http_port: 80 # variables for group
>         group4:
>           hosts:
>             tomato: # rename a host as you like
>               ansible_host: 10.1.1.109
> 
> ```
