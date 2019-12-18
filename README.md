This is a template for developing [Bricscad](https://www.bricsys.com/en-intl/) extension
with [ObjectBRX SDK](https://www.bricsys.com/en-intl/developer/) with VSCode and Meson build system on Linux.

## How to use

1. Copy ObjectBRX SDK to `/opt/bricsys/sdk`.
2. Make a link `/opt/bricsys/sdk/BRX19_SDK` pointing to current SDK version.
3. Copy `brx19-sdk.pc` to a directory where `pkg-config` can find it.
4. Add to `.bashrc`
    ```
    export BRX19_SDK_PATH=/opt/bricsys/sdk/BRX19_SDK
    ```
5. `.vscode` directory contains sample IntelliSence configuration `c_cpp_properties.json` for coding with *ObjectBRX*.
6. `meson.build` is a sample *Meson* project to build extension for *Bricscad*.
   I did not test the Meson build file with `brxSample` from the *SDK*. My project was simpler, but you can take the build file as a start.

You can use the template on your own if it help you.
