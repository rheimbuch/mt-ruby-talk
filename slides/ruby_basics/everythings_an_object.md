!SLIDE
# Everything's an Object #

!SLIDE

    @@@ ruby
    2 + 2 #=> 4
    2.+(2) #=> 4
    
    "hi" << " there" #=> "hi there"
    "hi".<<(" there") #=> "hi there"
    
    
    "hi".class #=> String
    
    2.class #=> Fixnum
    2.class.superclass #=> Integer
    2.class.class #=> Class
    
    
    
    