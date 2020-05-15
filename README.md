# C#で練習するアルゴリズムとデータ構造

## 概要

### 目的

### 前提

| ソフトウェア | バージョン | 備考 |
| :----------- | :--------- | :--- |
| .NETCore     | 3.1        |      |
| PowerShell   | 7.0        |      |

## 構成

- [構築](#構築)
- [配置](#配置)
- [運用](#運用)
- [開発](#開発)

## 詳細

### 構築

```powershell
dotnet new sln -o .
dotnet sln .\csharp-drill.sln add .\unit-testing-using-dotnet-test\PrimeService\PrimeService.csproj
dotnet sln .\csharp-drill.sln add .\unit-testing-using-dotnet-test\PrimeService.Tests\PrimeService.Tests.csprj
```

#### xUnit を使用した C#の単体テスト

```powershell
dotnet new sln -o unit-testing-using-dotnet-test
cd unit-testing-using-dotnet-test
dotnet new classlib -o PrimeService
ren .\PrimeService\Class1.cs PrimeService.cs
dotnet sln add ./PrimeService/PrimeService.csproj
dotnet new xunit -o PrimeService.Tests
dotnet add ./PrimeService.Tests/PrimeService.Tests.csproj reference ./PrimeService/PrimeService.csproj
dotnet sln add ./PrimeService.Tests/PrimeService.Tests.csproj
dotnet new gitignore
```

**[⬆ back to top](#構成)**

### 配置

**[⬆ back to top](#構成)**

### 運用

**[⬆ back to top](#構成)**

### 開発

**[⬆ back to top](#構成)**

## 参照

- [dotnet テストと xUnit を使用した .NET Core での単体テスト C#](https://docs.microsoft.com/ja-jp/dotnet/core/testing/unit-testing-with-dotnet-test})
- [Easy to create .gitignore for the dotnet developers](https://dev.to/rafalpienkowski/easy-to-create-gitignore-for-the-dotnet-developers-1h42)
