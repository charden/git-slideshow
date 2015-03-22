git-slideshow
===
# OverView

社内プレゼン用のGit資料

slideshow + markdown + guardで簡単スライド


# Install
## budnlerをインストール
```bash
$ gem install bundler
```

##  必要なライブラリをインストール
```bash
$ bundler install
```

## Slideshowテンプレートのインストール

```bash
$ slideshow install shower
```

## Build

```bash
$ slideshow build index.md -t shower
```

# Guardで自動ビルド、リロード

guardでindex.mdを監視

変更があればBuildを実行

LiveReloadでブラウザ更新(ChromeでLiveReloadのプラグインをインストールすること)

```ruby:Guardfile
guard 'shell' do
  watch(/index.md/) {|m|
    `slideshow b #{m[0]} -t shower ` }
end
guard 'livereload' do
  watch (%r{index.html})
end
```

```bash
$ guard
```
