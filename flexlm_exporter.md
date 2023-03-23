```
]~/MySoftwares/golang/go> bin/go env | grep GOPATH
GOPATH="/home/monadmin/go"
```

now download 
```
[monadmin@den-grafana-01]~/MySoftwares/golang/go> bin/go install github.com/mjtrangoni/flexlm_exporter
go: 'go install' requires a version when current directory is not in a module
        Try 'go install github.com/mjtrangoni/flexlm_exporter@latest' to install the latest version
```
retru download 
```
[monadmin@den-grafana-01]~/MySoftwares/golang/go> go install github.com/mjtrangoni/flexlm_exporter@latest
go: downloading github.com/mjtrangoni/flexlm_exporter v0.0.8
go: downloading github.com/go-kit/log v0.1.0
go: downloading github.com/prometheus/client_golang v1.11.0
go: downloading github.com/prometheus/common v0.30.0
go: downloading github.com/prometheus/exporter-toolkit v0.6.1
go: downloading gopkg.in/alecthomas/kingpin.v2 v2.2.6
go: downloading github.com/go-logfmt/logfmt v0.5.0
go: downloading gopkg.in/yaml.v3 v3.0.0-20210107192922-496545a6307b
go: downloading golang.org/x/text v0.3.6
go: downloading github.com/prometheus/client_model v0.2.0
go: downloading github.com/beorn7/perks v1.0.1
go: downloading github.com/cespare/xxhash/v2 v2.1.1
go: downloading github.com/golang/protobuf v1.5.2
go: downloading github.com/prometheus/procfs v0.6.0
go: downloading github.com/pkg/errors v0.9.1
go: downloading github.com/alecthomas/template v0.0.0-20190718012654-fb15b899a751
go: downloading github.com/alecthomas/units v0.0.0-20190924025748-f65c72e2690d
go: downloading golang.org/x/crypto v0.0.0-20210616213533-5ff15b29337e
go: downloading gopkg.in/yaml.v2 v2.4.0
go: downloading github.com/matttproud/golang_protobuf_extensions v1.0.1
go: downloading google.golang.org/protobuf v1.26.0
go: downloading golang.org/x/sys v0.0.0-20210630005230-0f9fa26af87c
go: downloading github.com/mwitkow/go-conntrack v0.0.0-20190716064945-2f068394615f
go: downloading golang.org/x/net v0.0.0-20210525063256-abc453219eb5
go: downloading golang.org/x/oauth2 v0.0.0-20210514164344-f6687ab2804c
go: downloading github.com/jpillora/backoff v1.0.0
[monadmin@den-grafana-01]~/MySoftwares/golang/go>
```
check the bin -
```
[monadmin@den-grafana-01]~/MySoftwares/golang/go> ls ~/go/bin/
flexlm_exporter
```

check the 
```
[monadmin@den-grafana-01]~/MySoftwares/golang/go> ls ~/go/pkg/mod/
cache  github.com  golang.org  google.golang.org  gopkg.in
[monadmin@den-grafana-01]~/MySoftwares/golang/go> ls ~/go/pkg/mod/g
github.com/        golang.org/        google.golang.org/ gopkg.in/
[monadmin@den-grafana-01]~/MySoftwares/golang/go> ls ~/go/pkg/mod/github.com/
alecthomas  beorn7  cespare  go-kit  golang  go-logfmt  jpillora  matttproud  mjtrangoni  mwitkow  pkg  prometheus
[monadmin@den-grafana-01]~/MySoftwares/golang/go> ls ~/go/pkg/mod/github.com/mjtrangoni
flexlm_exporter@v0.0.8
[monadmin@den-grafana-01]~/MySoftwares/golang/go> ls ~/go/pkg/mod/github.com/mjtrangoni/flexlm_exporter@v0.0.8/
CHANGELOG.md        config           flexlm_exporter.go  ISSUE_TEMPLATE.md  Makefile
CODE_OF_CONDUCT.md  CONTRIBUTING.md  go.mod              LICENSE            NOTICE
collector           Dockerfile       go.sum              MAINTAINERS.md     README.md
[monadmin@den-grafana-01]~/MySoftwares/golang/go>
```

```
]~/MySoftwares/golang/go> cd ~/go/pkg/mod/github.com/mjtrangoni/flexlm_exporter@v0.0.8/
]~/go/pkg/mod/github.com/mjtrangoni/flexlm_exporter@v0.0.8> export PATH=/MySoftwares/golang/go/bin:$PATH
```
run `make`
```
[monadmin@den-grafana-01]~/go/pkg/mod/github.com/mjtrangoni/flexlm_exporter@v0.0.8>make
>> Cleaning up
>> formatting code
>> vetting code
```



