# ERC20 Staking Contract

This contract allows users to stake ERC20 tokens and earn rewards based on the amount of tokens staked and the time elapsed in blocks.

## 🚀 Main Features

- **ERC20 Token Staking**: Users can deposit tokens and start earning rewards per block.
- **Token Withdrawal**: Withdraw staked tokens either partially or fully.
- **Reward Claiming**: Accumulated rewards can be claimed at any time.
- **Reward Rate Adjustment**: The owner can adjust the reward rate per block.

## 🔧 Key Functionalities

### String Comparison

The `compareStrings` function is included, which allows comparing two strings using `keccak256`. This pattern is useful in Solidity because there is no native function to directly compare strings. The function returns `true` if the strings are equivalent.

```solidity
function compareStrings(string memory string1, string memory string2) public pure returns (bool) {
    return keccak256(abi.encodePacked(string1)) == keccak256(abi.encodePacked(string2));
}
```

 Staking

- **stake(uint256 _amount)**: Allows users to deposit tokens into the contract and start accumulating rewards.

Token Withdrawal

- **withdraw(uint256 _amount)**: Withdraw staked tokens while maintaining pending rewards.

Reward Claiming

- **claimRewards()**: Claims the accumulated rewards up to the current moment. Rewards are calculated based on the blocks the user has staked.

## 📜 Requirements

- The token must adhere to the ERC20 standard.
- Users must approve the contract to spend tokens on their behalf beforehand.

## 💻 Creators

- [@kevinlatino](https://github.com/kevinlatino)
- [@villarley](https://github.com/villarley)
