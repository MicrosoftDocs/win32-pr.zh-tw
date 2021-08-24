---
description: 當使用者展開該節點時，附件嵌入式管理單元延伸模組必須將本身新增至 [服務] 節點底下。
ms.assetid: af853c29-11c2-4fd0-ad81-80aebeb74cc3
title: 新增附件嵌入式管理單元擴充功能節點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fa9d02167106bfd8c8860f34abdc6bc8f362697a82e3d0f7b0ef1983df07a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969747"
---
# <a name="adding-an-attachment-snap-in-extension-node"></a>新增附件嵌入式管理單元擴充功能節點

當使用者展開該節點時，附件嵌入式管理單元延伸模組必須將本身新增至 [服務] 節點底下。

當使用者展開其中一個 [安全性設定] 嵌入式管理單元下的 [服務] 節點時，MMC 會使用 [**IComponentData：：**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) NOTIFICATION 和 MMCN \_ EXPAND 通知訊息來通知 [安全性設定] 嵌入式管理單元，再加上它的所有延伸模組。

然後，[安全性設定] 嵌入式管理單元會從 *lpDataObject* 中解壓縮其內部格式，此格式會從 MMC 主要架構傳遞為類型 **lpDataObject**。 當它看到 [服務] 節點類型時，它會停止處理。 然後，附件嵌入式管理單元擴充功能會從 *lpDataObject* 中解壓縮節點類型。 如果節點類型是服務定義的其中一個節點類型，則附件嵌入式管理單元延伸模組會在指定的父節點下插入其根節點。

請注意，在此範例中，ExtractNodeType 是擴充功能所執行的私用函式。 此延伸模組會檢查資料物件以取得節點類型。 不會顯示 ExtractNodeType 的執行。


```C++
//  Detect which extension node to expand.
GUID* nodeType = ExtractNodeType(lpdataObject);

if (NULL == nodeType)
{
  return S_OK;
}

if (TRUE == ::IsEqualGUID(*nodeType, cNodetypeSceTemplateServices))
{
  folderType = ATTACHMENT_STATIC;  // defined by attachment writer
}

else if (TRUE == ::IsEqualGUID
    (*nodeType, cNodetypeSceAnalysisServices))
{
  folderType = ATTACHMENT_STATIC_ANALYSIS;
               // defined by attachment writer
}

//  Free resources.
::GlobalFree(reinterpret_cast<HANDLE>(nodeType));

//  Add service attachment root node and remember it as the
//  root of the SMB extension namespace.
//  ...
```



 

 
