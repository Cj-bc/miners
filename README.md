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

  - activate miner with profile:

  ```
  $ minerutl start koto -p miningLove
  $ minerutl start koto on miningLove
  ```

  - stop miner

  ```
  $ minerutl stop koto -p miningLove
  $ minerutl stop koto on miningLove
  ```

  - add address

  ```
  $ minerutl add address koto "k1LR5z3PSHnm9mN9KmmHSfF1zc2GhsAZRKn"
  ```

  - make profile

  ```
  $ minerutl add profile miningLove "-o stratum+tcp://koto.mining.love:3101 -u <koto/address>"
  ```


