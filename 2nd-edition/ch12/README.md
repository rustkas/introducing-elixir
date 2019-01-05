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

```
