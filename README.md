# armorcore

3D engine core for C with embedded V8. ArmorCore is designed for the [Graphics5](https://github.com/Kode/Kinc/tree/master/Backends/Graphics5) api and targets Direct3D12, Vulkan, Metal and WebGPU. *(wip!)*

Based on [Krom](https://github.com/Kode/Krom). Powered by [Kinc](https://github.com/Kode/Kinc). Powering [ArmorPaint](https://github.com/armory3d/armorpaint).

```bash
git clone --recursive https://github.com/armory3d/armorcore
cd armorcore
```

**Windows**
```bash
# Unpack `v8\libraries\win32\release\v8_monolith.7z` using 7-Zip - Extract Here (exceeds 100MB)
node Kinc/make.js -g direct3d11
# Open generated Visual Studio project at `build\Krom.sln`
# Build for x64 & release
```

**Linux**
```bash
node Kinc/make.js -g opengl --compiler clang --compile
cd Deployment
strip Krom
```

**macOS**
```bash
node Kinc/make.js -g metal
# Open generated Xcode project at `build/Krom.xcodeproj`
# Build
```

**Android** *wip*
```bash
node Kinc/make.js android -g opengl
# Manual tweaking is required for now:
# https://github.com/armory3d/armorcore/blob/master/kincfile.js#L68
# Open generated Android Studio project at `build/Krom`
# Build for device
```

**iOS** *wip*
```bash
node Kinc/make.js ios -g metal
# Open generated Xcode project at `build/Krom.xcodeproj`
# Build for device
```

**Windows DXR** *wip*
```bash
# Unpack `v8\libraries\win32\release\v8_monolith.7z` using 7-Zip - Extract Here (exceeds 100MB)
node Kinc/make.js -g direct3d12
# Open generated Visual Studio project at `build\Krom.sln`
# Build for x64 & release
```

**Linux VKRT** *wip*
```bash
node Kinc/make.js -g vulkan --compiler clang --compile
cd Deployment
strip Krom
```

**Windows VR** *wip*
```bash
# Unpack `v8\libraries\win32\release\v8_monolith.7z` using 7-Zip - Extract Here (exceeds 100MB)
node Kinc/make.js -g direct3d11 --vr oculus
# Open generated Visual Studio project at `build\Krom.sln`
# Build for x64 & release
```

**Generating a v8 snapshot file**
```bash
./Krom . --snapshot
# Generates a `krom.bin` file from `krom.js` file
```
