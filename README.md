# Swap

Copyright (c) 2014-2024 The Monero Project.   
Swap (previously known as Freehaven) is based on [Monero](README_original.md)

![Build-Linux]()

## Production & Development

Active Branches:
- Stable: master(latest/release)
- Unstable: swap-v3.3dev(latest)
- Testing: N/A

To contribute to the Nord Project, please make all pull requests to the _swap-v3.2dev_ branch.<br/>
For production, please use the _latest or tagged release_ of the _master_ branch.

## Resources
- Webpage: []()
- Explorer: []()
- Pool List: []()
- GitHub: []()

## Social/Contact

- Bitcointalk []()
- Discord: []()
- Reddit: [] ()
- Twitter: []()
- Email: 

## Specifications & Emission

- Coin ticker: XWP
- Total supply: 184,000,000 coins before tail emission
- Tail emission: ~1,580,000 coins each year (starting at year 8)
- Decimal places: 12
- PoW hash algorithm: Cuckaroo29s
- Block time: 15 seconds
- Difficulty Adjustment Algorithm: Monero DAA
- Genesis block: 2018-11-16 (November 16, 2018) at 09:06:03 (UTC)
- Premine: No
- Developer fee: No
- Founders reward: No
- Mainnet default P2P port: 19949
- Mainnet default RPC port: 19950

## Donation Address
fh2jc6PbQYd4a5PY3ooPMZiPVniMy4MGcjSRBnoBVc1xLmdCHJ6hc98Ess2hpN2mDgPnCAXtDUUbmjWYutRvdoSr2Nps2o5wc

## Build on linux

install deps:

`sudo apt-get install build-essential cmake pkg-config libboost-all-dev libssl-dev libzmq3-dev libunbound-dev libsodium-dev libreadline6-dev libpgm-dev libnorm-dev`

clone repo:

`git clone --recursive https://github.com/swap-dev/swap`

build daemon and wallet:

`cd swap && mkdir build && cd build && cmake .. && make daemon simplewallet`

or build everything:

`cd swap && mkdir build && cd build && cmake .. && make`

## Build on Windows (using MinGW)

install deps:

`pacman -S mingw-w64-x86_64-toolchain make mingw-w64-x86_64-cmake mingw-w64-x86_64-boost mingw-w64-x86_64-openssl mingw-w64-x86_64-zeromq mingw-w64-x86_64-libsodium mingw-w64-x86_64-hidapi`

clone repo:

`git clone --recursive https://github.com/swap-dev/swap`

build daemon and wallet:

`cd swap && mkdir build && cd build`

`cmake .. -G "MinGW Makefiles" -D STATIC=ON -D ARCH="x86-64" -D BUILD_64=ON -D CMAKE_BUILD_TYPE=Release -D BUILD_TAG="win-x64"`

`mingw32-make`