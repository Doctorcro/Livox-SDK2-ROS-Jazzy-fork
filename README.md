# Livox-SDK2

## Role
Low-level hardware communication SDK for Livox LiDAR devices.

## Dependencies
- None (standalone C++ library)

## How It Works
- Provides compile-time headers and runtime shared library (`liblivox_lidar_sdk_shared.so`)
- After `cmake --build` and `sudo cmake --install`, the `.so` is installed to `/usr/local/lib/`
- The source directory is retained for reference and SDK upgrades — do not delete

## Runtime Dependency
`ws_livox` (livox_ros_driver2) links against the installed `.so` at build time.
`sudo ldconfig` must be run after install on any new device.

## Cross-Device Note
Must be compiled and installed on every target device before building `ws_livox`.
