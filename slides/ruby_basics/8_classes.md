<!-- Ryan S -->
!SLIDE

# Classes
    @@@ ruby
	class Bug
		def alive?
			true
		end
	end
	
	ant = Bug.new
	ant.alive? # true
	
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
	
	class Insect < Bug
		def initialize
			super(6)
		end
	end
	
	ant = Insect.new
	ant.alive? 	  # true
	ant.legs == 6 # true

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
	
	<!-- Explain extend vs include -->
	