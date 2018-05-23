## CoreOS ARM64 Repositories

CoreOS is now releasing official ARM64 builds.  If unsure, you should start with the latest ARM64 beta binary release from here: https://coreos.com/releases/

If you want to make some modifications to CoreOS and build an OS image yourself, then you should probably just build from the upstream CoreOS source repositories.  Follow the CoreOS SDK instructions here: https://coreos.com/docs/sdk-distributors/sdk/modifying-coreos.

To build for ARM64 pass ```--board=arm64-usr``` to the CoreOS SDK utilities:

    ~/trunk/src/scripts/build_packages --board=arm64-usr --nousepkg
    ~/trunk/src/scripts/build_image --board=arm64-usr prod

If you are sure you want to use my development repositories, follow the above CoreOS SDK instructions, but use my manifest when initializing your local repositories:

    cork create --manifest-url=https://github.com/glevand/coreos--manifest.git
    cork enter
