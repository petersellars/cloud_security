# Cloud Security

## Install Score

### score-commpose

```
go install -v github.com/score-spec/score-compose/cmd/score-compose@0.24.2
```

### score-k8s

Not able to install using the go `install` command
```
go install -v github.com/score-spec/score-k8s/cmd/score-k8s@0.2.1
go: github.com/score-spec/score-k8s/cmd/score-k8s@0.2.1 (in github.com/score-spec/score-k8s@v0.0.0-20250121170719-da3d9b4322f7):
        The go.mod file for the module providing named packages contains one or
        more replace directives. It must not contain directives that would cause
        it to be interpreted differently than if it were the main module.
```

Workaround
```
git clone git@github.com:score-spec/score-k8s.git
cd score-k8s/cmd/score-k8s
go install .
```

Will install score-k8s and you can then remove the source code.
