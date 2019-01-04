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
mix test

```
