# KUDO COCKROACHDB #

## RELEASE V1.00 ##



## CREATE YOUR FIRST OPERATOR #

Install kubectl-kudo cli.  

```
$ brew tap kudobuilder/tap
$ brew install kudo-cli
```

Install Kudo Operator on Kubernetes

```
$ kubectl kudo init
```

Build your Kudo CockRoachDB Operator

```
$ cd ~/SymbioTekGit/operators
$ chmod u+x ./build-operator.sh
$ ./build-operator.sh cockroachdb
Using KUDO Version: version.Info{GitVersion:"0.17.1", GitCommit:"f7fa1438", BuildDate:"2020-10-19T14:05:17Z", GoVersion:"go1.15.3", Compiler:"gc", Platform:"darwin/amd64", KubernetesClientVersion:"v0.19.2"}
Warnings
package is valid
Package created: /Users/aheib/SymbioTekGit/operators/build/repo/cockroachdb-20.1.8_0.1.0.tgz
```

Install your Druid Operator

```
$ kubectl kudo install build/repo/cockroachdb-20.1.8_0.1.0.tgz
operator default/cockroachdb created
operatorversion default/cockroachdb-20.1.8-0.1.0 created
instance default/cockroachdb-instance created
```

## RELEASES ##

* 0.1.0: First working KUDO CockRoachDB Operator, single container, no param, no services

