Vagrant.configure("2") do |config|
  config.vm.box      = 'raring64'
  config.vm.box_url  = 'http://cloud-images.ubuntu.com/vagrant/raring/current/raring-server-cloudimg-amd64-vagrant-disk1.box'
  config.vm.hostname = 'makes.dev'
  config.vm.network    'forwarded_port', guest: 80, host: 8080, auto_correct: true
# create git user and home directory
# install git
#   https://www.digitalocean.com/community/articles/how-to-set-up-a-private-git-server-on-a-vps
# install docker
#   http://docs.docker.io/en/latest/installation/ubuntulinux/#ubuntu-raring
#   https://www.digitalocean.com/community/articles/how-to-install-docker-on-ubuntu-13-04-x64-vps
# create /deploys
# install varnish 
#   http://www.linuxsystemhacks.com/2013/08/how-to-install-varnish-reverse-proxy-on.html#.UlICxWR_XBg

  config.vm.provision :shell, inline: <<-SHELL

  SHELL

  config.vm.provider :virtualbox do |vb|
    vb.customize [
      "setextradata",
      :id,
      "VBoxInternal2/SharedFoldersEnableSymlinksCreate/v-root",
      "1"
    ]
  end 
end

