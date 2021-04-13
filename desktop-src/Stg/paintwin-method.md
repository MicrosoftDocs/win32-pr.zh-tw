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
# <a name="paintwin-method"></a><span data-ttu-id="86faf-103">PaintWin 方法</span><span class="sxs-lookup"><span data-stu-id="86faf-103">PaintWin Method</span></span>

<span data-ttu-id="86faf-104">以下是來自 GUIPAPER 的 CGuiPaper **PaintWin** 方法。Cpp。</span><span class="sxs-lookup"><span data-stu-id="86faf-104">The following is CGuiPaper's **PaintWin** method from GUIPAPER.CPP.</span></span>


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



<span data-ttu-id="86faf-105">**PaintWin** 基本上會呼叫 COPaper 的 **重繪** 方法。</span><span class="sxs-lookup"><span data-stu-id="86faf-105">**PaintWin** essentially calls COPaper's **Redraw** method.</span></span> <span data-ttu-id="86faf-106">在 [StoServe](structured-storage-server-sample--stoserve-.md) 範例中，會顯示 **重繪** 方法，以將 COPaper 的整個筆跡資料陣列廣播到所有連接的接收。</span><span class="sxs-lookup"><span data-stu-id="86faf-106">In the [StoServe](structured-storage-server-sample--stoserve-.md) sample, the **Redraw** method was shown to broadcast COPaper's entire ink data array to all connected sinks.</span></span> <span data-ttu-id="86faf-107">**PaintWin** 會呼叫伺服器端上的物件，將繪圖資料傳送回用戶端。</span><span class="sxs-lookup"><span data-stu-id="86faf-107">**PaintWin** calls an object on the server side to send back the drawing data to the client.</span></span>

 

 




