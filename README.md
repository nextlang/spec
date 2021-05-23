# Spec of Next Programming Language (In Progrress)

Some cool features will be available soon. The main goal of the lannguage is to provide a similar mechaism to **Swift**'s `#available/@available` feature to deploy single binary to multiple platform versions. A VM or JIT or Booter will drop uavailable features fom binary on the fly. 

Expectations:

* Optimize workflow with Universal Shading Language (https://github.com/UniversalShading)
* Built-in float3, float4, mat3, mat4...
* Built-in vector, matrix math
* Built-in AI / Machine Learning helpers
* Built-in CURL suppot (maybe)
* No garbage collector at runtime (thanks)
* C codes or libary can be used diectly with no cost
* High perfomance
* Pointers and all features in C must be supported
* API, Platform availability check
* Mutiple platform versions with single binary with `#available` 
* Fast compilation
* Small binary size
* Operator and function overloading, custom operators
* Simple
* Package manager (or use https://github.com/unipkg)
* Cross platform NextUI (https://github.com/nextlang/NextUI) or UniversalUI (https://github.com/UniversalUI) alternative to SwiftUI and Flutter
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
@get("/index") // ?
router() {

}

#[post("/index"), role("admin")]
router() {

}
```
