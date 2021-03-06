---
title: dotnet tool list 命令 - .NET Core CLI
description: dotnet tool list 命令會列出您電腦中指定的 .NET Core 通用工具。
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: e2bea974207d3098ed67b69ed16a72a03c44cd8b
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/01/2018
ms.locfileid: "47203472"
---
# <a name="dotnet-tool-list"></a>dotnet tool list

[!INCLUDE [topic-appliesto-net-core-21plus.md](../../../includes/topic-appliesto-net-core-21plus.md)]

## <a name="name"></a>名稱

`dotnet tool list` - 列出您電腦上的預設目錄或指定路徑中目前安裝的所有 [.NET Core 通用工具](global-tools.md)。

## <a name="synopsis"></a>概要

```console
dotnet tool list <-g|--global>
dotnet tool list <--tool-path>
dotnet tool list <-h|--help>
```

## <a name="description"></a>描述

`dotnet tool list` 命令可讓您列出電腦上所有使用者 (目前的使用者設定檔)，或指定路徑中安裝的所有 .NET Core 通用工具。 此命令會列出套件名稱、安裝的版本和通用工具命令。 若要使用這個 list 命令，您必須使用 `--global` 選項指定您要查看所有使用者範圍工具，或使用 `--tool-path` 選項指定自訂路徑。

## <a name="options"></a>選項

`-g|--global`

列出使用者範圍通用工具。 無法與 `--tool-path` 選項合併使用。 如果未指定此選項，您必須指定 `--tool-path` 選項。

`-h|--help`

印出命令的簡短說明。

`--tool-path <PATH>`

指定用來尋找通用工具的自訂位置。 PATH 可為絕對路徑或相對路徑。 無法與 `--global` 選項合併使用。 如果未指定此選項，您必須指定 `--global` 選項。

## <a name="examples"></a>範例

列出您電腦上所有使用者 (目前的使用者設定檔) 安裝的所有通用工具使用者：

`dotnet tool list -g`

列出特定 Windows 資料夾中的通用工具：

`dotnet tool list --tool-path c:\global-tools`

列出特定 Linux/macOS 資料夾中的通用工具：

`dotnet tool list --tool-path ~/bin`

## <a name="see-also"></a>另請參閱

* [.NET Core 通用工具](global-tools.md)