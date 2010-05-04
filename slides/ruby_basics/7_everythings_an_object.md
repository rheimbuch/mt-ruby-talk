!SLIDE code
# Everything's an Object #

!SLIDE code
# Everything's an Object #

    @@@ ruby
    2 + 4 #=> 6
    2.+(4) #=> 6
    
    "hi" + " there" #=> "hi there"
    "hi".+(" there") #=> "hi there"
    
    
    "hi".class #=> String
    
    2.class #=> Fixnum
    2.class.superclass #=> Integer
    2.class.class #=> Class
