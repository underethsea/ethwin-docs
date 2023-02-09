---
sidebar_position: 12

---

# Randomness

The stETH pool leverages the RNG service from the [Witnet Randomness Oracle](https://docs.witnet.io/smart-contracts/witnet-randomness-oracle) to select the prize winners. The prize awarding [contract](https://docs.steth.win/contracts) will send a request for a random number to the Witnet network. A predefined number of Witnet nodes will be selected to each generate a random number. Over several epochs, the randomly selected nodes commit, reveal and finally concatenate their numbers. Finally, the random number is calculated from a hash of the concatenated reveals.

Because Witnet uses a commit-reveal process and a hash of the reveal value is included in the commit transaction signature, no node can change the random number it will reveal once it has committed to solving a request. Hence, it can not change its random number based on the random numbers revealed by other nodes. Thus, as long as you have a single honest Witnet node participating in generating the final random number, it will be truly random.






