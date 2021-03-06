---
title: dotnet nuget push 命令 - .NET Core CLI
description: dotnet nuget push 命令會將套件推送至伺服器並發行。
author: karann-msft
ms.author: mairaw
ms.date: 09/04/2018
ms.openlocfilehash: 23d27cef29008955850f9ed9f4a8baed9e7ad982
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2018
ms.locfileid: "45609998"
---
# <a name="dotnet-nuget-push"></a>dotnet nuget push

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>名稱

`dotnet nuget push` - 將套件推送至伺服器並發行。

## <a name="synopsis"></a>概要

# <a name="net-core-21tabnetcore21"></a>[.NET Core 2.1](#tab/netcore21)
```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [-k|--api-key] [-n|--no-symbols]
    [--no-service-endpoint] [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```
# <a name="net-core-20tabnetcore20"></a>[.NET Core 2.0](#tab/netcore20)
```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [-k|--api-key] [-n|--no-symbols]
    [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)
```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [-k|--api-key] [-n|--no-symbols]
    [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```
---

## <a name="description"></a>描述

`dotnet nuget push` 命令會將套件推送至伺服器並發行。 推送命令會使用在系統 NuGet 組態檔案或組態檔案鏈中找到的伺服器及認證詳細資料。 如需組態檔的詳細資訊，請參閱[設定 NuGet 行為](/nuget/consume-packages/configuring-nuget-behavior)。 NuGet 預設組態的取得方式如下：載入 *%AppData%\NuGet\NuGet.config* (Windows) 或 *$HOME/.local/share* (Linux/macOS)，接著從磁碟機根目錄開始直到目前目錄，載入其中的任何 *nuget.config* 或 *.nuget\nuget.config*。

## <a name="arguments"></a>引數

`ROOT`

指定套件推送目標的檔案路徑。

## <a name="options"></a>選項

# <a name="net-core-21tabnetcore21"></a>[.NET Core 2.1](#tab/netcore21)

`-d|--disable-buffering`

推送至 HTTP(S) 伺服器時停用緩衝處理以減少記憶體使用量。

`--force-english-output`

強制使用非變異英文文化特性來執行應用程式。

`-h|--help`

印出命令的簡短說明。

`-k|--api-key <API_KEY>`

伺服器的 API 金鑰。

`-n|--no-symbols`

不推送符號 (即使存在)。

`--no-service-endpoint`

不會將 "api/v2/package" 附加至來源 URL。

`-s|--source <SOURCE>`

指定伺服器 URL。 除非在 NuGet 組態檔中設定 `DefaultPushSource` 設定值，否則此選項為必要。

`-sk|--symbol-api-key <API_KEY>`

符號伺服器的 API 金鑰。

`-ss|--symbol-source <SOURCE>`

指定符號伺服器 URL。

`-t|--timeout <TIMEOUT>`

指定推送至伺服器的逾時 (以秒為單位)。 預設為 300 秒 (5 分鐘)。 指定 0 (零秒) 會套用預設值。

# <a name="net-core-20tabnetcore20"></a>[.NET Core 2.0](#tab/netcore20)

`-d|--disable-buffering`

推送至 HTTP(S) 伺服器時停用緩衝處理以減少記憶體使用量。

`--force-english-output`

強制使用非變異英文文化特性來執行應用程式。

`-h|--help`

印出命令的簡短說明。

`-k|--api-key <API_KEY>`

伺服器的 API 金鑰。

`-n|--no-symbols`

不推送符號 (即使存在)。

`-s|--source <SOURCE>`

指定伺服器 URL。 除非在 NuGet 組態檔中設定 `DefaultPushSource` 設定值，否則此選項為必要。

`-sk|--symbol-api-key <API_KEY>`

符號伺服器的 API 金鑰。

`-ss|--symbol-source <SOURCE>`

指定符號伺服器 URL。

`-t|--timeout <TIMEOUT>`

指定推送至伺服器的逾時 (以秒為單位)。 預設為 300 秒 (5 分鐘)。 指定 0 (零秒) 會套用預設值。

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

`-d|--disable-buffering`

推送至 HTTP(S) 伺服器時停用緩衝處理以減少記憶體使用量。

`--force-english-output`

強制使用非變異英文文化特性來執行應用程式。

`-h|--help`

印出命令的簡短說明。

`-k|--api-key <API_KEY>`

伺服器的 API 金鑰。

`-n|--no-symbols`

不推送符號 (即使存在)。

`-s|--source <SOURCE>`

指定伺服器 URL。 除非在 NuGet 組態檔中設定 `DefaultPushSource` 設定值，否則此選項為必要。

`-sk|--symbol-api-key <API_KEY>`

符號伺服器的 API 金鑰。

`-ss|--symbol-source <SOURCE>`

指定符號伺服器 URL。

`-t|--timeout <TIMEOUT>`

指定推送至伺服器的逾時 (以秒為單位)。 預設為 300 秒 (5 分鐘)。 指定 0 (零秒) 會套用預設值。

---

## <a name="examples"></a>範例

將 *foo.nupkg* 推送至預設推送來源，指定 API 金鑰：

`dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a`

將 *foo.nupkg* 推送至自訂推送來源 `http://customsource`，指定 API 金鑰：

`dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a -s http://customsource/`

將 *foo.nupkg* 推送至預設推送來源：

`dotnet nuget push foo.nupkg`

將 *foo.symbols.nupkg* 推送至預設符號來源：

`dotnet nuget push foo.symbols.nupkg`

將 *foo.nupkg* 推送至預設推送來源，指定 360 秒逾時：

`dotnet nuget push foo.nupkg --timeout 360`

將目前目錄中的所有 *.nupkg* 檔案推送至預設推送來源：

`dotnet nuget push *.nupkg`
