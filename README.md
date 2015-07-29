StatexClient
============

Client for statex server. First, you should write config

```
config :statex_client, 
	app: "my_great_appication", 
	host: "127.0.0.1",
	statex_server: "http://127.0.0.1", # here we send data
	ttl: 1000, # interval for calling your callback
	memo_ttl: 3600000, # ttl for memorize json encoding and decoding
	callback: &StatexClient.example/0 # your callback
```

second, you should write callback, that should return %StatexClient.Info{} struct with you info

```
def example, do: %StatexClient.Info{ok: true}
```

enjoy!