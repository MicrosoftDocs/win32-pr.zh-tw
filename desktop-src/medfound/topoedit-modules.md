---
description: TopoEdit 模組
ms.assetid: f3da2d13-a8ad-4db0-9d18-e94857f0abc7
title: TopoEdit 模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728f39edace5974d390746173308361b595c3b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026531"
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

 

 



