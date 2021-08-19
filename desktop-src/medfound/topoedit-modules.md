---
description: TopoEdit 模組
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: TopoEdit 模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc95848a533ba67599c114917ebe502f42a4fe859df9c1ac6bf5acfc40bb393c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057713"
---
# <a name="topoedit-modules"></a>TopoEdit 模組

TopoEdit 工具隨附于 Windows Server 2008 和更新版本的 Windows SDK。 此工具需要 Windows Vista 或更新版本。

TopoEdit 模組位於 SDK 的 Bin 資料夾中。 這些模組包括：

-   TopoEdit.exe-應用程式可執行檔
-   TEDUTIL.dll-擴充 DLL

SDK 安裝會註冊 DLL。 但是，如果失敗，請在命令提示字元中執行下列命令。


```C++
Regsvr32 <Install path>\Microsoft SDKs\Windows\v6.0\Bin\TEDUTIL.dll
```



TopoEdit 的原始程式碼也提供為 Windows SDK 中的範例。 它位於下列目錄：

<samples root>\\多媒體 \\ 媒體基礎 \\ TopoEdit

## <a name="related-topics"></a>相關主題

<dl> <dt>

[TopoEdit 簡介](introduction-to-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



