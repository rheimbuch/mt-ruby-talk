!SLIDE code
# True and False #

## false and nil are false

    @@@ ruby
    !false == true
    !nil == true

## everything else is true (including 0)
  
    @@@ ruby
    if 0 
        puts('Zero is true!')
    end

!SLIDE code

# Conditionals #

    @@@ ruby
    1 == 1            # true
    1 == 2            # false
    'cat' == 'dog'    # false
    (1 < 2)           # true
    (4 > 6)           # false
    a = 1 
    b = 10000 
    (a > b)           # false
  
!SLIDE code small
# Loops #

    @@@ ruby
    # While, Until, For

    i = 0
    while i < 10
        puts i
        i += 1
    end

    j = 10
    until j == 0
        puts j
        j -= 1
    end

    cars = ['spyder','jeep','skycar']
    for car in cars
        puts "My car is a #{car}."
    end

!SLIDE code small
# Iteration Through Enumerables #

    @@@ ruby
    bugs = ["fly","mosquito","moth","ant"]
    bugs.each do |bug|
        puts "I step on the #{bug}"
    end

    capitals = {
        'montana'    => 'helena',
        'california' => 'sacramento',
        'washington' => 'olympia',
        'illinois'   => 'springfield'
    }
    capitals.each do |state, capital|
        puts "The capital of #{state} is #{capital}."
    end

    capitals.each { |state, capital|
        puts "The capital of #{state} is #{capital}."
    }

    capitals.map{|capital| capital.upcase } #=> returns an array
    # of upper-cased capitals
