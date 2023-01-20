# Azure Management Application

### 参照
  - [クイックスタート](https://learn.microsoft.com/ja-jp/azure/azure-resource-manager/managed-applications/publish-service-catalog-app?tabs=azure-powershell)
  - [Azure PowerShellリファレンス](https://learn.microsoft.com/ja-jp/powershell/azure/?view=azps-9.3.0)

# PowerShell補足

## コマンド、ファイル
- PowerShellのファイル拡張子は「.ps1」である。version互換を意識して「1」としたそうだが、いまだにps2はなく全て「.ps1」である。

## PowerShellモジュールのインストール

### インストール済みモジュールの確認方法
- 
  ``` ps
  # $PSHome　の内容を見る。Modules下にインストール済みの内容が格納されている
  echo $PSHome/Modules
  > /usr/local/microsoft/powershell/7/Modules

  # モジュールの一覧を取得する。
  ls $PSHome/Modules
  > Microsoft.PowerShell.Archive    Microsoft.PowerShell.Management Microsoft.PowerShell.Utility    PackageManagement               ThreadJob
  > Microsoft.PowerShell.Host       Microsoft.PowerShell.Security   PSReadLine                      PowerShellGet
  ```
