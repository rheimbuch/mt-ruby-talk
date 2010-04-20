<!-- Pol -->
!SLIDE code
# Variable Names #
  
  Idiomatic: max_int 
  
  Valid, but not common: maxInt
  
  Also valid: _max_int
  
  Still valid (but why!?): ___
  

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
    
    d, e, f = [1, 2, 3]
    