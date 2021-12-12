# grpc-go-1

We modified gRPC-go-0bc741730b8171fc51cdaf826caea5119c411009 by doing the two changes:

1. We replace all 'func (s) Test' with 'func Test' by executing the following command. 

```
$ grep -rl 'func (s) Test' ./ | xargs sed -i 's/func (s)/func/g'
```

2. We comment out the body of ```func check(efer Errorfer, timeout time.Duration)``` in file internal/leakcheck/leakcheck.go.



