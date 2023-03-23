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

dd
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
go: downloading github.com/golangci/golangci-lint v1.48.0
go: downloading github.com/fatih/color v1.13.0
go: downloading github.com/gofrs/flock v0.8.1
go: downloading github.com/spf13/cobra v1.5.0
go: downloading github.com/spf13/pflag v1.0.5
go: downloading github.com/spf13/viper v1.12.0
go: downloading gopkg.in/yaml.v3 v3.0.1
go: downloading github.com/mattn/go-colorable v0.1.12
go: downloading github.com/mattn/go-isatty v0.0.14
go: downloading golang.org/x/tools v0.1.12
go: downloading github.com/go-critic/go-critic v0.6.3
go: downloading github.com/hashicorp/go-version v1.6.0
go: downloading github.com/ldez/gomoddirectives v0.2.3
go: downloading github.com/mitchellh/go-homedir v1.1.0
go: downloading github.com/hashicorp/go-multierror v1.1.1
go: downloading github.com/stretchr/testify v1.8.0
go: downloading github.com/sirupsen/logrus v1.9.0
go: downloading github.com/go-xmlfmt/xmlfmt v0.0.0-20191208150333-d5b6f63a941b
go: downloading github.com/golangci/revgrep v0.0.0-20220804021717-745bb2f7c2e6
go: downloading github.com/fsnotify/fsnotify v1.5.4
go: downloading github.com/mitchellh/mapstructure v1.5.0
go: downloading github.com/spf13/afero v1.8.2
go: downloading github.com/spf13/cast v1.5.0
go: downloading github.com/spf13/jwalterweatherman v1.1.0
go: downloading golang.org/x/sys v0.0.0-20220722155257-8c9f86f7a55f
go: downloading github.com/go-toolsmith/astcast v1.0.0
go: downloading github.com/go-toolsmith/astcopy v1.0.0
go: downloading github.com/go-toolsmith/astequal v1.0.1
go: downloading github.com/go-toolsmith/astfmt v1.0.0
go: downloading github.com/go-toolsmith/astp v1.0.0
go: downloading github.com/go-toolsmith/strparse v1.0.0
go: downloading github.com/go-toolsmith/typep v1.0.2
go: downloading github.com/quasilyte/go-ruleguard v0.3.16-0.20220213074421-6aa060fab41a
go: downloading github.com/quasilyte/regex/syntax v0.0.0-20200407221936-30656e2c4a95
go: downloading golang.org/x/mod v0.6.0-dev.0.20220419223038-86c51ed26bb4
go: downloading github.com/hashicorp/errwrap v1.0.0
go: downloading 4d63.com/gochecknoglobals v0.1.0
go: downloading github.com/Antonboom/errname v0.1.7
go: downloading github.com/Antonboom/nilnil v0.1.1
go: downloading github.com/BurntSushi/toml v1.2.0
go: downloading github.com/Djarvur/go-err113 v0.0.0-20210108212216-aea10b59be24
go: downloading github.com/GaijinEntertainment/go-exhaustruct/v2 v2.2.2
go: downloading github.com/OpenPeeDeeP/depguard v1.1.0
go: downloading github.com/alexkohler/prealloc v1.0.0
go: downloading github.com/alingse/asasalint v0.0.11
go: downloading github.com/ashanbrown/forbidigo v1.3.0
go: downloading github.com/ashanbrown/makezero v1.1.1
go: downloading github.com/bkielbasa/cyclop v1.2.0
go: downloading github.com/blizzy78/varnamelen v0.8.0
go: downloading github.com/bombsimon/wsl/v3 v3.3.0
go: downloading github.com/breml/bidichk v0.2.3
go: downloading github.com/breml/errchkjson v0.3.0
go: downloading github.com/butuzov/ireturn v0.1.1
go: downloading github.com/charithe/durationcheck v0.0.9
go: downloading github.com/daixiang0/gci v0.6.2
go: downloading github.com/denis-tingaikin/go-header v0.4.3
go: downloading github.com/esimonov/ifshort v1.0.4
go: downloading github.com/firefart/nonamedreturns v1.0.4
go: downloading github.com/fzipp/gocyclo v0.6.0
go: downloading github.com/golangci/check v0.0.0-20180506172741-cfe4005ccda2
go: downloading github.com/golangci/dupl v0.0.0-20180902072040-3e9179ac440a
go: downloading github.com/golangci/go-misc v0.0.0-20220329215616-d24fe342adfe
go: downloading github.com/golangci/gofmt v0.0.0-20190930125516-244bba706f1a
go: downloading github.com/golangci/lint-1 v0.0.0-20191013205115-297bf364a8e0
go: downloading github.com/golangci/maligned v0.0.0-20180506175553-b1d89398deca
go: downloading github.com/golangci/misspell v0.3.5
go: downloading github.com/golangci/unconvert v0.0.0-20180507085042-28b1c447d1f4
go: downloading github.com/gordonklaus/ineffassign v0.0.0-20210914165742-4cc7213b9bc8
go: downloading github.com/gostaticanalysis/forcetypeassert v0.1.0
go: downloading github.com/gostaticanalysis/nilerr v0.1.1
go: downloading github.com/hexops/gotextdiff v1.0.3
go: downloading github.com/jgautheron/goconst v1.5.1
go: downloading github.com/jingyugao/rowserrcheck v1.1.1
go: downloading github.com/jirfag/go-printf-func-name v0.0.0-20200119135958-7558a9eaa5af
go: downloading github.com/julz/importas v0.1.0
go: downloading github.com/kisielk/errcheck v1.6.2
go: downloading github.com/kulti/thelper v0.6.3
go: downloading github.com/kunwardeep/paralleltest v1.0.6
go: downloading github.com/kyoh86/exportloopref v0.1.8
go: downloading github.com/ldez/tagliatelle v0.3.1
go: downloading github.com/leonklingele/grouper v1.1.0
go: downloading github.com/lufeee/execinquery v1.2.1
go: downloading github.com/maratori/testpackage v1.1.0
go: downloading github.com/matoous/godox v0.0.0-20210227103229-6504466cf951
go: downloading github.com/mbilski/exhaustivestruct v1.2.0
go: downloading github.com/mgechev/revive v1.2.1
go: downloading github.com/moricho/tparallel v0.2.1
go: downloading github.com/nakabonne/nestif v0.3.1
go: downloading github.com/nishanths/exhaustive v0.8.1
go: downloading github.com/nishanths/predeclared v0.2.2
go: downloading github.com/polyfloyd/go-errorlint v1.0.0
go: downloading github.com/ryancurrah/gomodguard v1.2.4
go: downloading github.com/ryanrolds/sqlclosecheck v0.3.0
go: downloading github.com/sanposhiho/wastedassign/v2 v2.0.6
go: downloading github.com/sashamelentyev/usestdlibvars v1.8.0
go: downloading github.com/securego/gosec/v2 v2.12.0
go: downloading github.com/shazow/go-diff v0.0.0-20160112020656-b6b7b6733b8c
go: downloading github.com/sivchari/containedctx v1.0.2
go: downloading github.com/sivchari/nosnakecase v1.7.0
go: downloading github.com/sivchari/tenv v1.7.0
go: downloading github.com/sonatard/noctx v0.0.1
go: downloading github.com/sourcegraph/go-diff v0.6.1
go: downloading github.com/ssgreg/nlreturn/v2 v2.2.1
go: downloading github.com/stbenjam/no-sprintf-host-port v0.1.1
go: downloading github.com/sylvia7788/contextcheck v1.0.4
go: downloading github.com/tdakkota/asciicheck v0.1.1
go: downloading github.com/tetafro/godot v1.4.11
go: downloading github.com/timakin/bodyclose v0.0.0-20210704033933-f49887972144
go: downloading github.com/tomarrell/wrapcheck/v2 v2.6.2
go: downloading github.com/tommy-muehle/go-mnd/v2 v2.5.0
go: downloading github.com/ultraware/funlen v0.0.3
go: downloading github.com/ultraware/whitespace v0.0.5
go: downloading github.com/uudashr/gocognit v1.0.6
go: downloading github.com/yagipy/maintidx v1.0.0
go: downloading github.com/yeya24/promlinter v0.2.0
go: downloading gitlab.com/bosi/decorder v0.2.3
go: downloading honnef.co/go/tools v0.3.3
go: downloading mvdan.cc/interfacer v0.0.0-20180901003855-c20040233aed
go: downloading mvdan.cc/gofumpt v0.3.1
go: downloading mvdan.cc/unparam v0.0.0-20220706161116-678bad134442
go: downloading github.com/davecgh/go-spew v1.1.1
go: downloading github.com/pmezard/go-difflib v1.0.0
go: downloading github.com/stretchr/objx v0.4.0
go: downloading github.com/subosito/gotenv v1.4.0
go: downloading github.com/hashicorp/hcl v1.0.0
go: downloading github.com/magiconair/properties v1.8.6
go: downloading gopkg.in/ini.v1 v1.66.6
go: downloading github.com/pelletier/go-toml/v2 v2.0.2
go: downloading golang.org/x/text v0.3.7
go: downloading github.com/pelletier/go-toml v1.9.5
go: downloading github.com/quasilyte/gogrep v0.0.0-20220120141003-628d8b3623b5
go: downloading github.com/quasilyte/stdinfo v0.0.0-20220114132959-f7386bf02567
go: downloading github.com/gobwas/glob v0.2.3
go: downloading go.uber.org/zap v1.17.0
go: downloading github.com/kisielk/gotool v1.0.0
go: downloading golang.org/x/sync v0.0.0-20220722155255-886fb9371eb4
go: downloading github.com/gostaticanalysis/comment v1.4.2
go: downloading github.com/ettle/strcase v0.1.1
go: downloading github.com/gostaticanalysis/analysisutil v0.7.1
go: downloading github.com/fatih/structtag v1.2.0
go: downloading github.com/Masterminds/semver v1.5.0
go: downloading github.com/phayes/checkstyle v0.0.0-20170904204023-bfd46e6a821d
go: downloading github.com/nbutton23/zxcvbn-go v0.0.0-20210217022336-fa2cb2858354
go: downloading github.com/prometheus/client_golang v1.12.1
go: downloading golang.org/x/exp/typeparams v0.0.0-20220613132600-b0d781184e0d
go: downloading github.com/google/go-cmp v0.5.8
go: downloading mvdan.cc/lint v0.0.0-20170908181259-adc824a0674b
go: downloading go.uber.org/atomic v1.7.0
go: downloading go.uber.org/multierr v1.6.0
go: downloading github.com/chavacava/garif v0.0.0-20220316182200-5cad0b5181d4
go: downloading github.com/olekukonko/tablewriter v0.0.5
go: downloading github.com/cespare/xxhash/v2 v2.1.2
go: downloading github.com/prometheus/common v0.32.1
go: downloading github.com/prometheus/procfs v0.7.3
go: downloading google.golang.org/protobuf v1.28.0
go: downloading github.com/mattn/go-runewidth v0.0.9
>> linting code
ERRO [runner] Panic: buildir: package "netip" (isInitialPkg: false, needAnalyzeSource: true): in net/netip.AddrFromSlice: cannot convert Load <[]byte> t0 ([]byte) to [4]byte: goroutine 2978 [running]:
runtime/debug.Stack()
        /home/monadmin/MySoftwares/golang/go/src/runtime/debug/stack.go:24 +0x65
github.com/golangci/golangci-lint/pkg/golinters/goanalysis.(*action).analyzeSafe.func1()
        /home/monadmin/go/pkg/mod/github.com/golangci/golangci-lint@v1.48.0/pkg/golinters/goanalysis/runner_action.go:101 +0x155
panic({0x14ced60, 0xc00cb77040})
        /home/monadmin/MySoftwares/golang/go/src/runtime/panic.go:884 +0x213
honnef.co/go/tools/go/ir.emitConv(0xc003082b40, {0x1902808, 0xc003ce4ae0}, {0x18f5cf8?, 0xc00ddb5f68}, {0x18f53e8, 0xc002a7f0c0})
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/emit.go:293 +0xd29
honnef.co/go/tools/go/ir.(*builder).expr0(0xc000d8fa28, 0xc003082b40, {0x18f9090?, 0xc002a7f0c0?}, {0x7, {0x18f5cf8, 0xc00ddb5f68}, {0x0, 0x0}})
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:610 +0x5d7
honnef.co/go/tools/go/ir.(*builder).expr(0x18f5e88?, 0xc003082b40, {0x18f9090, 0xc002a7f0c0})
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:566 +0x1fa
honnef.co/go/tools/go/ir.(*builder).emitCallArgs(0x18f5e88?, 0xc003082b40, 0xc004d8cac0, 0xc002a7f100, {0x0?, 0x0, 0x8a96e7?})
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:975 +0x135
honnef.co/go/tools/go/ir.(*builder).setCall(0x1537d40?, 0xc003082b40, 0xc002a7f100, 0xc0029aaae8)
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:1037 +0x8e
honnef.co/go/tools/go/ir.(*builder).expr0(0xc000d8fa28, 0xc003082b40, {0x18f9090?, 0xc002a7f100?}, {0x7, {0x18f5de8, 0xc00601dd50}, {0x0, 0x0}})
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:623 +0x218e
honnef.co/go/tools/go/ir.(*builder).expr(0xc000d8ee78?, 0xc003082b40, {0x18f9090, 0xc002a7f100})
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:566 +0x1fa
honnef.co/go/tools/go/ir.(*builder).stmt(0xc003082b40?, 0xc003082b40, {0x18f95d0?, 0xc003a75800?})
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:2291 +0x194c
honnef.co/go/tools/go/ir.(*builder).stmtList(...)
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:855
honnef.co/go/tools/go/ir.(*builder).switchStmt(0xc000d8f308?, 0xc003082b40, 0xc003db66c0, 0x0)
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:1366 +0x19a5
honnef.co/go/tools/go/ir.(*builder).stmt(0x20?, 0xc003082b40, {0x18f9720?, 0xc003db66c0?})
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:2365 +0x121c
honnef.co/go/tools/go/ir.(*builder).stmtList(0x8b0065?, 0xc000d8f4f8?, {0xc003a759c0?, 0x2, 0x8b1c70?})
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:855 +0x45
honnef.co/go/tools/go/ir.(*builder).stmt(0xc003082b40?, 0xc003082b40, {0x18f9030?, 0xc003db66f0?})
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:2338 +0x9b9
honnef.co/go/tools/go/ir.(*builder).buildFunction(0xc000d8fa28, 0xc003082b40)
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:2450 +0x3d7
honnef.co/go/tools/go/ir.(*builder).buildFuncDecl(0x0?, 0xc0001a1200, 0xc003db6720)
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:2488 +0x19b
honnef.co/go/tools/go/ir.(*Package).build(0xc0001a1200)
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:2594 +0xc16
sync.(*Once).doSlow(0xc0060095e0?, 0xc00de9c1e0?)
        /home/monadmin/MySoftwares/golang/go/src/sync/once.go:74 +0xc2
sync.(*Once).Do(...)
        /home/monadmin/MySoftwares/golang/go/src/sync/once.go:65
honnef.co/go/tools/go/ir.(*Package).Build(...)
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/go/ir/builder.go:2512
honnef.co/go/tools/internal/passes/buildir.run(0xc002b0ac30)
        /home/monadmin/go/pkg/mod/honnef.co/go/tools@v0.3.3/internal/passes/buildir/buildir.go:86 +0x368
github.com/golangci/golangci-lint/pkg/golinters/goanalysis.(*action).analyze(0xc00322f360)
        /home/monadmin/go/pkg/mod/github.com/golangci/golangci-lint@v1.48.0/pkg/golinters/goanalysis/runner_action.go:187 +0x9d6
github.com/golangci/golangci-lint/pkg/golinters/goanalysis.(*action).analyzeSafe.func2()
        /home/monadmin/go/pkg/mod/github.com/golangci/golangci-lint@v1.48.0/pkg/golinters/goanalysis/runner_action.go:105 +0x1d
github.com/golangci/golangci-lint/pkg/timeutils.(*Stopwatch).TrackStage(0xc0014845a0, {0x1697471, 0x7}, 0xc000213748)
        /home/monadmin/go/pkg/mod/github.com/golangci/golangci-lint@v1.48.0/pkg/timeutils/stopwatch.go:111 +0x4a
github.com/golangci/golangci-lint/pkg/golinters/goanalysis.(*action).analyzeSafe(0xc0005f93e0?)
        /home/monadmin/go/pkg/mod/github.com/golangci/golangci-lint@v1.48.0/pkg/golinters/goanalysis/runner_action.go:104 +0x85
github.com/golangci/golangci-lint/pkg/golinters/goanalysis.(*loadingPackage).analyze.func2(0xc00322f360)
        /home/monadmin/go/pkg/mod/github.com/golangci/golangci-lint@v1.48.0/pkg/golinters/goanalysis/runner_loadingpackage.go:80 +0xb4
created by github.com/golangci/golangci-lint/pkg/golinters/goanalysis.(*loadingPackage).analyze
        /home/monadmin/go/pkg/mod/github.com/golangci/golangci-lint@v1.48.0/pkg/golinters/goanalysis/runner_loadingpackage.go:75 +0x1eb
WARN [runner] Can't run linter goanalysis_metalinter: goanalysis_metalinter: buildir: package "netip" (isInitialPkg: false, needAnalyzeSource: true): in net/netip.AddrFromSlice: cannot convert Load <[]byte> t0 ([]byte) to [4]byte
WARN [linters context] rowserrcheck is disabled because of generics. You can track the evolution of the generics support by following the https://github.com/golangci/golangci-lint/issues/2649.
WARN [linters context] structcheck is disabled because of generics. You can track the evolution of the generics support by following the https://github.com/golangci/golangci-lint/issues/2649.
ERRO Running error: 1 error occurred:
        * can't run linter goanalysis_metalinter: goanalysis_metalinter: buildir: package "netip" (isInitialPkg: false, needAnalyzeSource: true): in net/netip.AddrFromSlice: cannot convert Load <[]byte> t0 ([]byte) to [4]byte

make: *** [golangci] Error 3
[monadmin@den-grafana-01]~/go/pkg/mod/github.com/mjtrangoni/flexlm_exporter@v0.0.8>
```



