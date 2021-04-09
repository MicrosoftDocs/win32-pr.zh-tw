---
description: 表示 debug 符號伺服器的相關資訊。
MS-HAID: vspixengine.SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SymbolServerInfo 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D57D87E4-BA94-4C6F-9D5F-999C61F4DD6F
api_name:
- SymbolServerInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 65bf07a8ff915668c6c059b831bd049d9a25d9a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108937"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span id="vspixengine.symbolserverinfo"></span>SymbolServerInfo 結構

表示 debug 符號伺服器的相關資訊。

## <a name="syntax"></a>語法


```C++
} SymbolServerInfo;
```

## <a name="members"></a>成員

**symbolPath**  
包含符號伺服器路徑的 COM 字串。

**symbolCacheDir**  
COM 字串，其中包含符號伺服器的快取目錄。

**publicSymbolServerName**  
COM 字串，其中包含符號伺服器的公用名稱。

**symbolExcludeList**  
COM 字串，指定要排除的符號清單。

**symbolIncludeList**  
COM 字串，指定要包含的符號清單。

**useExcludeList**  
如果忽略排除清單，則為 true;否則為 false。

**useMSSymbolServer**  
如果使用 Microsoft 符號伺服器，則為 true;否則為 false。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



