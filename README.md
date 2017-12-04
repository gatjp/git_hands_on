# Git ハンズオン

実際に Git コマンドを操作することで、 Git に慣れてスムーズにチーム開発に入れることを目標にします。

## Git イメージ図

## Pull Request (PR) の流れ

**ここからハンズオン開始！！**

### ブランチを切る

```
git checkout -b "y-kida-pr"
```

### ファイルを修正する

なんでも良いので、1行追加する。

```md:fixme.md
# このファイルを編集してみましょう

hogehoge
```

### 状態を確認する

```bash
$ git status
On branch y-kida-pr
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   fixme.md
```

### 差分を確認する

```bash
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
