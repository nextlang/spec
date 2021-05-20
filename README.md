# spec

Some cool features will be available soon. The main goal of the lannguage is to provide a similar mechaism to **Swift**'s `#available/@available` feature to deploy single binary to multiple platform versions. A VM or JIT or Booter will drop uavailable features fom binary on the fly. 

Expectations:

* No garbage collector at runtime (thanks)
* C codes or libary can be used diectly with no cost
* High perfomance
* Pointers and all features in C must be supported
* API, Platform availability check
* Mutiple platform versions with single binary with `#available` 
* Fast compilation
* ...

```Swift
struct vertex {
  position float3 #attibute(0)
}

add(a float, b float): float {
  ret a + b
}

dosomething() {

  if #available(iOS 14, *) {
    // iOS 14 specific API
  } else if #available(Windows 10, *) {
    // Windows 10 specific API
  } else if #available(Windows 8, *) {
    // Windows 8 specific API
  }

  if #available(DirectX_11, *) {
    // DirectX 11 specific API
  } else if #available(DirectX 12, *) {
    // DirectX 12 specific API
  }
  
  if #available(Metal iOS, *) {
    // Metal iOS specific API
  } else if #available(Metal macOS, *) {
    // Metal macOS specific API
  }
  
  // ...
}

#get("/index")
router() {

}

#[post("/index"), role("admin")]
router() {

}
```
