# Ore CLI with Nvidia GPU Support

A command line interface for the Ore program to utilize Nvidia GPU's. 


Built by [@BenjaSOL](https://x.com/benjasol_) & [@KaedonsCrypto](https://x.com/KaedonsCrypto)

## Building

To build the Ore CLI, you will need to have the Rust programming language installed. You can install Rust by following the instructions on the [Rust website](https://www.rust-lang.org/tools/install).

You must have CUDA installed 

```sh
export CUDA_VISIBLE_DEVICES=<GPU_INDEX>
```

Windows users

```sh
nvcc windows.cu -o windows
```

Linux users

```sh
nvcc linux.cu -o linux
```

Take the path to the executsble that was just created and replace the PATH_TO_EXE with the path to the .exe in the mine.rs.

Once you have Rust installed, you can build the Ore CLI by running the following command:

```sh
cargo build --release
```


```sh
./target/release/ore.exe --rpc "" --priority-fee 1 --keypair 'path to keypair' --priority-fee 1 mine --threads 4
```

FOR mine-v2

- `-s 100` - is used to control send_interval to rpc.
- `-b 5` - is used to set the batch size. Max 5. 
- `-w C:\Folder\To\Wallets` - is a folder containing all the wallets (.json) that you want to mine with.
```sh
./target/release/ore.exe --rpc "" mine-v2  -w D:\Dev\MinerWallets -s 100 --threads 4 -b 5
```


You will now run your hashing on the GPU instead of the CPU!

Donations in ORE or SOL: EVK3M6Cth3uPZcATCtnZ16mqArSNXt5oC6kcmakwXudb

## Credits

[ORE Miner](https://github.com/tonyke-bot/ore-miner)

[ORE CLI](https://github.com/HardhatChad/ore-cli)