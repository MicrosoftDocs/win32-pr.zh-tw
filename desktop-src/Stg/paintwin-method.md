---
title: PaintWin 方法
description: PaintWin 方法
ms.assetid: e89794e6-c059-4531-a1e3-3a4972e0218d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b30e7a52640255934762943f910e367d76088d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311588"
---
# <a name="paintwin-method"></a>PaintWin 方法

以下是來自 GUIPAPER 的 CGuiPaper **PaintWin** 方法。Cpp。


```C++
HRESULT CGuiPaper::PaintWin(void)
  {
    HRESULT hr = E_FAIL;
    COLORREF crInkColor;
    SHORT nInkWidth;

    if (m_pIPaper && !m_bPainting && !m_bInking)
    {
      m_bPainting = TRUE;
      // Save and restore ink color and width since redraw otherwise
      // ends up changing these values in CGuiPaper.
      crInkColor = m_crInkColor;
      nInkWidth = m_nInkWidth;
      hr = m_pIPaper->Redraw(m_nLockKey);
      m_nInkWidth = nInkWidth;
      m_crInkColor = crInkColor;
      m_bPainting = FALSE;
    }

    return hr;
  }
```



**PaintWin** 基本上會呼叫 COPaper 的 **重繪** 方法。 在 [StoServe](structured-storage-server-sample--stoserve-.md) 範例中，會顯示 **重繪** 方法，以將 COPaper 的整個筆跡資料陣列廣播到所有連接的接收。 **PaintWin** 會呼叫伺服器端上的物件，將繪圖資料傳送回用戶端。

 

 




