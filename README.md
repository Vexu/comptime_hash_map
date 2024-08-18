# Comptime HashMap

A statically initiated HashMap, originally a pull request to the Zig std lib [#5359](https://github.com/ziglang/zig/pull/5359).

## Installation

Build for Zig `0.13.0`.

```sh
zig fetch --save git+https://github.com/Vexu/comptime_hash_map
```

In your `build.zig`:
```zig
const chm = b.dependency("comptime_hash_map", .{});
exe.root_module.addImport("comptime_hash_map", chm.module("comptime_hash_map"));
```

In your `exe` module:
```zig
const chm = @import("comptime_hash_map");
```
