# Netlogo_Lesson1

# Create turtles

Create a turtle with defult attributes:

```crt 1``` or 
```create turtles 1 ```

Create a turtle with given attributes:

```
create-turtles 1 [set color green
                  set shape car
                  set xcor 1
                  set ycor 2]
```
 
# Breeds and variables

```
breed [cars car]
breed [passengers passenger]
cars-own [year speed]
passengers-own [satisfied]
globals [cars_num pass_num]

create-cars 5
[set color green
 set shape car
 ]
 create-passengers 50
 [set color red
  set shape person
  set satisfied false
 ]
```

# functions

```
to go
ca
ask cars [fd 1] 
end
```

```
to go
ca
ask cars with [color = green][fd 1] 
end
```

# Call specific agent or  agentset

`one-of`
`min-one-of`
`with`

# Interaction between agnets
```
to go
ca
ask cars with [color = green][
let target one-of passngers with [satisfied = false]
move-to target
ask target [set color white 
            set satisfied true]
           ] 
end
```
# Ticks
