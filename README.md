# Eclipse-testnet-interaction

# REMEMBER, THIS IS ONLY FOR EDUCATIONAL PURPOSES! NOTHING IS PROMISED!  


__________________
## Amount Raised 
Eclipse raised a total of $65M HackVC, Polychain Capital among other Investors 
<img width="898" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/c4336c7a-ba61-4403-a87f-754a9fa2dddb">

----------------


## Gettings Started 
### Installing Perequisite 
```
sudo apt update
sudo apt upgrade -y
```


### Install Rust 

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
Reply with ```1```
<img width="551" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/774b93db-a96a-4a63-9de7-658340b86c8a">


### Environment Variable  

```
. "$HOME/.cargo/env"
```
<img width="737" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/10418c58-dd67-42e3-85ed-fa7504c5e102">


### check ```RUST version```

```
rustc --version
```


## Install Solana CLI 

```
sh -c "$(curl -sSfL https://release.solana.com/stable/install)"
```
<img width="819" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/d0e5f173-2789-4992-95ba-857ad8fd14bd">


```
export PATH="/root/.local/share/solana/install/active_release/bin:$PATH"
```
<img width="584" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/7ab8ff70-b57f-4c52-bb93-4afc6e9a74ca">


### check version if installed properly 
```
solana --version
```
<img width="469" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/a63c08db-d6b7-4764-8cb1-5d0feb785d3c">




### Install dependencies 
Reply with ```y``` and proceed 
```
sudo apt-get update
sudo apt-get install nodejs
sudo apt-get install npm
npm install --global yarn

```


### Checking version 
```
node -v
npm --version
yarn --version
```
<img width="803" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/18b47089-dbb8-436c-bcdc-793c2feafc21">



# Install Anchor 

```
cargo install --git https://github.com/project-serum/anchor anchor-cli --locked
```
<img width="811" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/8d8b3814-9928-4470-a89a-5294d1c466b1">


-------------------

### Check version 
```
anchor --version
```
------------


## Create a Solana Wallet 
```
solana-keygen new -o /path-to-wallet/my-wallet.json
```
<img width="505" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/2caf0af0-0f9c-4e9b-bb51-c1ab83470649">


Press ```ENTER``` ans save the Info 
<img width="497" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/6630442d-d1e9-4eb0-add5-cf4621e9b2cd">




## Update configuration to use new wallet
```
solana config set --url https://testnet.dev2.eclipsenetwork.xyz/
```
<img width="553" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/a3d46a1c-a6ed-4e62-bd1e-ee92218ffb2f">

```
solana config set --keypair /path-to-wallet/my-wallet.json

```

### Save Solana address 
```
solana address
```


-----------------------

# Import the same seedphrase to Metamask/Rabby Wallet --- for we are gonna send Ethereum Sepolia to it 
## I renamed it so i won't mix it up with my wallet 

<img width="709" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/18361a71-7e46-426c-8688-f01b2255577f">

### Request Sepolia gas on your main wallet: 
MINE SEPOLIA GAS  ---https://sepolia-faucet.pk910.de/
Request from Quicknode ---  https://faucet.quicknode.com/ethereum/sepolia 
<img width="911" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/d381cc00-a47b-4b09-952e-f99159cdee4f">
<img width="901" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/29e02b7c-717c-4a26-b9b7-3b04e933075d">




---------------------
### Send Sepolia ETH to the wallet imported 
<img width="288" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/e582ddd1-0ba6-4c8d-a228-87e2aadedc57">

---------------



# Clone Eclipse Bridge Script 

```
git clone https://github.com/Eclipse-Laboratories-Inc/testnet-deposit
```
<img width="574" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/627db375-b9a7-48b7-8016-23cbae7ffebe">


### Navigate to ```testnet-deposit```
```
cd testnet-deposit
```

```
npm install
```
<img width="637" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/6ec421e8-0879-4c4b-91c1-4c080285a250">



# AMENDEMENT BEFORE WE PROCEED 
Update Node version 
```
sudo apt-get remove nodejs
```
press `y``` and proceed 


```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
source ~/.bashrc
```

```
nvm install --lts
nvm use --lts
```

```
node -v
```
<img width="808" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/68248116-af93-45a7-a4df-2c63851ca106">



## Run Bridge script 

```
node deposit.js [Solana Address] 0x7C9e161ebe55000a3220F972058Fb83273653a6e [Amount in Gwei] [Fee in Gwei] [Ethereum Private Key] [Sepolia RPC Endpoint]
```

### Repalce solana address with the one you coped alonside the seedphrase
### Amount in GWEI ```3000000```
### Fee in GWEI ```100000``` 
### Private key [view the private key of that seedphrase imported in Rabby wallet and paste 
### Sepolia RPC ```Endpoint```  -- https://rpc.sepolia.org/ 


------------------
### E.g  End product will look like this 
```
node deposit.js 7m3wLFNgA2wzG7MvY8ij3SpE8sU51Fc15rXA5UwCXHkR 0x7C9e161ebe55000a3220F972058Fb83273653a6e 3000000 3000000 0xeeeeeeeeeeeeeeeeeeprivatekey https://rpc.sepolia.org/
```
<img width="466" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/21722a9b-caf6-4e0b-9f4d-fd5bb95bcc6c">

### REPEAT PROCESS 3 - 4 TIMES 


## Ckeck balance 
```
solana balance
```
<img width="298" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/239d5586-4ca3-48ed-b62f-2d338a84cf2d">


------------------
# Creating a Token 
```
spl-token create-token --enable-metadata -p TokenzQdBNbLqP5VEhdkAS6EPFLC1PHnBqCXEpPxuEb
```
<img width="812" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/142dbc86-01db-4c1b-926a-9f258a0866e0">



## Mint Token 
```
spl-token create-account <YOUR_TOKEN_ADDRESS>
```

### Replace with your token address previously deplyed from above step 
<img width="633" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/63757d78-9dfb-4d06-9dac-58889244c92c">


### Mint token
```
spl-token mint <YOUR_TOKEN_ADDRESS> 10000
```
<img width="610" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/32d3286c-3ab8-4e09-8bf0-2463e533bbfe">


### Check token balance 
```
spl-token accounts
```
<img width="414" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/520387e5-ae7b-4289-9e37-4b48f28d3663">



# DONE! !!

# THAT'S ALL FOR NOW, REMEMBER, THIS IS ONLY FOR EDUCATIONAL PURPOSES! NOTHING IS PROMISED! 






Fill form: 
https://docs.google.com/forms/d/e/1FAIpQLSfJQCFBKHpiy2HVw9lTjCj7k0BqNKnP6G1cd0YdKhaPLWD-AA/viewform?pli=1

<img width="344" alt="image" src="https://github.com/raghav353/Eclipse-testnet-interaction/assets/151916837/3ac3e33e-0aa9-4013-a83c-46017f247883">











---------------



