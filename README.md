# catch-exception-without-abi-cxx11
We expect this demo can build pass, run pass, and catch `sycl::exception` when using -D_GLIBCXX_USE_CXX11_ABI=0
The one of expected result may be:
```bash
gpu number: 2
tile partition is UNSUPPORTED!
tile partition is UNSUPPORTED!
pass!
```
`tile partition is UNSUPPORTED!` is our expectation. But `tile partition is supported!` means the demo doesn't go `catch` path, resulting in `sycl::exception` wasn't tested.
