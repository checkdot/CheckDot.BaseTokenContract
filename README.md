# CheckDot Base Token Contract

### CheckDot Interface

The smart contract is an ERC20 token that respects the EIP-20 standard represented by the IERC20 interface.  
We added an interface to have the holding time of the holders, represented by the IHoldingTime interface.  
We have added an interface to allow token burning, represented by the IHoldingTime interface.  

Here is the interface of the token:  

```solidity
interface ICheckDot {
    function totalSupply() external view returns (uint256);
    function balanceOf(address account) external view returns (uint256);
    function holdTimeOf(address account) external view returns (uint256);
    function transfer(address recipient, uint256 amount) external returns (bool);
    function allowance(address owner, address spender) external view returns (uint256);
    function approve(address spender, uint256 amount) external returns (bool);
    function transferFrom(address sender, address recipient, uint256 amount) external returns (bool);
    function burn(uint256 amount) external returns (bool);
}
```

## Token Published address

https://basescan.org/token/0x0cBD6fAdcF8096cC9A43d90B45F65826102e3eCE