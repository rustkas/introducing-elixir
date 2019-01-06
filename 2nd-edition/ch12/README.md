```code
mix new ex1-records --app records && cd ex1-records && iex -S mix

require Tower;
tower1 = Tower.tower();
tower2 = Tower.tower(location: "Grand Canyon");
tower3 = Tower.tower(location: "NYC", height: 241, name: "Woolworth Building");
tower4 = Tower.tower location: "Rupes Altat 241", height: 500, planemo: :moon, name: "Piccolini View";
tower5 = Tower.tower planemo: :mars, height: 500, name: "Daga Vallis", location: "Valles Marineris";

Tower.tower(tower5, :planemo)

import Tower
tower(tower5, :height)

tower5
tower5 = tower(tower5, height: 512)

mix new ex2-records --app record_drop && cd ex2-records && iex -S mix

mix new ex3-records --app record_drop && cd ex3-records && iex -S mix

RecordDrop.fall_velocity(tower1)
RecordDrop.fall_velocity(tower5)

mix new ex4-records --app record_drop && cd ex4-records && iex -S mix
mix new ex5-ets --app planemo_storage && cd ex5-ets && iex -S mix

PlanemoStorage.setup
PlanemoStorage.info

mix new ex6-ets --app planemo_storage && cd ex6-ets && iex -S mix

PlanemoStorage.setup
:ets.tab2list :planemos

:observer.start()

:ets.lookup(:planemos, :eris)
hd(:ets.lookup(:planemos, :eris))
result = hd(:ets.lookup(:planemos, :eris))
require Planemo
Planemo.planemo(result, :gravity)


:ets.insert(:planemos, Planemo.planemo(name: :mercury, gravity: 3.9, diameter: 4878, distance_from_sun: 57.9))
:ets.lookup(:planemos, :mercury)

mix new ex7-ets-calculator --app mph_drop && cd ex7-ets-calculator && iex -S mix

pid1 = spawn(MphDrop, :mph_drop, [])
send(pid1, {:earth, 20})
send(pid1, {:eris, 20})
send(pid1, {:makemake, 20})


:mnesia.start()
Drop.setup
:mnesia.table_info(PlanemoTable, :all)

:mnesia.transaction(fn()->:mnesia.read(PlanemoTable, :neptune) end)

      Drop.fall_velocity(:mercury, 10)
      Drop.fall_velocity(:venus, 10)
      Drop.fall_velocity(:earth, 10)
      Drop.fall_velocity(:moon, 10)
      Drop.fall_velocity(:mars, 10)
      Drop.fall_velocity(:ceres, 10)
      Drop.fall_velocity(:jupiter, 10)
      Drop.fall_velocity(:saturn, 10)
      Drop.fall_velocity(:uranus, 10)
      Drop.fall_velocity(:neptune, 10)
      Drop.fall_velocity(:pluto, 10)
      Drop.fall_velocity(:haumea, 10)
      Drop.fall_velocity(:makemake, 10)

pid1 = spawn(MphDrop, :mph_drop, [])
send(pid1, {:mercury, 10})
send(pid1, {:venus, 10})
send(pid1, {:earth, 10})
send(pid1, {:moon, 10})
send(pid1, {:mars, 10})
send(pid1, {:ceres, 10})
send(pid1, {:jupiter, 10})
send(pid1, {:saturn, 10})
send(pid1, {:uranus, 10})
send(pid1, {:neptune, 10})
send(pid1, {:pluto, 10})
send(pid1, {:haumea, 10})
send(pid1, {:makemake, 10})



```
