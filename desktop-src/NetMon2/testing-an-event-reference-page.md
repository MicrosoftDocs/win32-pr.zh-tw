---
description: " (ERP) 建立事件參考頁面的最後一個步驟是進行測試。"
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: 測試事件參考頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2aa9fb8697181085a9b74333dba82328e90b502e6590a764fac589efa8e6f90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676631"
---
# <a name="testing-an-event-reference-page"></a>測試事件參考頁面

 (ERP) 建立事件參考頁面的最後一個步驟是進行測試。 您可以在 HTML 瀏覽器（例如 Microsoft Internet Explorer）中查看檔案，以測試 ERP。 或者，您可以安裝 ERP 和其專家 DLL 來測試事件調用，並將其顯示在網路監視器事件檢視器中。

## <a name="viewing-erps-that-have-no-dll"></a>查看沒有 DLL 的 ERPs

若要在沒有已安裝專家 DLL 的情況下查看已完成的 ERP，請使用支援內嵌來源的 HTML 檢視器來開啟檔案。 下圖顯示在使用 Microsoft Internet Explorer 4.01 版顯示的情況下 [撰寫 erp](writing-an-event-reference-page.md) 時所述的 erp 檔案範例。

![範例 erp 檔案](images/ie-erp.png)

測試具有 DLL 的 ERPs

建立 ERP 檔案和 [**專家**](experts.md) DLL 之後，您就可以使用網路監視器來測試 ERPs 的完整功能。 假設 DLL 已進行調試，而且可以產生有效的事件。

**若要測試具有 DLL 的 ERPs**

1.  確認正確的專家 DLL 已安裝在適當的目錄中。 如需詳細資訊，請參閱 [安裝專家至網路監視器 2.1](installing-an-expert-to-network-monitor-2-1.md)。
2.  驗證 ERP 檔案的 [正確名稱](naming-an-event-reference-page.md) 。
3.  確認網路監視器目錄中的 ERPs [正確位置](installing-existing-erps-to-network-monitor-2-1.md) 。
4.  測試網路監視器 UI 中的專家 ERPs。
5.  產生測試事件。
6.  確認 ERP 出現在網路監視器事件檢視器中。

如需有關建立 ERP 的詳細資訊，請參閱：

-   [建立專家和監視事件參考頁面](creating-expert-and-monitor-event-reference-pages.md)
-   [撰寫事件參考頁面](writing-an-event-reference-page.md)
-   [命名事件參考頁面](naming-an-event-reference-page.md)

 

 



