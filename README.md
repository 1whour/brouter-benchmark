## 运行命令
```
go test -test.bench=".*" ./...
```

## 测试结果
* httprouter 1.3
* brouter 0.0.1
```
GithubAPI Routes: 180
GithubAPI2 Routes: 203
   BeegoMuxRouter: 97024 Bytes
   BoneRouter: 86368 Bytes
   ChiRouter: 64584 Bytes
   HttpRouter: 35360 Bytes
   BRouter: 51096 Bytes
   trie-mux: 121736 Bytes
   MuxRouter: 1373064 Bytes
   GoRouter1: 76528 Bytes
   GoRouter2: 84624 Bytes
#Static Routes: 157
   HttpRouter: 21680 Bytes
   BRouter: 35208 Bytes

goos: linux
goarch: amd64
pkg: test
BenchmarkBeegoMuxRouterWithGithubAPI-4   	   10000	    111713 ns/op	  116352 B/op	     900 allocs/op
BenchmarkBoneRouterWithGithubAPI-4       	     721	   1546779 ns/op	  562878 B/op	    6807 allocs/op
BenchmarkTrieMuxRouterWithGithubAPI-4    	   19060	     64217 ns/op	   57024 B/op	     468 allocs/op
BenchmarkBRouterWithGithubAPI-4          	   70467	     16971 ns/op	       0 B/op	       0 allocs/op
BenchmarkHttpRouterWithGithubAPI-4       	   45830	     26609 ns/op	   11744 B/op	     144 allocs/op
BenchmarkGoRouter1WithGithubAPI-4        	   24042	     49632 ns/op	   11920 B/op	     360 allocs/op
BenchmarkGoRouter2WithGithubAPI2-4       	   21088	     57408 ns/op	   13832 B/op	     406 allocs/op
BenchmarkChiRouterWithGithubAPI2-4       	    8469	    128427 ns/op	  106000 B/op	    1110 allocs/op
BenchmarkMuxRouterWithGithubAPI2-4       	     358	   3414899 ns/op	   59373 B/op	     992 allocs/op
BenchmarkHttpRouter_StaticAll-4          	  120054	      9994 ns/op	       0 B/op	       0 allocs/op
BenchmarkBRouter_StaticAll-4             	  111614	     10838 ns/op	       0 B/op	       0 allocs/op
PASS
ok  	test	15.950s
```
