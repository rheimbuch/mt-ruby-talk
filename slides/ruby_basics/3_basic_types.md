!SLIDE code
# Simple Types #
    
    @@@ ruby
    # Strings
    "hello world!"       #=> "hello world"
    'single quotes work' #=> "single quotes work"
    %{more string "literals"} #=> "more string \"literals\""

    # Variable interpolation
    "the value of the variable is #{variable}"
    
    # Numbers
    5000   #=> Fixnum
    50.00  #=> Float
    2e-5   #=> Float
    
    # Boolean
    true
    false

!SLIDE code
# Arrays #

    @@@ ruby
    colors = ['red', 'green', 'blue']
    
    empty = []
    
    mixed = [1, 'two', 3, 3.14]
    
    mixed.size  #=> 4
    
    mixed << 'append'
    mixed[7] = 'arrays are dynamic'
    
    mixed #=> [1, "two", 3, 3.14, 'append', nil, nil, "arrays are dynamic"]


!SLIDE code
# Hashes #

    @@@ ruby
    colors = {'blue' => 0x0000FF,
              'red' => 0xFF0000,
              'green => 0x00FF00 }
    
    empty = {}
    
    mixed = {1 => 'one',
             'two' => 2}
    
    mixed.size  #=> 2
    
    mixed['new_key'] = 'seven'
    
    mixed #=> {1 => 'one', 'two' => 2, 'new_key' => 'seven'}
    
!SLIDE

[fluffy cat picture]

!SLIDE code
# Symbols #

    * Prefixed with ':'
    * Light-weight, immutable strings
    * Often used as hash keys

!SLIDE code
# Symbols Continued #

    @@@ ruby
    "a string".object_id #=> 273821
    "a string".object_id #=> 345637
    
    :a_symbol.object_id #=> 23543
    :a_symbol.object_id #=> 23543

!SLIDE code
# Other Unusual Types #

## Ranges ##
 
    @@@ ruby
    (1..6).class # Range
    (1..6).each do |num|
      puts num
    end
 
## Regular Expressions ##
  
    @@@ ruby
    /old/.class # Regexp
    "the quick brown fox" =~ /quick/ #=> 4


