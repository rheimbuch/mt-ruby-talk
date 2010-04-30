!SLIDE code

# Classes
    @@@ ruby
	class Bug
		def alive?
			true
		end
	end
	
	ant = Bug.new
	ant.alive? # true

!SLIDE code

# Classes Execute
	@@@ ruby
	class Bug
		puts "Setting up a Bug Class"
		puts "(Not an Instance)"
		
		def alive?
			true
		end
	end
	
	=> Setting up a Bug Class
	=> (Not an Instance) 

!SLIDE code

# Inheritance

	@@@ ruby
	class Insect < Bug
		def legs
			6
		end
	end

	ant = Insect.new
	ant.alive?    # true
	ant.legs == 6 # true

!SLIDE code small

# Instance Variables

	@@@ ruby
	class Bug
		attr_reader :legs

		def initialize(legs)
			@legs = legs
			@size = 20
		end

		def alive?
			true
		end

		def size=(size_in_mm)
			@size = size_in_mm
		end

		def size
			@size
		end
	end

!SLIDE code

# Instance Variables

	@@@ ruby
	class Insect < Bug
		def initialize
			super(6)
		end
	end

	ant = Insect.new
	ant.alive? 	  # true
	ant.legs == 6 # true

!SLIDE code

# Accessors

	@@@ ruby
	attr_reader :wings
	attr_writer :name
	attr_accessor :location

!SLIDE code

<!-- Explain attr_accessor -->
# Modules

	@@@ ruby
	module Wing
		def fly!
			@flying = true
		end

		def land!
			@flying = false
		end

		def flying?
			@flying || false
		end
	end

!SLIDE code

<!-- Explain extend vs include -->
# Modules

	@@@ ruby
	class Bee < Insect
		include Wing
	end

	bee = Bee.new
	bee.flying?  # false
	bee.fly!
	bee.flying?  # true

	flying_ant = Insect.new
	flying_ant.extend(Wing)
	flying_ant.flying?  # false
	flying_ant.fly!
	flying_ant.flying?  # true
