```code
self()
send(self(), :test1)
pid = self()
send(pid, :test2)

flush()
flush()

send(self(), :test1)

receive do
x -> x
end

send(self(), 23)

 receive do
 y -> 2 * y
 end
46

mix new ex1-simple --app bounce && cd ex1-simple && iex -S mix

pid = spawn(Bounce, :report, [])
send(pid, 23)

mix new ex2-recursion --app bounce && cd ex2-recursion && iex -S mix

pid2 = spawn(Bounce, :report, [])
send(pid2, 23)

Bounce.do_send(pid2)

mix new ex3-counter --app bounce && cd ex3-counter && iex -S mix

pid2 = spawn(Bounce, :report, [1])
send(pid2, :test)
Bounce.do_send(pid2)

mix new ex4-state --app bounce && cd ex4-state && iex -S mix
pid2 = spawn(Bounce, :report, [1])
send(pid2, :test)
Bounce.do_send(pid2)

pid1 = spawn(Bounce, :report, [1])
Process.register(pid1, :bounce)
send(:bounce, :hello)

send(:zingo, :test)

get_bounce = Process.whereis(:bounce)
send(get_bounce, "Still there?")

Process.registered

mix new ex5-division --app bounce && cd ex5-division && iex -S mix

pid3 = spawn(Bounce, :report, [])
send(pid3, 38)
send(pid3, 27.56)

send(pid3, :seven) # process raised an exeption
send(pid3, 14)

mix new ex6-talking --app drop && cd ex6-talking && iex -S mix
 pid1 = spawn(Drop, :drop, [])
 send(pid1, {self(), :moon, 20})
 
 flush()
 
 mix new ex7-talkingProcs --app mph_drop && cd ex7-talkingProcs && iex -S mix

pid1 = spawn(MphDrop, :mph_drop, [])
send(pid1, {:earth, 20})
send(pid1, {:mars,  20})


:observer.start

mix new ex8-linking --app mph_drop && cd ex8-linking && iex -S mix

:observer.start()
pid1 = spawn(MphDrop, :mph_drop, [])
send(pid1, {:moon, :zoids})

Process.exit(pid1,:kill)


mix new ex9-trapping --app mph_drop && cd ex9-trapping && iex -S mix
pid1 = spawn(MphDrop, :mph_drop, [])
send(pid1, {:moon, 20})
send(pid1, {:moon, :zoids})


mix new ex10-resilient --app mph_drop && cd ex10-resilient && iex -S mix

pid1 = spawn(MphDrop, :mph_drop, [])
send(pid1, {:moon, 20})
send(pid1, {:mars, 20})

send(pid1, {:mars, :zoids})
send(pid1, {:moon, 20})


```
