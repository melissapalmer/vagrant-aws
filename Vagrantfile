VAGRANTFILE_API_VERSION = "2"

# Require the AWS provider plugin
require 'vagrant-aws'

# Create and configure the AWS instance(s)
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  # Use dummy AWS box
  config.vm.box = 'aws/dummy'
  
  config.ssh.username = "ubuntu"
  
  # Being asked for details for SMB details
  config.vm.synced_folder ".", "/vagrant", disabled: true  

  # Specify configuration of AWS provider
  config.vm.provider 'aws' do |aws, override|
    aws.access_key_id = ENV['AWS_ACCESS_KEY']
    aws.secret_access_key = ENV['AWS_SECRET_KEY']
    
    # Specify SSH keypair to use
    aws.keypair_name = 'aws_key_nopass'
    
     # Specify region, AMI ID, and security group(s)
    aws.region = "eu-central-1"
    aws.ami = "ami-de8fb135"
    aws.instance_type = "t2.micro"
    aws.security_groups = ['vagrant-group']  
    
    # Specify username and private key path
    override.ssh.username = 'ubuntu'
    override.ssh.private_key_path = 'ssh/aws_key_nopass.pem'
    
  end # config.vm.provider 'aws'
end # Vagrant.configure