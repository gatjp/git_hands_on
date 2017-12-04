# Git ハンズオン

実際に Git コマンドを操作することで、 Git に慣れてスムーズにチーム開発に入れることを目標にします。

## Git イメージ図

## Git のインストール・設定

### Mac

Mac には標準で Git がインストールされているはず。
Homebrew で最新版を入れたければ、以下などを参照。

- [HomebrewでGitをインストールする \- Qiita](https://qiita.com/micheleno13/items/133aee005ae37c28960e)
- [HomebrewでGitをインストールする \- 1\.21 jigowatts](http://sh-yoshida.hatenablog.com/entry/2017/02/11/213323)

### Windows

今回は、 Git for Windows を使用する。

[Git for Windows](https://git-for-windows.github.io/) からダウンロードしてインストールする。

### ユーザー名、メールアドレスを設定する

```
git config --global user.name "y.kida"
git config --global user.email "y.kida@gingerapp.co.jp"
```

以下で確認する

```
git config --list
```

## Pull Request (PR) の流れ

**ここからハンズオン開始！！**

## リポジトリをクローンする

```
git clone git@github.com:gatjp/git_hands_on.git
```

### ブランチを切る

```
git checkout -b "y-kida-pr"
```

### ファイルを修正する

なんでも良いので、 `fixme.md` に1行追加する。

fixme.md

```
# このファイルを編集してみましょう

hogehoge
```

### 状態を確認する

```
$ git status
On branch y-kida-pr
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   fixme.md
```

### 差分を確認する

```
$ git diff
diff --git a/fixme.md b/fixme.md
index 78085de..da6f413 100644
--- a/fixme.md
+++ b/fixme.md
@@ -1 +1,3 @@
 # このファイルを編集してみましょう
+
+hogehoge
```

### 変更したファイルをインデックスに追加する

```
git add fixme.md
```

全ての変更ファイルを追加することもできます。

```
git add .
```

### インデックスに追加したファイルをコミットする

```
git commit -m "fixme.md に一行追加"
```

### リモートリポジトリにブランチを作成する（変更を反映する）

```
git push origin y-kida-pr
```

### GitHub で PR を立てる

実際に立ててみる。

### コメントをもらったら修正する

他の人にコメントをもらって、それに沿って修正してみる。

### approve してもらったらマージする

今回は、実際にはマージしない。
