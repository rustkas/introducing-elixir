```code
fall_velocity = fn(distance) -> :math.sqrt(2 * 9.8 * distance) end
fall_velocity.(20)
fall_velocity.(200)

mix new ex1-hof --app hof && cd ex1-hof && iex -S mix

my_function = fn(value) -> 20 * value end
Hof.tripler(6, my_function)
Hof.tripler(6, fn(value) -> 20 * value end)

ampersand_function = &(20 * &1)
Hof.tripler(6, ampersand_function)
Hof.tripler(6, &(20 * &1))

 x = 20
 my_function2 = fn(value) -> x * value end
 x = 0
 my_function2.(6)
 
  x = 20
  my_function3 = &(x * &1)
  x = 0
 Hof.tripler(6, my_function3)
 
 Hof.tripler(:math.pi, &:math.cos(&1))
 
 print = fn(value) -> IO.puts(" #{value}") end
 list = [1, 2, 4, 8, 16, 32]
 Enum.each(list, print)
 
 square = &(&1 * &1)
 Enum.map(list, square)
 Enum.each(list, square)

Enum.map(1..3, square)
Enum.map(-2..2, square)
Enum.map(?a..?d, square)

for value <- list, do: value * value
for value <- 1..3, do: value * value

four_bits = fn(value) -> (value >= 0) and (value < 16) end
Enum.filter(list, four_bits)
for value <- list, value >= 0, value < 16, do: value

Enum.partition(list, four_bits)


int? = fn(value) -> is_integer(value) end

Enum.all?(list, int?)
Enum.any?(list, int?)

greater_than_ten? = &(&1 > 10)

Enum.all?(list, greater_than_ten?)
Enum.any?(list, greater_than_ten?)

compare = fn(value) -> value > 10 end
Enum.partition(list, compare) # depricated. use Enum.split_with/2
Enum.split_with(list, compare)


test = &(&1 < 4)

Enum.drop_while([1, 2, 4, 8, 4, 2, 1], test)



sumsq = fn(value, accumulator) -> accumulator + value * value end
List.foldl([2, 4, 6], 0, sumsq)
List.foldr([2, 4, 6], 0, sumsq)

divide = fn(value, accumulator) -> value / accumulator end
 1/2/4/8/16/32
 List.foldl(list, 1, divide)
 32/16/8/4/2/1
 List.foldr(list, 1, divide)
 
 
```
