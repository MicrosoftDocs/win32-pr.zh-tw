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
# <a name="inkstart-method"></a><span data-ttu-id="bc74e-103">InkStart 方法</span><span class="sxs-lookup"><span data-stu-id="bc74e-103">InkStart Method</span></span>

<span data-ttu-id="bc74e-104">**InkStart**、 [**InkDraw**](inkdraw-method.md)和 [**INKSTOP**](cguipaper-methods.md) 方法都使用 Win32 GUI 結構，例如裝置內容和畫筆物件。</span><span class="sxs-lookup"><span data-stu-id="bc74e-104">**InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods all use Win32 GUI constructs such as device contexts and pen objects.</span></span> <span data-ttu-id="bc74e-105">這說明為什麼需要 CGuiPaper 作為不同的封裝層級。</span><span class="sxs-lookup"><span data-stu-id="bc74e-105">This illustrates why CGuiPaper is needed as a separate level of encapsulation.</span></span> <span data-ttu-id="bc74e-106">繪圖紙的 GUI 層面是在 CGuiPaper 中處理。</span><span class="sxs-lookup"><span data-stu-id="bc74e-106">The GUI aspects of the drawing paper are handled in CGuiPaper.</span></span> <span data-ttu-id="bc74e-107">COPaper 物件只會傳送筆墨資料。</span><span class="sxs-lookup"><span data-stu-id="bc74e-107">The COPaper object is sent only ink data.</span></span>

<span data-ttu-id="bc74e-108">CGuiPaper 層級封裝的另一個設計原因是其 **InkStart**、 [**InkDraw**](inkdraw-method.md)和 [**InkStop**](cguipaper-methods.md) 方法的雙重本質。</span><span class="sxs-lookup"><span data-stu-id="bc74e-108">Another design reason for the CGuiPaper level of encapsulation is the dual nature of its **InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods.</span></span> <span data-ttu-id="bc74e-109">他們不只會在 COPaper 上呼叫來記錄筆墨資料，也會在繪製時繪製繪圖的視覺影像。</span><span class="sxs-lookup"><span data-stu-id="bc74e-109">They not only call on COPaper to record the ink data as it occurs, they also paint a visual image of the drawing as it occurs.</span></span> <span data-ttu-id="bc74e-110">CGuiPaper 會保留 m \_ bInkSaving 旗標來管理此雙重本質。</span><span class="sxs-lookup"><span data-stu-id="bc74e-110">CGuiPaper keeps an m\_bInkSaving flag to manage this dual nature.</span></span> <span data-ttu-id="bc74e-111">當 m \_ bInkSaving 為 FALSE 時，會在螢幕上繪製影像，但不會將資料傳送到 COPaper 進行錄製。</span><span class="sxs-lookup"><span data-stu-id="bc74e-111">When m\_bInkSaving is FALSE, the image is drawn on screen but the data is not sent to COPaper for recording.</span></span>

<span data-ttu-id="bc74e-112">當使用者未移動滑鼠，但 COPaper 的筆墨資料正在重新傳送至 CGuiPaper 以進行自動重畫時，此配置會用於重新繪製。</span><span class="sxs-lookup"><span data-stu-id="bc74e-112">This scheme is used in repainting when the user is not moving the mouse but COPaper's ink data is being resent to CGuiPaper for automatic repainting.</span></span> <span data-ttu-id="bc74e-113">您可以藉 \_ 由呼叫 [**InkSaving**](cguipaper-methods.md) 方法，告知 CGuiPaper 設定 m bInkSaving 旗標。</span><span class="sxs-lookup"><span data-stu-id="bc74e-113">CGuiPaper can be told to set the m\_bInkSaving flag by calling its [**InkSaving**](cguipaper-methods.md) method.</span></span>

<span data-ttu-id="bc74e-114">下列範例程式碼片段說明 GUIPAPER 的 **InkStart** 方法。CPP 和接收器。Cpp。</span><span class="sxs-lookup"><span data-stu-id="bc74e-114">The following sample code snippets illustrate the **InkStart** methods of GUIPAPER.CPP AND SINK.CPP.</span></span>

## <a name="inkstart-method-guipapercpp"></a><span data-ttu-id="bc74e-115">InkStart 方法 (GUIPAPER。CPP) </span><span class="sxs-lookup"><span data-stu-id="bc74e-115">InkStart Method (GUIPAPER.CPP)</span></span>


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



## <a name="inkstart-method-sinkcpp"></a><span data-ttu-id="bc74e-116"> (接收器的 InkStart 方法。CPP) </span><span class="sxs-lookup"><span data-stu-id="bc74e-116">InkStart Method (SINK.CPP)</span></span>

<span data-ttu-id="bc74e-117">**StoClien** 會在其 COPaperSink 物件中，以呼叫連接 **IPaperSink** 介面的形式接收繪圖資料。</span><span class="sxs-lookup"><span data-stu-id="bc74e-117">**StoClien** receives the drawing data in the form of calls to the connected **IPaperSink** interface in its COPaperSink object.</span></span> <span data-ttu-id="bc74e-118">這些方法會對應至 CGuiPaper 中的類似 **InkStart**、 [**InkDraw**](inkdraw-method.md)和 [**InkStop**](cguipaper-methods.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="bc74e-118">These methods correspond to the similar **InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods in CGuiPaper.</span></span>


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



<span data-ttu-id="bc74e-119">當接收器中呼叫 **InkStart** 時，它會呼叫 CGuiPaper 來關閉儲存至 COPaper 的筆墨。</span><span class="sxs-lookup"><span data-stu-id="bc74e-119">When **InkStart** is called in the sink, it calls CGuiPaper to turn off ink saving to COPaper.</span></span> <span data-ttu-id="bc74e-120">COPaper 不需要接收正在傳送之資料的回顯複本。</span><span class="sxs-lookup"><span data-stu-id="bc74e-120">COPaper does not need to receive an echoed copy of the data it is sending.</span></span> <span data-ttu-id="bc74e-121">當接收器中呼叫 [**InkDraw**](inkdraw-method.md) 時，它只會將呼叫傳遞至 **CGuiPaper：： InkDraw**。</span><span class="sxs-lookup"><span data-stu-id="bc74e-121">When [**InkDraw**](inkdraw-method.md) is called in the sink, it simply passes the call on to **CGuiPaper::InkDraw**.</span></span> <span data-ttu-id="bc74e-122">在接收中呼叫 [**InkStop**](cguipaper-methods.md) 時，會呼叫 CGuiPaper 來開啟筆墨的儲存。</span><span class="sxs-lookup"><span data-stu-id="bc74e-122">When [**InkStop**](cguipaper-methods.md) is called in the sink, CGuiPaper is called to turn ink saving back on.</span></span> <span data-ttu-id="bc74e-123">結果會將 COPaper 的筆墨資料播放 CGuiPaper 為僅供顯示之用。</span><span class="sxs-lookup"><span data-stu-id="bc74e-123">The result is a playback of COPaper's ink data to CGuiPaper for display only.</span></span>

<span data-ttu-id="bc74e-124">您可以選擇 [接收器] 功能表上的 [中斷連線] 選項，在 **IPaperSink** 中斷連接時測試 **StoClien** 的行為。</span><span class="sxs-lookup"><span data-stu-id="bc74e-124">You can test the behavior of **StoClien** when its **IPaperSink** is disconnected by choosing the Disconnect choice on the Sink menu.</span></span> <span data-ttu-id="bc74e-125">在中斷連接接收器之後，請從 [說明] 功能表選擇 [關於]，做為實驗。</span><span class="sxs-lookup"><span data-stu-id="bc74e-125">As an experiment, after disconnecting the sink, choose About from the Help menu.</span></span> <span data-ttu-id="bc74e-126">這將會顯示 [About （關於）] 對話方塊，其中涵蓋 **StoClien** 的繪圖部分。</span><span class="sxs-lookup"><span data-stu-id="bc74e-126">This will show the About dialog box, which will cover part of the **StoClien**'s drawing.</span></span> <span data-ttu-id="bc74e-127">按一下 [關於] 對話方塊中的 [確定]。</span><span class="sxs-lookup"><span data-stu-id="bc74e-127">Click OK in the About dialog box.</span></span> <span data-ttu-id="bc74e-128">請注意，所涵蓋的繪圖部分現在已消失。</span><span class="sxs-lookup"><span data-stu-id="bc74e-128">Notice that the portion of the drawing that was covered is now gone.</span></span> <span data-ttu-id="bc74e-129">繪圖資料不會遺失，但影像的一部分是。</span><span class="sxs-lookup"><span data-stu-id="bc74e-129">The drawing data is not lost, but part of the image is.</span></span> <span data-ttu-id="bc74e-130">用戶端收到了 WM \_ 油漆訊息併發出 [**IPaper：：重繪**](ipaper--redraw.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="bc74e-130">The client received the WM\_PAINT message and issued the [**IPaper::Redraw**](ipaper--redraw.md) method.</span></span> <span data-ttu-id="bc74e-131">但因為接收器未連接，所以它不會收到重新繪製繪圖的 **IPaperSink** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="bc74e-131">But because the sink was not connected, it did not receive the **IPaperSink** calls to repaint the drawing.</span></span>

<span data-ttu-id="bc74e-132">您也可以藉由將 **StoClien** 降到最低，然後加以還原，來測試此行為。</span><span class="sxs-lookup"><span data-stu-id="bc74e-132">You can also test this behavior by minimizing **StoClien** and then restoring it.</span></span> <span data-ttu-id="bc74e-133">在此情況下，整個繪圖影像會遺失，且需要重新繪製。</span><span class="sxs-lookup"><span data-stu-id="bc74e-133">In this case, the entire drawing image is lost and needs repainting.</span></span> <span data-ttu-id="bc74e-134">若要在其中一個測試之後重新繪製繪圖影像，請使用 [接收] 功能表重新連接，然後從 [繪製] 功能表 [**中選擇 [重新繪製]**](ipaper--redraw.md) 。</span><span class="sxs-lookup"><span data-stu-id="bc74e-134">To repaint the drawing image after either of these tests, use the Sink menu to reconnect, and then choose [**Redraw**](ipaper--redraw.md) from the Draw menu.</span></span>

 

 




