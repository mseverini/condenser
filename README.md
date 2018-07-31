# Config

Configuration must exist in `config.json`. There is an example configuration provided in `example-config.json`. Below we describe the use of all configuration parameters.

*passthrough_threshold*: Integer specifying maximum number of rows a table can contain to be automatically considered as a passthrough table. Leave empty to disable.

*passthrough_tables*: Array of strings of all tables to be passthrough-ed

*dependency_breaks*: An array containg a JSON object with *"parent"* and *"child"* fields of table relationships to be ignored in order to break cycles

*tables*: All tables to consider.  Do not need to replicate passthrough tables in this list.

*desired_result*: JSON object containing a *"table"* and *"percent"* fields to specify desired end result.  Also contains *"required_pks"* an array of primary keys for table that must be included.

*max_tries*: Number of iterations of binary search to find optimal input table size.

# To Run
```bash
python main.py
```

# (Optional) Start Docker Container:

This starts a docker container which you can use as a destination database.

```bash
docker-compose up -d
```

To confirm it is running:
```bash
docker ps
```
