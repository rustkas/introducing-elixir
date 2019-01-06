```code
mix new ex1-drop --app drop_server && cd ex1-drop && iex -S mix

DropServer.start_link()
GenServer.call(DropServer, 20)
GenServer.call(DropServer, 40)
GenServer.call(DropServer, 60)
GenServer.cast(DropServer, {})


 GenServer.call(DropServer, -60)
  GenServer.call(DropServer, -60) # no process

mix new ex2-drop-sup --app drop_sup && cd ex2-drop-sup && iex -S mix


{:ok, pid} = DropSup.start_link()
Process.unlink(pid)
Process.whereis(DropServer)

GenServer.call(DropServer, 60)

GenServer.call(DropServer, -60) #shut down process

GenServer.call(DropServer, 60) #ok
Process.whereis(DropServer) #new pid we have


mix new drop_app
cd drop_app
mix compile

iex -S mix
{:ok, pid} = DropServer.start_link()
elixir -pa _build/dev/lib/drop_app/ebin --app drop_app
elixir -pa _build/prod/lib/drop_app/ebin --app drop_app


```
