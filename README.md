# SlimeVR Feeder Application

This is a modified version of the [SlimeVR Feeder App](https://github.com/SlimeVR/SlimeVR-Feeder-App) that is for **debugging only**. I used the feeder app as a base only because its already pulling the OpenVR props, and its an easy modification to make it spit more info out.

## How to use

1. Follow the [building from source](#building-from-source) instructions below.
2. Launch SteamVR and connect your HMD and controllers as you normally do.
3. Launch the app in a terminal with the `--hmd` flag:
   - `./build/_CPack_Packages/win64/ZIP/SlimeVR-Feeder-App-win64/SlimeVR-Feeder-App.exe --hmd`
4. If the SteamVR dashboard is open, close it.
5. The terminal output should show all OpenVR devices detected and all their relevant OpenVR props.

It might not work if you don't have the SlimeVR server, in which case, download and install it normally. When launching SteamVR, close its copy of the feeder app, and launch this one.

## Building from source

We assume that you already have [Git](https://git-scm.com/download/win) and [CMake](https://cmake.org/) installed. Run:

```
git clone --recursive https://github.com/SlimeVR/SlimeVR-Feeder-App.git
cd SlimeVR-Feeder-App
cmake -B build
cmake --build build --target package --config Release
```

You can then execute the newly built binary:

```
./build/_CPack_Packages/win64/ZIP/SlimeVR-Feeder-App-win64/SlimeVR-Feeder-App.exe --hmd
```

## Thanks
This is a fork of the [SlimeVR Feeder App](https://github.com/SlimeVR/SlimeVR-Feeder-App) because it was quicker than writing my own OpenVR app.

Thanks from the original README as follows:

This was largely based off of https://github.com/Omnifinity/OpenVR-Tracking-Example , even if the structure is different. Thanks, @Omnifinity.

Rust setup was basically copy-pasted from https://github.com/XiangpengHao/cxx-cmake-example.
Thanks, @XiangpengHao.
