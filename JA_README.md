English: [README.md](README.md)

---

# miners -- 仮想通貨マイナー用ユーティリティツール

仮想通貨マイナーを総合的に扱うユーティリティツールです

# feature

  The **General utility to use miners**

  - 複数のマイナーを同じコマンドで管理
  - プール毎、ポート毎にプロフィールを作成して素早く管理

# 依存パッケージ

  - [0k/shyaml](https://github.com/0k/shyaml)
  - [Cj-bc/blib](https://github.com/Cj-bc/blib)


# インストール方法

  - [ ] homebrew for macOS
  - [ ] homebrew for Linux
  - [ ] homebrew for Windows

# 使い方


  ```bash
  # コンフィグ設定
  # 1. マイナーの追加
  # 2. アドレスの追加
  # 3. プロフィールの追加
  $ miners add miner koto "koto-minerd"
  $ miners add address koto "k1LR5z3PSHnm9mN9KmmHSfF1zc2GhsAZRKn"
  $ miners add profile miningLove "-o stratum+tcp://koto.mining.love:3101 -u <koto/address>"

  # マイニングの開始
  $ miners start koto -p miningLove [-b]
  # もしくは
  $ miners start koto at miningLove [on background]

  # マイニング停止
  $ miners stop koto -p miningLove
  # もしくは
  $ miners stop koto at miningLove
  ```

# config file

  コンフィグファイルはyaml形式で書かれています

  - configpath: `~/.miners`

  ```yaml
  miners:
    - koto: koto-minerd
    - mona: mona-miner
  address:
    - &koto: k1LR5z3PSHnm9mN9KmmHSfF1zc2GhsAZRKn
  profiles:
    - miningLove: -o stratum+tcp://koto.mining.love:3101 -u *koto
  `
