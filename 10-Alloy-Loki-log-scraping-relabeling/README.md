# How to run and analyze

To use the current example, which leverages *log* 
1. scraping, 
2. relabeling, and 
3. writing to Loki 

via Alloy and allows us to analyze logs in the Grafana frontend. Make sure to run Alloy from within the root folder of the project.

The most critical step is to reference the proper log file path in the component `local.file_match`, so make sure the component `loki.source.file` references the correct log file. 
Otherwise, no logs will be sent to Loki and you won't see any logs when querying it via Grafana.

To simulate new log entries, you can use the following echo:

```shell
    # make sure to run them from within the root folder of the project
    echo 'level=info msg="INFO: This is an info level log!"' >> ./tmp/alloy-logs/log.log
    echo 'level=warn msg="WARN: This is a warn level log!"' >> ./tmp/alloy-logs/log.log
    echo 'level=debug msg="DEBUG: This is a debug level log!"' >> ./tmp/alloy-logs/log.log
```

