```shell
# Installation prerequisites for Void Linux:
sudo xbps-install unzip git gdb curl cmake libX11-devel glu-devel libXrandr-devel libXinerama-devel  libXcursor-devel libXi-devel zlib-devel alsa-lib-devel gtk+-devel jack-devel jq

# Compile VCV Rack:
git clone https://github.com/VCVRack/Rack.git
cd Rack
git submodule update - -init - -recursive
make dep
make
make run

# Test a basic compilation:
pushd .
cd /tmp
git clone https://github.com/LOGUNIVPM/VCVBook.git
popd
cp -r /tmp/VCVBook/HelloWorld/ ./plugins
make
cd ../..
make run
```
