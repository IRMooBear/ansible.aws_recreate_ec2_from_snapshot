[![Build Status](https://travis-ci.org/IRMooBear/ansible.aws_recreate_ec2_from_snapshot.svg?branch=master)](https://travis-ci.org/IRMooBear/ansible.aws_recreate_ec2_from_snapshot)

AWS recreate EC2 from snapshot
=========

This role is used to recreate an EC2 EBS volume from snapshot.  It will detach the running EBS volume and recreate it from a defined snapshot ID.

This would primarily be used in tests where a snapshot of a pristine VM is made and need to be restored after modifications.

Requirements
------------

AWS credentials has to be defined.

Role Variables
--------------

    aws_host: my.server.name
    
FQDN of the server    
    
    aws_inventory_name: myservername
    
Short inventory name    
    
    aws_host_id:
    
AWS EC2 ID    
    
    aws_snapshot_id:
    
AWS Snapshot ID  
    
    aws_device_name: /dev/xvda
    
Mount point for EBS    
    
    aws_new_volume_type: gp2
    
EBS type when recreated    

    aws_access_key:
    aws_secret_key:
    aws_region: us-west-2
    
AWS Credentials     

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

You have to defined several variables for this role to work.  It is assume you know how to look at the documentation and source code.  This role is not that complicated, it has been tested to work.

    - hosts: servers
      roles:
         - { role: irmoobear.aws_recreate_ec2_from_snapshot }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
