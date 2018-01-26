####Settup the Environment for GO lang in Ubuntu 


Step 1 : Setup GVM (GO version Manager)
      ==>$ bash < <(curl -s -S -L https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer)
      
Step 2 : install the Dependencey 
      ==>$ sudo apt-get install bison
      ==>$ sudo apt-get install curl git mercurial make binutils bison gcc build-essential
      
Step 3 : install the Go in Ur machine
      ==>$ gvm install go1.4
   
(Credit Referance : https://github.com/moovweb/gvm ||  http://www.hostingadvice.com/how-to/install-golang-on-ubuntu/)


      
But this work for Real in AMD machine
======================================

      gvm_version=master # you may use a tag like "1.0.22" instead
 
      # Install OS level dependencies (see the GVM README for other distros)
      sudo apt-get install curl git mercurial make binutils bison gcc build-essential
 
      # Install GVM
      cd /tmp
      curl -sOSL "https://raw.githubusercontent.com/moovweb/gvm/master/binscripts/gvm-installer"
      view gvm-installer # give the "gvm-installer" script a short review
      bash gvm-installer "$gvm_version" "$HOME/.local"
      . ~/.local/gvm/scripts/gvm
 
      # Install bootstrapping version, alternatively you could do…
      #   sudo apt-get install golang
      #   export GOROOT_BOOTSTRAP=$(ls -1d /usr/lib/go-[0-9]* | tail -n1)
      gvm install "go1.4" -B
      gvm use "go1.4"
      export GOROOT_BOOTSTRAP=$GOROOT
 
      # List available go *release* versions
      gvm listall | egrep 'go[.0-9]+$'
      
      
      
(Credit Referance : https://github.com/moovweb/gvm/issues/197)
