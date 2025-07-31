# onsyuri-libretro-trimui-smart-pro

onsyuri-libretro build for **Trimui Smart Pro**

# usage

1. download .info and .so from release page
2. copy .info and .so to SDCARD/RetroArch/.retroarch/cores
3. copy ONS folder of repository to SDCARD/Enums (you can edit the config.json as you wish)
4. put your ONS games to SDCARD/Roms
5. Refresh ROMS on device and launch game by .nt2/.nt3/.dat/.txt/...

### how to building it yourself

1. get toolchain from offcial sdk，extract it e.g. /opt/aarch64-linux-gnu-7.5.0-linaro

2. git clone  --recurse-submodules https://github.com/YuriSizuku/OnscripterYuri.git

3. cd src/onsyuri_libretro && mkdir build &&cd build

4. create toolchain.cmake

   ```cmake
   set(CMAKE_C_COMPILER /opt/aarch64-linux-gnu-7.5.0-linaro/bin/aarch64-linux-gnu-gcc)
   set(CMAKE_CXX_COMPILER/opt/aarch64-linux-gnu-7.5.0-linaro/bin/aarch64-linux-gnu-g++)
   ```

5. cmake -DCMAKE_TOOLCHAIN_FILE=./toolchain.cmake ..
6. make

Then you will get onsyuri-libretro.so with .info already exists src/onsyuri_libretro/onsyuri-libretro.info

## based on

- [trimui/toolchain_sdk_smartpro: SDK and toolchain for TRIMUI Smart Pro TG5040](https://github.com/trimui/toolchain_sdk_smartpro)
- [YuriSizuku/OnscripterYuri: An enhancement ONScripter project porting to many platforms, especially web.](https://github.com/YuriSizuku/OnscripterYuri)
- [iyzsong/onscripter-libretro: Libretro core for ONScripter](https://github.com/iyzsong/onscripter-libretro)

Thanks for this issus：[Compiling the libretro core · Issue #32 · YuriSizuku/OnscripterYuri](https://github.com/YuriSizuku/OnscripterYuri/issues/32)
