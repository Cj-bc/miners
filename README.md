# minerutl -- cryptcoin miners utility tool

This is a utility to control various kinds of miners

# feature

  The **General utility to use miners**

  - manage miners with one command
  - make profiles for each miner, each pool

# installation

  - [ ] homebrew for macOS
  - [ ] homebrew for Linux
  - [ ] homebrew for Windows

# usage


  ```bash
  # initialize configs
  # 1. add miner
  # 2. add addres
  # 3. add profile
  $ minerutl add miner koto "koto-minerd"
  $ minerutl add address koto "k1LR5z3PSHnm9mN9KmmHSfF1zc2GhsAZRKn"
  $ minerutl add profile miningLove "-o stratum+tcp://koto.mining.love:3101 -u <koto/address>"

  # start mining
  $ minerutl start koto -p miningLove [-b]
  # or
  $ minerutl start koto at miningLove [on background]

  # stop mining
  $ minerutl stop koto -p miningLove
  # or
  $ minerutl stop koto at miningLove
  ```
