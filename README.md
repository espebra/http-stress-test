Configuration
-------------
Put the following in host_vars/localhost:

    ec2_access_key: "ACCESS_KEY"
    ec2_secret_key: "SECRET_KEY"
    keypair: "KEYPAIR_NAME"
    instance_type: "m3.medium"
    image: "ami-018c9568"
    group: "SECURITY_GROUP"
    region: "us-east-1"
    zone: "us-east-1c"
    instance_count: 10

