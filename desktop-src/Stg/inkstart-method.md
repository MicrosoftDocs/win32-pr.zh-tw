---
title: InkStart 方法
description: InkStart、InkDraw 和 InkStop 方法都使用 Win32 GUI 結構，例如裝置內容和畫筆物件。
ms.assetid: a639e1d2-6d81-472b-b639-d237e202020f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e25d02c4490106180298b6977ec539bd96fd03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932451"
---
# <a name="inkstart-method"></a>InkStart 方法

**InkStart**、 [**InkDraw**](inkdraw-method.md)和 [**INKSTOP**](cguipaper-methods.md) 方法都使用 Win32 GUI 結構，例如裝置內容和畫筆物件。 這說明為什麼需要 CGuiPaper 作為不同的封裝層級。 繪圖紙的 GUI 層面是在 CGuiPaper 中處理。 COPaper 物件只會傳送筆墨資料。

CGuiPaper 層級封裝的另一個設計原因是其 **InkStart**、 [**InkDraw**](inkdraw-method.md)和 [**InkStop**](cguipaper-methods.md) 方法的雙重本質。 他們不只會在 COPaper 上呼叫來記錄筆墨資料，也會在繪製時繪製繪圖的視覺影像。 CGuiPaper 會保留 m \_ bInkSaving 旗標來管理此雙重本質。 當 m \_ bInkSaving 為 FALSE 時，會在螢幕上繪製影像，但不會將資料傳送到 COPaper 進行錄製。

當使用者未移動滑鼠，但 COPaper 的筆墨資料正在重新傳送至 CGuiPaper 以進行自動重畫時，此配置會用於重新繪製。 您可以藉 \_ 由呼叫 [**InkSaving**](cguipaper-methods.md) 方法，告知 CGuiPaper 設定 m bInkSaving 旗標。

下列範例程式碼片段說明 GUIPAPER 的 **InkStart** 方法。CPP 和接收器。Cpp。

## <a name="inkstart-method-guipapercpp"></a>InkStart 方法 (GUIPAPER。CPP) 


```C++
HRESULT CGuiPaper::InkStart(
                       SHORT nX,
                       SHORT nY)
  {
    HRESULT hr = E_FAIL;

    if (m_nLockKey || (!m_nLockKey && !m_bInkSaving))
    {
      // Start an ink drawing sequence only if one is not in progress.
      if (!m_bInking)
      {
        // Remember start position.
        m_OldPos.x = nX;
        m_OldPos.y = nY;

        // Delete old pen.
        if (m_hPen)
          DeleteObject(m_hPen);

        // Create and select the new drawing pen.
        m_hPen = CreatePen(PS_SOLID, m_nInkWidth, m_crInkColor);
        SelectObject(m_hDC, m_hPen);

        hr = NOERROR;

        // Ask the Paper object to mark the start of the ink drawing
        // sequence in the current ink color.
        if (m_pIPaper && m_bInkSaving)
        {
          hr = m_pIPaper->InkStart(
                            m_nLockKey,
                            nX,
                            nY,
                            m_nInkWidth,
                            m_crInkColor);
          // Capture the Mouse.
          SetCapture(m_hWnd);

          // We've modified the ink data--it is now "dirty" with
          // respect to the compound file image. Set dirty flag.
          m_bDirty = TRUE;
        }

        // Set inking flag to TRUE.
        m_bInking = TRUE;
      }
    }

    return hr;
  }
```



## <a name="inkstart-method-sinkcpp"></a> (接收器的 InkStart 方法。CPP) 

**StoClien** 會在其 COPaperSink 物件中，以呼叫連接 **IPaperSink** 介面的形式接收繪圖資料。 這些方法會對應至 CGuiPaper 中的類似 **InkStart**、 [**InkDraw**](inkdraw-method.md)和 [**InkStop**](cguipaper-methods.md) 方法。


```C++
STDMETHODIMP COPaperSink::CImpIPaperSink::InkStart(
                                              SHORT nX,
                                              SHORT nY,
                                              SHORT nWidth,
                                              COLORREF crInkColor)
  {
    // Turn off ink saving to the COPaper object.
    m_pBackObj->m_pGuiPaper->InkSaving(FALSE);

    // Play the data back to the CGuiPaper for display only.
    m_pBackObj->m_pGuiPaper->InkWidth(nWidth);
    m_pBackObj->m_pGuiPaper->InkColor(crInkColor);
    m_pBackObj->m_pGuiPaper->InkStart(nX, nY);

    return NOERROR;
  }
```



當接收器中呼叫 **InkStart** 時，它會呼叫 CGuiPaper 來關閉儲存至 COPaper 的筆墨。 COPaper 不需要接收正在傳送之資料的回顯複本。 當接收器中呼叫 [**InkDraw**](inkdraw-method.md) 時，它只會將呼叫傳遞至 **CGuiPaper：： InkDraw**。 在接收中呼叫 [**InkStop**](cguipaper-methods.md) 時，會呼叫 CGuiPaper 來開啟筆墨的儲存。 結果會將 COPaper 的筆墨資料播放 CGuiPaper 為僅供顯示之用。

您可以選擇 [接收器] 功能表上的 [中斷連線] 選項，在 **IPaperSink** 中斷連接時測試 **StoClien** 的行為。 在中斷連接接收器之後，請從 [說明] 功能表選擇 [關於]，做為實驗。 這將會顯示 [About （關於）] 對話方塊，其中涵蓋 **StoClien** 的繪圖部分。 按一下 [關於] 對話方塊中的 [確定]。 請注意，所涵蓋的繪圖部分現在已消失。 繪圖資料不會遺失，但影像的一部分是。 用戶端收到了 WM \_ 油漆訊息併發出 [**IPaper：：重繪**](ipaper--redraw.md) 方法。 但因為接收器未連接，所以它不會收到重新繪製繪圖的 **IPaperSink** 呼叫。

您也可以藉由將 **StoClien** 降到最低，然後加以還原，來測試此行為。 在此情況下，整個繪圖影像會遺失，且需要重新繪製。 若要在其中一個測試之後重新繪製繪圖影像，請使用 [接收] 功能表重新連接，然後從 [繪製] 功能表 [**中選擇 [重新繪製]**](ipaper--redraw.md) 。

 

 




