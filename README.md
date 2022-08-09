# Mastering Solidity

Author : Gun Gun Febrianza



- [The Ethereum Course](https://github.com/Cryptolibertarian-id/The-Ethereum-Course)
- [The Polygon Course](https://github.com/Cryptolibertarian-id/The-Polygon-Course)
- [The Solana Course](https://github.com/Cryptolibertarian-id/The-Solana-Course)
  - [Mastering Solana](https://github.com/Cryptolibertarian-id/Mastering-Solana)
- [The Bitcoin Course](https://github.com/Cryptolibertarian-id/The-Bitcoin-Course)





# Table of Contents



- [x] Solidity
  - [ ] High-level Language
  - [ ] Object Oriented Language
  - [ ] Statically-Typed Language
  - [ ] Case Sensitive Language
  - [ ] Turing Complete Language
- [ ] Development Tools
  - [ ] Node Provider
  - [ ] Hardhat
  - [ ] Etherscan

- [ ] Gas Optimization
- [ ] ERC-20
- [ ] ERC-721 (NFT)
- [ ] IPFS
- [ ] ERC-1155 (SFT)
- [ ] Upgrade Smart Contract
- [ ] Audit Smart Contract
- [ ] Layer 2
- [ ] Advance
  - [ ] EVM Codes
  - [ ] Flash Loans

- [ ] Examples



----



# Header

Last touched on 28 July 2022

| Parameter | Value | Note |
| --------- | ----- | ---- |
|           |       |      |
|           |       |      |
|           |       |      |



---



## Resources 

- Ebooks
  - [Go Ethereum Book](https://goethereumbook.org/en/) By Miguel Mota 
- Repositories
  - [Ethereum Development Tools](https://github.com/miguelmota/ethereum-devtools) By Miguel Mota ([Typescript](https://lab.miguelmota.com/ethereum-devtools/))
  - [Ethereum HD Wallet](https://github.com/miguelmota/ethereum-hdwallet) By Miguel Mota 
  - [EthereumJS Monorepo](https://github.com/ethereumjs/ethereumjs-monorepo)
    - 



---



# Solidity

**Solidity** is a programming language developed by **Gavin Wood**, **Christian Reitwiessner**, **Alex Beregszaszi** and other **Ethereum Contributors**. **Solidity** programming language is influenced by **C++**, **Javascript** and **Python** programming languages.







# Metamask



To detect metamask on user browser use this syntax :

```javascript
if (window.ethereum) {
  //form.classList.add("has-eth"); //display web3 apps, widget, etc
}
```



If we want to initiate request to metamask use this scripts :

```javascript
window.ethereum.request({
    method: "eth_requestAccounts",
});
```



Here is the example to send native token using metamask :

```javascript
const send = async function send(amount) {
  const accounts = await window.ethereum.request({
    method: "eth_requestAccounts",
  });

  const wei = web3.utils.toWei(amount, "ether");

  if (accounts.length > 0) {
    window.ethereum.request({
      method: "eth_sendTransaction",
      params: [
        {
          from: accounts[0],
          to: "0x7ceb23fd6bc0add59e62ac25578270cff1b9f619",
          value: web3.utils.toHex(wei),
        },
      ],
    });
  }
};
```

