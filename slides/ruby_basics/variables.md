!SLIDE code
# puts "Storing Values" #


!SLIDE code
# Variable Types #

    @@@ ruby
    my_var = "Variables must start with [a-z]"
    camelCased = false
    FIXED = "a constant"
    @name = "instance variable"
    @@foo = "class variable"
    $global = "global variable"

!SLIDE
# Assignments
    a = 5
    b = 2
    
    b = b + 1
    # equivalent to:
    b += 1
    
    c = (c || 2)
    # equivalent to:
    c ||= 2
    