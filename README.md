About
-----
This is template configuration for building and executing short lived stress testing environments in EC2. The purpose is to automate the following steps:

1. Build a given number of instances.
2. Apply configuration.
3. Start stress testing.
4. Terminate the instances when done.

Configuration
-------------
Put the following in ``host_vars/localhost``:

    ec2_access_key: "ACCESS_KEY"
    ec2_secret_key: "SECRET_KEY"
    keypair: "KEYPAIR_NAME"
    instance_type: "m3.medium"
    image: "ami-018c9568"
    group: "SECURITY_GROUP"
    region: "us-east-1"
    zone: "us-east-1c"
    instance_count: 10

Change the siege command to run in ``roles/siege/files/siege-exec`` and the URLs to request in ``roles/siege/files/urls.txt``.

Usage
-----

    ./run.sh

Requirements
------------

* ansible <https://github.com/ansible/ansible>
* python-boto <https://github.com/boto/boto>
* EC2 account with credentials

