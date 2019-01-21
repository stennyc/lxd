# lxd
LXD profiles and examples. This repo contains lxc profiles to create different boxes where where each profile represent simple capability, mount, resource or contraint. This helps me up to define my lxc machines. For example one box capable of running for kvm & GUI applications, another one for nesting docker containers, third for binary forensics which shall be inspected in isolated environment etc.

## Structure
###### Directories
*profiles/* - contains lxc profiles to be loaded. Profiles contains variosu capabilities or aspects that can be associated with containers.

*for-launching/* - contains launching script for various lxc boxes/machines. Normally scripts are using profiles to define the machine.

*for-host/* - additional things that might be needed to be executed on the host before using machine or profile. Rare stuff.

*for-containers/* - resources/configuration files that can be mounted in containers.

`cd <directory` to look what is inside each directory.

## Todo
- [x] Example of passthrough of a lvm volume
- [ ] Example of passthrough of IOMMU group of mouse & keyboard (extra mouse & keyboard attached where host does not load kernel driver for it) 
- [ ] Example of passthrough of GPU in multi GPU setup where LXC/KVM using that gpu and monitor output.
- [ ] Profile with network sitting directly to switch. (macvtap)
- [ ] Profile with network managed by dedicated wifi dongle (perhap IOMMU passthough is needed)
- [ ] Profile with TOR network
