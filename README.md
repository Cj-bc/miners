日本語: [JA_README.md](JA_README.md)

---

# miners -- cryptcoin miners utility tool

This is a utility to control various kinds of miners

# feature

  The **General utility to use miners**

  - manage miners with one command
  - make profiles for each miner, each pool

# dependency

  - [0k/shyaml](https://github.com/0k/shyaml)
  - [Cj-bc/blib](https://github.com/Cj-bc/blib)

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
  $ miners add miner koto "koto-minerd"
  $ miners add address koto "k1LR5z3PSHnm9mN9KmmHSfF1zc2GhsAZRKn"
  $ miners add profile miningLove "-o stratum+tcp://koto.mining.love:3101 -u <koto/address>"

  # start mining
  $ miners start koto -p miningLove [-b]
  # or
  $ miners start koto at miningLove [on background]

  # stop mining
  $ miners stop koto -p miningLove
  # or
  $ miners stop koto at miningLove
  ```

# config file

  config file is written in yaml

  - configpath: `~/.miners`

  ```yaml
  miners:
    - koto: koto-minerd
    - mona: mona-miner
  address:
    - &koto: k1LR5z3PSHnm9mN9KmmHSfF1zc2GhsAZRKn
  profiles:
    - miningLove: -o stratum+tcp://koto.mining.love:3101 -u *koto
  ```
