# How to use

```bash
docker-compose up -d

curl -XPOST -d '{ "input": { "user": "john", "password": "secret" } }' http://localhost:8181/v1/data/foo/allow
```

Output

```
logger_1  | [
logger_1  |   {
logger_1  |     "labels": {
logger_1  |       "id": "734fe644-cfa9-4fed-9b87-dd11edbd4c8e",
logger_1  |       "version": "0.13.0"
logger_1  |     },
logger_1  |     "decision_id": "9bbf532b-b7f8-49b9-a8fd-2711c24ece70",
logger_1  |     "path": "foo/allow",
logger_1  |     "input": {
logger_1  |       "user": "john"
logger_1  |     },
logger_1  |     "result": true,
logger_1  |     "erased": [
logger_1  |       "/input/password"
logger_1  |     ],
logger_1  |     "requested_by": "172.18.0.1:54560",
logger_1  |     "timestamp": "2019-08-10T00:46:02.994297Z",
logger_1  |     "metrics": {
logger_1  |       "timer_rego_module_compile_ns": 18800,
logger_1  |       "timer_rego_module_parse_ns": 1723900,
logger_1  |       "timer_rego_query_compile_ns": 248100,
logger_1  |       "timer_rego_query_eval_ns": 206800,
logger_1  |       "timer_rego_query_parse_ns": 2582800,
logger_1  |       "timer_server_handler_ns": 5260600
logger_1  |     }
logger_1  |   }
logger_1  | ]
```