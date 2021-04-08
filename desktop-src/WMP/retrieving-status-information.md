---
title: 正在抓取狀態資訊
description: 正在抓取狀態資訊
ms.assetid: 61561520-705a-4d06-a72c-c1cc6315f54e
keywords:
- Windows Media Player 線上商店，下載管理員
- 線上商店、下載管理員
- 輸入2個線上商店、下載管理員
- Windows Media Player 線上商店，正在抓取狀態
- 線上商店，正在抓取狀態
- 輸入2個線上商店，正在抓取狀態
- Windows Media Player，下載管理員
- Windows Media Player 下載管理員
- 下載管理員
- 正在抓取狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 155d1c9d949306ae5cda3ffff6a7a55fd3bae23c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674680"
---
# <a name="retrieving-status-information"></a>正在抓取狀態資訊

狀態資訊會使用 **Init** 函式中所建立的計時器進行更新。 所有狀態都會使用相同的計時器進行更新。 計時器事件的函式名稱為 **OnTimer**。

**OnTimer** 會根據使用者選取專案來決定要顯示的資訊，此資訊會儲存在名為 g oCurrentDLItem 的全域變數中 \_ 。 函數會先測試大小或進度值是否有效，並為每個案例建立字串。


```C++
var Size = g_oCurrentDLItem.size <=0 ? "Waiting..." : g_oCurrentDLItem.size + " bytes";
var Progress = g_oCurrentDLItem.progress <=0 ? "Waiting..." : g_oCurrentDLItem.progress + " bytes";

```



如果值有效，則字串代表位元組計數。 如果值無效，例如-1，則字串會提供訊息，通知使用者資訊尚無法使用。

接下來， **switch** 區塊會決定是否要完成或取消所選取專案的下載。 如果任一案例都是 true，則會據此更新變數大小或進度的值。


```C++
switch(g_oCurrentDLItem.downloadState)
{
    case 3:            
        Size = "Completed";
        Progress = "Completed";
        break;
        
    case 4:
        Size = "Canceled";
        Progress = "Canceled";
        break;
        
    default:
        break;                
}

```



最後，狀態資訊會顯示在名為 dlstate 的 DIV 元素中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用下載管理員**](using-the-download-manager.md)
</dt> </dl>

 

 




