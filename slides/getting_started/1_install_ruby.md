!SLIDE code
# Installing Ruby #

!SLIDE
# Mac #
## installed by default on Leopard ##

!SLIDE commandline
# Linux #
	apt-get install ruby
	
	-- or --
	
	download and compile
	http://www.ruby-lang.org/

	wget "ftp://ftp.ruby-lang.org/pub/ruby/1.9/ruby-1.9.1-p376.tar.gz"
	tar xvfpz ruby-1.9.1-p376.tar.gz
	cd ruby-1.9.1-p376
	./configure
	make
	sudo make install

!SLIDE
# Windows #
	download the ruby installer
	http://rubyinstaller.org/

	- check "add Ruby to your path"
