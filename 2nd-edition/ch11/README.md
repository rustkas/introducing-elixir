```code
git clone https://github.com/jeremyjh/dialyxir
$ cd dialyxir
mix deps.get
mix do compile
mix do archive.build
mix archive.install
$ mix archive.build
mix local.hex --force
$ mix archive.install
$ mix dialyzer

git clone https://github.com/jeremyjh/dialyxir && cd dialyxir &&  mix local.hex && && mix deps.update --all && mix deps.get &&  mix do compile && mix do archive.build && mix archive.install


mix new ex1-guards --app drop && cd ex1-guards && iex -S mix

mix clean
mix dialyzer

mix new ex2-specs --app specs && cd ex2-specs && iex -S mix
recompile

Specs.calculate()

mix new ex3-specs --app new_type && cd ex3-specs && iex -S mix

mix new ex4a-testing --app drop && cd ex4a-testing && iex -S mix
mix test --seed 0
mix new ex4-testing --app drop_test && cd ex4-testing && iex -S mix

mix test --seed 0 --cover --color

mix new ex5-setup --app drop_test && cd ex5-setup && iex -S mix
mix new ex6-doctest --app drop_test && cd ex6-doctest && iex -S mix
mix new zorko --app zorko && cd zorko && iex -S mix
```
