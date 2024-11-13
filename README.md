Eh? TODO!

```elixir
ducks =
  for i <- 1..:erlang.system_info(:dirty_io_schedulers) do
    DuxDB.open(":memory:", %{"max_memory" => "1GB"})
  end

{:ok, _pid} = DuxDB.Pool.start_link(ducks: ducks, name: QUAKE)
DuxDB.Pool.query(QUAKE, "select 1 + $num", %{"num" => 2})
```
