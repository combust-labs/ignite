## ignite vm create

Create a new VM without starting it

### Synopsis


Create a new VM by combining the given image and kernel.
Various VM tunables can be set during creation by using
the flags for this command. The image and kernel are
matched by prefix based on their ID and name.

If the name flag (-n, --name) is not specified,
the VM is given a random name. Using the copy files
flag (-f, --copy-files), additional files can be added to
the VM during creation with the syntax /host/path:/vm/path.

Example usage:
	$ ignite create my-image my-kernel \
		--name my-vm \
		--cpus 2 \
		--memory 2048 \
		--size 6GB


```
ignite vm create <image> [flags]
```

### Options

```
      --config string        Specify a path to a file with the API resources you want to pass
  -f, --copy-files strings   Copy files from the host to the created VM
      --cpus uint            VM vCPU count, 1 or even numbers between 1 and 32 (default 1)
  -h, --help                 help for create
  -k, --kernel string        Specify a kernel to use. By default this equals the image name
      --kernel-args string   Set the command line for the kernel (default "console=ttyS0 reboot=k panic=1 pci=off ip=dhcp")
      --memory size          Amount of RAM to allocate for the VM (default 512MB)
  -n, --name string          Specify the name
  -s, --size size            VM filesystem size, for example 5GB or 2048MB (default 4GB)
      --ssh[=<path>]         Enable SSH for the VM. If <path> is given, it will be imported as the public key. If just '--ssh' is specified, a new keypair will be generated. (default is unset, which disables SSH access to the VM)
```

### Options inherited from parent commands

```
  -q, --quiet   The quiet mode allows for machine-parsable output, by printing only IDs
```

### SEE ALSO

* [ignite vm](ignite_vm.md)	 - Manage VMs
