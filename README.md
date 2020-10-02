# BM-SC_VNF_Status

If BM-SC application is running on RHEL then [pcs status commands](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/high_availability_add-on_reference/s1-pcsstatus-haar) you can display the status of the cluster and the cluster resources with the following command. If you do not specify a commands parameter, this command displays all information about the cluster and the resources.

The resources name may vary as per vendor. I picked up the resources which show Master DB and Active CP or UP instances with grep and awk. The playbook registered the resuld and diplay it in a task advising that snapshots of standby nodes are recommended first if you plan to bakcup VMs/instances. 

BM-SC_Openstack-Snapshot has palybook to take snapshot of VNF instance as per user input.
