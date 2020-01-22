# k8s   tested centos 7.7

1.  Installing Ansible on RHEL, CentOS, or Fedora

    On Fedora:

    $ sudo dnf install ansible

    On RHEL and CentOS:

    $ sudo yum install ansible

    RPMs for RHEL 7 and RHEL 8 are available from the Ansible Engine repository.

    To enable the Ansible Engine repository for RHEL 8, run the following command:

    $ sudo subscription-manager repos --enable ansible-2.9-for-rhel-8-x86_64-rpms

    To enable the Ansible Engine repository for RHEL 7, run the following command:

    $ sudo subscription-manager repos --enable rhel-7-server-ansible-2.9-rpms


 2. yum install git


 3. testing host menggunakan 
    ansible -i hosts -m ping all
    
 4. https://metallb.universe.tf/installation/
    
    kubectl apply -f https://raw.githubusercontent.com/google/metallb/v0.8.3/manifests/metallb.yaml

    
    ===================================================


    petunjuk install ada dibawah ini menggunakan ansible
  
    https://medium.com/@baskoro.oktianto/how-to-create-a-high-availability-vanilla-kubernetes-cluster-7e50f0c6f671
    https://howto.lintel.in/enable-disable-selinux-centos/
    https://kubernetes.io/docs/reference/kubectl/cheatsheet/
    note:
    
    /etc/selinux/config 
    if you open file you would see something like

# This file controls the state of SELinux on the system.
# SELINUX= can take one of these three values:
# enforcing – SELinux security policy is enforced.
# permissive – SELinux prints warnings instead of enforcing.
# disabled – No SELinux policy is loaded.
SELINUX=enforcing
# SELINUXTYPE= can take one of these two values:
# targeted – Targeted processes are protected,
# mls – Multi Level Security protection.
SELINUXTYPE=targeted

 	
getenforce
