# redteam

## Tools
nuclei
```
go install -v github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest
```
subfinder
```
go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
```
httpx
```
go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest
```

## Commands
**Integrating Nuclei with Other Tools**
```
subfinder -d targetdomain.site -silent | httpx | nuclei -t http/exposures/
```

**Using Template Tags**
```
nuclei -u https://jira.targetdomain.site -tags jira,generic
```

**Filtering by Severity**
```
nuclei -u https://targetdomain.site -s critical,high,medium
```

**Custom Headers**
```
nuclei -H 'User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/125.0.0.0 Safari/537.36' -l targets.txt
```

**Limiting Requests and Threads**
```
nuclei -l targets.txt -rl 20 -c 5
```

**Saving Output**
```
nuclei -l targets.txt -o nuclei.log
```

**JSONL Output**
```
nuclei -l targets.txt -jsonl
```

****
```
```

****
```
```

****
```
```

**Updating Templates and Nuclei**
```
nuclei -up
```







