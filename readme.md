# Packer Builds
Packer templates to install various components

## Prerequisites

You need the following to run the template:

1. [Packer](https://packer.io/docs/installation.html)

OSX install - `brew install packer`

Windows install - `chocolatey install packer`

## Building from the template file
Execute `packer` to run a template:

```
packer build -var-file=nginx_vars.json nginx_app.json
```

#### Debugging
Either set an environmental variable for `PACKER_LOG=1` or use the `-debug` flag:
```
packer build -debug -var-file=nginx_vars.json nginx_app.json
```

## Performance
Testing shows an instance type optimized for high network performance (such as `m5.large`) can reduce run times
by 33% compared to instance types with low to moderate network performance. More info for instance types can be found [here](https://aws.amazon.com/ec2/instance-types/)
