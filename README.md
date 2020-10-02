# BM-SC_VNF_Status

If BM-SC application is running on RHEL then with [pcs status commands](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/high_availability_add-on_reference/s1-pcsstatus-haar) you can display the status of the cluster and the cluster resources. If you do not specify a commands parameter, this command displays all information about the cluster and the resources.

The resources name may vary as per vendor. I picked up the resources which show Master DB and Active CP or UP instances with [grep](https://man7.org/linux/man-pages/man1/grep.1.html) and [awk](https://www.grymoire.com/Unix/Awk.html). The playbook registered the result and diplay it in a task advising that snapshots of standby nodes are recommended first if you plan to bakcup VMs/instances. 

[BM-SC_Openstack-Snapshot](https://github.com/qaswarh/BM-SC_Openstack-Snapshot) has palybook to take snapshot of VNF instance as per user input.

BM-SC group in the inventory should have all the hosts (IPs/FQDN) of VNF. ansible_connection=ssh, ansible_user=user, ansible_ssh_pass=password and ansible_sudo_pass=sudo password should also be the part of inventory

