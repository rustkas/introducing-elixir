```code
mix new ex1a-tryCatch --app drop && cd ex1a-tryCatch && iex -S mix
Drop.fall_velocity(:earth, 20)
Drop.fall_velocity(:earth, -20)
Drop.fall_velocity(:jupiter, 20)

mix new ex1b-tryCatch --app drop && cd ex1b-tryCatch && iex -S mix

mix format mix.exs "lib/**/*.{ex,exs}" "test/**/*.{ex,exs}"

Drop.fall_velocity(:jupiter, 20)


mix new ex1c-tryCatch --app drop && cd ex1c-tryCatch && iex -S mix
Drop.fall_velocity(:earth, -20)
Drop.fall_velocity(:jupiter, 20)
Drop.fall_velocity(:earth, :twelwe)
Drop.fall_velocity(:earth, 1.0)
Drop.fall_velocity(:earth, "1.0")
Drop.fall_velocity(:earth, '1.0')

mix new ex1d-tryCatch --app drop && cd ex1d-tryCatch && iex -S mix
Drop.fall_velocity(:earth, -20)


require Logger
counter=255
Logger.info("About to begin test")
Logger.debug("Current value of counter is #{counter}")
Logger.warn("Connection lost; will retry.")
Logger.error("Unable to read database.")

alias :dbg, as: Dbg

mix new ex2-debug --app mph_drop && cd ex2-debug && iex -S mix

:dbg.tracer()
pid1 = spawn(MphDrop, :mph_drop, [])
:dbg.p(pid1, :m)
send(pid1, {:moon, 20})

mix new ex3-debug --app fact && cd ex3-debug && iex -S mix
:dbg.tracer()
:dbg.p(:all, :c)

:dbg.tpl(Fact, :factorial, [])


```
