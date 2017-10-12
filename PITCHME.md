moby project
 - runc, HyperKit, VPNKit, SwarmKit, InfraKit, containerd, etc..
 - moby tool converts the yaml specification into one or more bootable images.

skopeo

linuxkit
 - *kernel* specifies a kernel Docker image, containing a kernel and a filesystem tarball, eg containing modules. The example kernels are built from kernel/
 - *init* is the base init process Docker image, which is unpacked as the base system, containing init, containerd, runc and a few tools. Built from pkg/init/
 - *onboot* are the system containers, executed sequentially in order. They should terminate quickly when done.
 - *services* is the system services, which normally run for the whole time the system is up
 - *files* are additional files to add to the image


linuxkit image
 - platform-aws.md
 - platform-azure.md
 - platform-gcp.md
 - platform-hyperkit.md 
 - platform-hyperv.md
 - platform-openstack.md
 - platform-packet.md
 - platform-qemu.md
 - platform-vmware.md

linuxkit kernel config
 - https://github.com/linuxkit/linuxkit/tree/master/kernel
 - https://github.com/linuxkit/linuxkit/blob/master/docs/kernels.md

Alpine Linux History
 - LRP -> LEAF -> Alpine
 - Alpine was originally built with Gentoo
 - apk: evaluated pacman from Arch Linux, .deb, ipkg, .rpm and others
   - “Our main requirement was that it should have only a few files as the full state — all others usually had one or more files per installed package,”


https://thenewstack.io/alpine-linux-heart-docker/

 Natanael Copa: "The idea was that the system was installed in memory during boot from a read-only media and that you could remove the boot media once it was booted"
 - security-oriented
   - (grsec/PaX)[https://grsecurity.net/features.php] patches
 - core utilities:
   - musl libc
   - BusyBox
 - bootloader: syslinux
 - init system: openrc
 - installation modes: sys/diskless/data
   - lbr (Alpine local backup)

disposable container concept

Alpine and Containers:
 - before docker
   - alpine-vserver flavor
   - LXC

package
 - Alpine Package Keeper
    - “since the system was installed from scratch every reboot we needed a package manager that was fast too,” said Copa.
   - “The major reason that we ended up with our own is our ‘run-from-ram’ requirement. We needed a fast manager that can set up tmpfs rootfs from initfs.”
 - aports: a tree of ported applications for the distro

sub-projects
 - linux-okernel

https://docs.docker.com/engine/userguide/eng-image/multistage-build/

runc

ostree vs alpine

