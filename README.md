# language-hsp3-ex for VSCode

現在公開されているlanguage-hsp3に、HSP3付随モジュールやWin32APIのシンタックスハイライトを追加するものです。
 
![image](https://raw.githubusercontent.com/UMAGODi/vscode-language-hsp3-extended/master/highlight.png)

## 実装済みハイライト
<details><summary>一覧</summary>

### HSP3付随モジュール
* a2d
* hgimg3
* hgimg4
### Win32API
* advapi32
* comctl32
* comdlg
* gdi32
* kernel32
* shell32
* user32</details>

## インストール
必要なもの
* Visual Studio Code
* この拡張機能
* language-hsp3 (無くともハイライトは可能)

手順
1. language-hsp3をインストールする
2. language-hsp3-exをインストールする
3. 試しにHSPファイル(.hsp, .as)にalCreateImageやSetWindowLong等を書いてみて反映されていれば完了

## Win32API定数について
当初はこのパッケージでWin32API定数も対応するつもりでしたが、何せ**量が尋常ではなく(25万個)** 内容が長いファイルほど開いた際にエディタが重くなるため対応は断念しました。 

**が、** 別パッケージで対応することにしました。(何故か別パッケージすると少しは軽くなる)  
Win32API版は`language-hsp3-constant`のパッケージ名で公開しています。レポジトリは[こちら](https://github.com/UMAGODi/vscode-language-hsp3-constant)

## スコープ名詳細
色を好みのものに変更したいとき等に使用するスコープ名です。
<details><summary>一覧</summary>

|名前    |スコープ名                    |
|:-------|:-----------------------------|
|a2d     |keyword.module.a2d.hsp3       |
|hgimg3  |keyword.module.hgimg3.hsp3    |
|hgimg4  |keyword.module.hgimg4.hsp3    |
|advapi32|keyword.win32api.advapi32.hsp3|
|comctl32|keyword.win32api.comctl32.hsp3|
|comdlg32|keyword.win32api.comdlg32.hsp3|
|gdi32   |keyword.win32api.gdi32.hsp3   |
|kernel32|keyword.win32api.kernel32.hsp3|
|shell32 |keyword.win32api.shell32.hsp3 |
|user32  |keyword.win32api.user32.hsp3  |

### サンプル  
_Win32APIの色を赤に変更したい場合 (settings.json)_
```json
{
  "scope": "keyword.win32api",
  "settings": {
    "foreground": "#FF0000"
  }
}
```
</details>

## バージョン履歴

### v1.0.1 [2020/03/09]
* 初版