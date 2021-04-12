---
title: InkDraw 方法
description: CGuiPaper 也會保留 m \_ bInking 旗標。 InkStart 會將它設定為 TRUE，以表示繪圖順序正在處理中。 例如，InkDraw 方法會使用此旗標來判斷是否應該繪製和儲存筆跡資料。
ms.assetid: 0fe9d029-1522-4caf-8efb-0a4eb2b59958
keywords:
- InkDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41973d3f8560f25a81ac1deb782bada51b015239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372466"
---
# <a name="inkdraw-method"></a>InkDraw 方法

CGuiPaper 也會保留 m \_ bInking 旗標。 [InkStart](inkstart-method.md) 會將它設定為 **TRUE** ，以表示繪圖順序正在處理中。 例如，InkDraw 方法會使用此旗標來判斷是否應該繪製和儲存筆跡資料。

以下是來自 GUIPAPER 的 InkDraw 方法。Cpp。


```C++
HRESULT CGuiPaper::InkDraw(
                       SHORT nX,
                       SHORT nY)
  {
    if (m_bInking)
    {
      // Start this ink line at previous old position.
      MoveToEx(m_hDC, m_OldPos.x, m_OldPos.y, NULL);

      // Assign new old position and draw the new line.
      LineTo(m_hDC, m_OldPos.x = nX, m_OldPos.y = nY);

      // Ask the Paper object to save this data.
      if (m_bInkSaving)
        m_pIPaper->InkDraw(m_nLockKey, nX, nY);
    }

    return NOERROR;
  }
```



如果 m \_ bInking 為 **FALSE**，則這個方法不會執行任何動作。 當使用者只要在用戶端視窗上移動滑鼠，而不按下滑鼠左鍵時，就會發生這種情況。

InkDraw 清楚地擁有雙重責任。 Win32 MoveToEx 和 LineTo 呼叫是在 GUI 畫面上繪製線條影像 (使用保留在 m hDC) 的裝置內容控制碼 \_ 。 筆墨資料也會傳遞至 COPaper 物件，以使用 [IPaper](ipaper-methods.md) 介面的 InkDraw 方法進行錄製。 當 m \_ bInkSaving 為 **FALSE** 時，InkDraw 會繪製線條影像，但不會將資料儲存在 COPaper 中。 這是在重新繪製期間使用的條件。

 

 




