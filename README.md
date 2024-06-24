# Eclipse-testnet-interaction

# REMEMBER, THIS IS ONLY FOR EDUCATIONAL PURPOSES! NOTHING IS PROMISED!  


__________________
## Amount Raised 
Eclipse raised a total of $65M HackVC, Polychain Capital among other Investors 
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/2d2c5a3e-ae73-4991-ba2b-eb4eeb9de915)

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
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/5ebb84f3-8c57-4fdd-af89-b72d58373470)


Press ```ENTER``` ans save the Info 
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/dc67db2f-e5aa-44d6-b033-882a96573d0c)




## Update configuration to use new wallet
```
solana config set --url https://testnet.dev2.eclipsenetwork.xyz/
```
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/5e778d24-6df2-4ce9-a152-6e4d2fa8bc27)

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

![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/e6a55210-d6a4-45de-a708-d599238bd841)

### Request Sepolia gas on your main wallet: 
MINE SEPOLIA GAS  ---https://sepolia-faucet.pk910.de/
Request from Quicknode ---  https://faucet.quicknode.com/ethereum/sepolia 
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/3ec18a31-9b77-4fc7-876e-bd383d10ad1b)
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/7196a7bd-0b77-43db-8640-9d1434c6ba52)




---------------------
### Send Sepolia ETH to the wallet imported 
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/9658de88-4fa4-47a5-b667-21ea2db684f6)

---------------



# Clone Eclipse Bridge Script 

```
git clone https://github.com/Eclipse-Laboratories-Inc/testnet-deposit
```
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/9361e940-f603-400c-8cfa-87f244566a9c)


### Navigate to ```testnet-deposit```
```
cd testnet-deposit
```

```
npm install
```
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/dd7d8ece-6657-4ee4-b5a6-c78e828b967f)



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
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/1b077a5c-a23d-4b85-9ea0-397ead36f43f)



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
node deposit.js Cz2CCCtzqUAB97NAkVM6FzdF6d3EPx7pa4pN1JaWwrxz 0x7C9e161ebe55000a3220F972058Fb83273653a6e 3000000 3000000 0xeeeeeeeeeeeeeeeeeeprivatekey https://rpc.sepolia.org/
```
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/e1b43551-6eaf-4a2a-81fb-9312c775d47e)

### REPEAT PROCESS 3 - 4 TIMES 


## Ckeck balance 
```
solana balance
```
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/626224c9-d871-4fc9-bb3d-f7560fbb7f56)


------------------
# Creating a Token 
```
spl-token create-token --enable-metadata -p TokenzQdBNbLqP5VEhdkAS6EPFLC1PHnBqCXEpPxuEb
```
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/c677fb79-afdf-479c-9940-513760fd14c6)



## Mint Token 
```
spl-token create-account <YOUR_TOKEN_ADDRESS>
```

### Replace with your token address previously deplyed from above step 
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/14b85f96-e975-41ee-aebb-de86ff38203d)


### Mint token
```
spl-token mint <YOUR_TOKEN_ADDRESS> 10000
```
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/05eba99a-cf61-42cf-a69d-ea3d8a04b8c2)


### Check token balance 
```
spl-token accounts
```
![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/e5308f99-62ad-457a-89ea-a8fed07110ef)



# DONE! !!

# THAT'S ALL FOR NOW, REMEMBER, THIS IS ONLY FOR EDUCATIONAL PURPOSES! NOTHING IS PROMISED! 






Fill form: 
https://docs.google.com/forms/d/e/1FAIpQLSfJQCFBKHpiy2HVw9lTjCj7k0BqNKnP6G1cd0YdKhaPLWD-AA/viewform?pli=1

![image](https://github.com/mztacat/Eclipse-Testnet-Interaction/assets/31314340/ee9dbd6e-1517-4aa8-a2b1-9ebac3f743ac)











---------------



