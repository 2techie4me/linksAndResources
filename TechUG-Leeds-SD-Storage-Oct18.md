# Software defined Storage - Navigating the Brave New World #

On the 18th October 2018 I presented a session at the [TechUG](https://www.technologyug.co.uk/) [Leeds Event](https://www.technologyug.co.uk/Communities/Leeds) on the subject of Software Defined Storage.
Below are the "further reading" links and resources so that those with an inquiring mind can dig a little deeper.

## Synopsis: ##
All computer storage, from a vendor propriatory array to a open-source scale-out Ceph cluster, relies on layer upon layer of software from the physical disk drives upwards. How "software defined" a storage solution is boils down to how much of the functionality of the software has been exposed for the consumption of the programs and scripts the ITOps and development folks are using.

## General Reading ##

* Software Defined Infrastructure drives the on-prem part of your Cloud Strategy: [Why do we need it?](https://packetpushers.net/podcast/datanauts-147-whats-your-private-cloud-strategy/) 

* [Software Defined Storage](https://en.wikipedia.org/wiki/Software-defined_storage), defined as per Wikipedia - always a good place to start

* Strong, light and cheap - choose two! What have Mountainbike frames to do with IT Infrastructure? Well, it's just a way of [expressing the constraints](https://medium.com/@devsociety_/good-cheap-fast-pick-two-and-how-ngos-can-play-the-triangle-like-a-pro-20d1380884a8) and highlighting that different priorities will influence the amount of risk or spend organizations are willing to bear in order to go faster and improve time to market.

* Dan Young from EngineerBetter Consultancy writes about ["Escaping the Iron Triangle"](http://www.engineerbetter.com/blog/escaping-iron-triangle/) - the triangle is bound by speed, cost and user experience. Have a think about your own organization's ["time to hello world"](https://cloud.google.com/blog/products/gcp/time-to-hello-world-vms-vs-containers-vs-paas-vs-faas) how agile are you?

* Cross Functional Teams will save us from the Four Horsemen of the IT Ops Apocalypse, [see the article on Newstack.io](https://thenewstack.io/cloud-native-devops-four-horsemen-of-the-operations-apocalypse/), but breaking down the siloes means infrastructure needs to become abstracted and programmable.

## A Selection Of Storage Ecosystem Software Partners ##

* [VMware VSAN](https://www.vmware.com/uk/products/vsan.html) and [Microsoft Storage Spaces Direct](https://docs.microsoft.com/en-us/windows-server/storage/storage-spaces/storage-spaces-direct-overview) - No escaping the fact that they are the obvious choice for a lot of customers already invested in that particular stack. Both bring "hyperconvergence" to their respective family of hypervisor / server software. VMware now able to bridge environments, including the storage, into VMware real estate in AWS. Microsoft have ["Azure Data Box"](https://azure.microsoft.com/en-gb/services/storage/databox/) for on-prem Azure managed storage, and more convergence to come. MS Server 2019 to have native Kubernetes support. VMware have just acquired Heptio. Hybrid cloud is starting to get figured out.

* [Qumulo](https://qumulo.com/) - scale-out NAS. If you need a large POSIX compatible filesystem for billions of small files or to run traditional applications against, this one is hard to beat. Even as a big scratch file for your data analytics workloads there's a lot to like. Can be thought of as a [next generation EMC Isilon or NetApp Filer](https://qumulo.com/resources/its-your-space-you-can-use-all-of-it/). Cached and accelerated metadata for your file storage means your "ls -l" won't take 5 minutes to return a result. Sits really well as multi-tiered filesystem behind your Splunk! logging servers or your CCTV video repository. To make the purchasing easier Qumulo can be bought as "tee-shirt" sized ["storage appliance" building blocks](https://qumulo.com/product/capacity/hpe/), with hardware, software subscriptions and support bundled together, from HPE and others.

* [Hedvig](https://www.hedvig.io/product#hedvig-distributed) - Distributed storage platform that can be deployed as Hyperconverged on the server itself, as a storage appliance on x86 hardware or as a smart layer on top of your public cloud storage service. Offers block, object and file services for any OS, hypervisor or Container platform. Universal Storage Fabric means you can run workloads with app and storage portability across clouds, clusters and resource pools. Worth a look. 

* [Portworx](https://portworx.com/) - Container-centric storage volume service. Almost like a storage "middleware" to abstract away the sharp edges of your storage arrays, pools, cloud resources and let the containerized apps consume a standardized storage service. [Simplifies database and KVS designs](https://portworx.com/use-case/databases/) by abstracting away the resilience traditionally provided by redundant database engines into the storage layer.

* [Scality](https://www.scality.com/products/ring/) and [Cloudian](https://cloudian.com/) - Object storage for large scale-out deployments into the 100's of Petabytes and beyond.

* [RedHat Ceph](https://www.redhat.com/en/technologies/storage/ceph) and [SUSE Enterprise Storage](https://www.suse.com/products/suse-enterprise-storage/) - The two major Linux distro's each have an increasingly Enterprise focussed software proposition built out of the Ceph project and enhanced with aditional provisioning (Ansible and Salt respectively), monitoring and administration tools. Redhat still seemingly differentiates between Object and File with Ceph and [Gluster](https://www.redhat.com/en/technologies/storage/gluster) as seperate offerings. SUSE has a Ceph Object back-end but has native object, CephFS iSCSI, NFS and SMB/CIFS gateways to facilitate multiple use-cases. These solutions can deliver exceptional bang for buck due to the software cost coming from "node" based support (the software itself is free open-source!) rather than capacity based subscriptions as per other vendors.

## Emerging Technologies ##

* My Fellow TechUG guest presenter Alex Gallagher has put together an [extensive list](https://www.bytesizedalex.com/techug-october-2018/) of resources to accompany his deep dive into the latest hardware technologies in the world of storage. Highly recommended.

* [Gen-Z](https://www.nextplatform.com/2018/02/15/gen-z-interconnect-ready-restore-compute-memory-balance/). A scalable memory bus interconnect that will radically change the computer architecture and restore the balance between memory and CPU.

## See you at the next [TechUG](https://www.technologyug.co.uk/) in either Manchester or Leeds
IanV Nov 2018

<a href="https://twitter.com/2techie4me?ref_src=twsrc%5Etfw" class="twitter-follow-button" data-show-count="false">Follow @2techie4me on Twitter</a><script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
