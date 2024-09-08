# build_mmcv
MMCV Build Manual (1.4.3, 1.7.0)

```
sudo apt install gcc-12
sudo apt install g++-12
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-12 12
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-12 12
gcc --version
g++ --version

```

```
cd mmcv
sed -i 's/c++14/c++17/g' setup.py
export MMCV_WITH_OPS=1
python setup.py build_ext
python setup.py develop

# comment out #include <THC/THC.h>
```
