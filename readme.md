# Azure Management Application

### 参考
  - [クイックスタート](https://learn.microsoft.com/ja-jp/azure/azure-resource-manager/managed-applications/publish-service-catalog-app?tabs=azure-powershell)
  - [Azure PowerShellリファレンス](https://learn.microsoft.com/ja-jp/powershell/azure/?view=azps-9.3.0)

# サービスプリンシパル

上記ARMテンプレート発行のクイックスタートの手順の中で、GroupIDやRoleIDを指定する手順が示されているが、何の「グループ」なのか、がわからなかった。

### 参考
  - [もう多分怖くないサービスプリンシパル](https://tech-lab.sios.jp/archives/23371)

### 理解
- ARMに指定するグループには、AzureActiveDirectoryの「グループ」を指定する。
- このグループには、発行するアプリケーションが使用するアプリケーションを登録する。
- 登録されるアプリケーションには、Azureリソースを操作するための認証情報「サービスプリンシパル」が設定される。
- アプリケーションの認証情報をADユーザ（人）に依存させないため、「アプリケーション」自体をグループに属させる。
- アプリケーションのサービスプリンシパルを指定する。

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
