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

# Instance Variables 1

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

# Instance Variables 2

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

<!-- Explain attr_accessor -->
# Modules 1

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
# Modules 2

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
