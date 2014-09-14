Vagrant.configure("2") do |config|
	config.vm.box="opscode_centos-5.10"
#  config.berkshelf.enabled = true
	config.vm.box_url='http://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_centos-5.10_chef-provisionerless.box'
	config.omnibus.chef_version=:latest
	config.vm.provision :chef_client do |chef|
		chef.provisioning_path='/Users/jim.sun/.ssh'
		chef.chef_server_url='https://api.opscode.com/organizations/jimworkday'
		chef.validation_key_path='.chef/jimworkday-validator.pem'
		chef.validation_client_name='jimworkday-validator'
		chef.node_name="server"
	end
end

