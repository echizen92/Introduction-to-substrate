# Introduction-to-substrate
Trying out substrate 

On MacOs run this script to set up your computer 

```
curl https://getsubstrate.io -sSf | bash -s -- --fast
```

This script installs the following:

-CMake
-pkg-config
-OpenSSL
-Git
-Rust

If you did not have Rust installed prior to running this script, make sure to add restart your terminal before continuing (command given in last line of the script output).

#Compiling Substrate

```
 git clone -b v2.0.0-rc5 --depth 1 https://github.com/substrate-developer-hub/substrate-node-template
```

#Initialize your WebAssembly build environment
 
Load settings into the current shell script if you can't use rustup command
If you've run this before, you don't need to run it again. But doing so is harmless.
```
source ~/.cargo/env
```
Update Rust

```
rustup update nightly
rustup update stable
```
Add Wasm target
```
rustup target add wasm32-unknown-unknown --toolchain nightly
```

#Create a branch for your work and Compile your Substrate node

```
cd substrate-node-template/
git checkout -b my-first-substrate-chain
cargo build --release
```

#Front-End

In order to interact with your node, you will be running a local instance of the Substrate Developer Hub Front-End Template (https://github.com/substrate-developer-hub/substrate-front-end-template ) which requires you to have Node.js (https://nodejs.org/) installed on your computer. You may want to use the time that your node is compiling to ensure that your development environment is prepared with these dependencies.
