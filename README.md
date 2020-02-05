# Netlogo_Lesson1

# Create turtles

create a turtle with defult attributes:

```crt 1``` or 
```create turtles 1 ```

create a turtle with given attributes:

`create-turtles 1 [set color green
                   set shape car
                   set xcor 1
                   set ycor 2]`
 
# Create a new breed

`breed [cars car]`

`breed [passengers passenger]`

`cars-own [year speed]`

`passengers-own [satisfied]`

`globals [cars_num pass_num]`

