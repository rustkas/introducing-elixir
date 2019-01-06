```code
mix new ex1-difference --app difference && cd ex1-difference && iex -S mix

require Difference
Difference.f_test(1 + 3)
Difference.m_test(1 + 3)

mix new ex2-double --app double && cd ex2-double && iex -S mix

require Double;
Double.double(3)

quote do: 1 + 3
quote do: 3 * x + 20

require BadDouble
BadDouble.double(3)

mix new ex3-double --app double && cd ex3-double && iex -S mix
require Double;
Double.double(3)

mix new ex4-unless --app logic && cd ex4-unless && iex -S mix

require(Logic)
Logic.unless (4 == 5) do
IO.puts("arithmetic still works")
end
mix new ex5-programmatic --app multiply && cd ex5-programmatic && iex -S mix

Multiply.double(21)
Multiply.triple(54)
Multiply.example()

mix new ex6-multidrop --app drop && cd ex6-multidrop && iex -S mix


```
