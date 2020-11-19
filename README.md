## 测试结果
* httprouter 1.3
* brouter 0.0.1
```
GithubAPI Routes: 180
GithubAPI2 Routes: 203
   BeegoMuxRouter: 97440 Bytes
   BoneRouter: 88288 Bytes
   ChiRouter: 64584 Bytes
   HttpRouter: 33440 Bytes
   BRouter: 51096 Bytes
   trie-mux: 121320 Bytes
   MuxRouter: 1373064 Bytes
   GoRouter1: 76320 Bytes
   GoRouter2: 84832 Bytes
#Static Routes: 157
   HttpRouter: 21680 Bytes
   BRouter: 35200 Bytes

goos: linux
goarch: amd64
pkg: test
BenchmarkBeegoMuxRouterWithGithubAPI-4   	    9409	    113888 ns/op	  116352 B/op	     900 allocs/op
BenchmarkBoneRouterWithGithubAPI-4       	     775	   1562220 ns/op	  562881 B/op	    6807 allocs/op
BenchmarkTrieMuxRouterWithGithubAPI-4    	   19135	     63543 ns/op	   57024 B/op	     468 allocs/op
BenchmarkBaseRouterWithGithubAPI-4       	   69416	     17271 ns/op	       0 B/op	       0 allocs/op
BenchmarkHttpRouterWithGithubAPI-4       	   45282	     26845 ns/op	   11744 B/op	     144 allocs/op
BenchmarkGoRouter1WithGithubAPI-4        	   24510	     48947 ns/op	   11920 B/op	     360 allocs/op
BenchmarkGoRouter2WithGithubAPI2-4       	   21008	     57357 ns/op	   13832 B/op	     406 allocs/op
BenchmarkChiRouterWithGithubAPI2-4       	    9284	    126014 ns/op	  105097 B/op	    1110 allocs/op
BenchmarkMuxRouterWithGithubAPI2-4       	     352	   3397559 ns/op	   59511 B/op	     992 allocs/op
BenchmarkHttpRouter_StaticAll-4          	  120474	     10068 ns/op	       0 B/op	       0 allocs/op
BenchmarkBRouter_StaticAll-4             	  111889	     10822 ns/op	       0 B/op	       0 allocs/op
PASS
ok  	test	17.046s

```
