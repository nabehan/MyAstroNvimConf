# AstroNvim テンプレート

**注記:** これは AstroNvim v4+ 用です

[AstroNvim](https://github.com/AstroNvim/AstroNvim) を始めるためのテンプレートです。

## 🛠️ インストール方法

#### 現在の nvim と共有フォルダのバックアップを取る

```shell
mv ~/.config/nvim ~/.config/nvim.bak
mv ~/.local/share/nvim ~/.local/share/nvim.bak
mv ~/.local/state/nvim ~/.local/state/nvim.bak
mv ~/.cache/nvim ~/.cache/nvim.bak
```

#### AstroNvim/テンプレートから新しいユーザーリポジトリを作成する

本家 [AstroNvim/template](https://github.com/AstroNvim/template) の github に移動します。

右上の “Use this template” ボタンを押して、ユーザー設定を保存する新しいリポジトリを作成します。

GitHubでユーザー設定を追跡したくない場合は、本家のリポジトリを直接クローンすることもできます。

#### リポジトリをクローンする

```shell
git clone https://github.com/<your_user>/<your_repository> ~/.config/nvim
```

#### Neovim を起動する

```shell
nvim
```

自動で各種 plugin が インストールされます。

## カスタマイズ方法の覚え書き

### plugin の追加

#### Astrocommunity に無い plugin の追加

`puts '~/.config/nvim/lua/plugins/user.lua' ` に変更を加える

1行目をコメントアウトします

目的の plugin を 次のように記載します。

```lua
-- if true then return {} end -- WARN: REMOVE THIS LINE TO ACTIVATE THIS FILE

---@type LazySpec
return {
-- == Examples of Overriding Plugins ==
  "h-hg/fcitx.nvim",
  {
    "h-hg/fcitx.nvim",
  },
}
```
