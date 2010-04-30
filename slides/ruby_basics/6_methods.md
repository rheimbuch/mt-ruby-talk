!SLIDE code
# Defining Methods #

    @@@ ruby
    def hello_world
        puts "Hello World"
    end
    
!SLIDE code

    @@@ ruby
    def hello(name)
        puts "Hello #{name}"
    end

!SLIDE code

    @@@ ruby
    def hello2(name="World")
        puts "Hello #{name}"
    end


!SLIDE code
# Calling Methods #

    @@@ ruby
    hello_world()
    #=> nil
    Hello World
    
    hello_world
    #=> nil
    Hello World

!SLIDE code
    
    @@@ ruby
    hello("World")
    #=> nil
    Hello World
    
    hello "World"
    #=> nil
    Hello World
    
!SLIDE code

    @@@ ruby
    hello2
    #=> nil
    Hello World
    
    hello2 "Everyone"
    #=> nil
    Hello Everyone

!SLIDE code

# Return Values #
## Methods return the last expression executed ##

    @@@ ruby
    def method_return
        a = 5 + 2
        4
    end

    method_return #=> 4

    def explicit_return
        return 5
        puts "This is never executed"
    end
    
    explicit_return  #=> 5