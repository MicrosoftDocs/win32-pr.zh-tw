---
title: IPaper 方法
description: 提供主要由其原生 IPaper 介面控制的 COPaper 物件。
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- IPaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84153c9fcec021d9084807d73d46198e3a56482
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184047"
---
# <a name="ipaper-methods"></a><span data-ttu-id="82380-104">IPaper 方法</span><span class="sxs-lookup"><span data-stu-id="82380-104">IPaper Methods</span></span>

<span data-ttu-id="82380-105">**StoServe** 會提供主要由其原生 **IPaper** 介面控制的 COPaper 物件。</span><span class="sxs-lookup"><span data-stu-id="82380-105">**StoServe** provides COPaper objects that are controlled primarily by their native **IPaper** interface.</span></span>

<span data-ttu-id="82380-106">下表列出來自 IPAPER 的 **IPaper** 方法。在 [中] \\ inc. 目錄中的 H。</span><span class="sxs-lookup"><span data-stu-id="82380-106">The following table lists **IPaper** methods from IPAPER.H in the sibling \\INC directory.</span></span>



| <span data-ttu-id="82380-107">方法</span><span class="sxs-lookup"><span data-stu-id="82380-107">Method</span></span>    | <span data-ttu-id="82380-108">描述</span><span class="sxs-lookup"><span data-stu-id="82380-108">Description</span></span>                                                         |
|-----------|---------------------------------------------------------------------|
| <span data-ttu-id="82380-109">InitPaper</span><span class="sxs-lookup"><span data-stu-id="82380-109">InitPaper</span></span> | <span data-ttu-id="82380-110">初始化紙張物件並建立筆墨資料陣列。</span><span class="sxs-lookup"><span data-stu-id="82380-110">Initializes paper object and create ink data array.</span></span>                 |
| <span data-ttu-id="82380-111">鎖定</span><span class="sxs-lookup"><span data-stu-id="82380-111">Lock</span></span>      | <span data-ttu-id="82380-112">提供紙張的用戶端控制權，並鎖定其他用戶端。</span><span class="sxs-lookup"><span data-stu-id="82380-112">Gives client control of the paper and locks out other clients.</span></span>      |
| <span data-ttu-id="82380-113">Unlock</span><span class="sxs-lookup"><span data-stu-id="82380-113">Unlock</span></span>    | <span data-ttu-id="82380-114">紙張的會讓出用戶端控制。</span><span class="sxs-lookup"><span data-stu-id="82380-114">Relinquishes client control of the paper.</span></span>                           |
| <span data-ttu-id="82380-115">載入</span><span class="sxs-lookup"><span data-stu-id="82380-115">Load</span></span>      | <span data-ttu-id="82380-116">從用戶端的複合檔案載入紙張內容，並通知接收。</span><span class="sxs-lookup"><span data-stu-id="82380-116">Loads paper content from client's compound file and notifies sinks.</span></span> |
| <span data-ttu-id="82380-117">儲存</span><span class="sxs-lookup"><span data-stu-id="82380-117">Save</span></span>      | <span data-ttu-id="82380-118">將紙張內容儲存至用戶端的複合檔案。</span><span class="sxs-lookup"><span data-stu-id="82380-118">Saves paper content to client's compound file.</span></span>                      |
| <span data-ttu-id="82380-119">InkStart</span><span class="sxs-lookup"><span data-stu-id="82380-119">InkStart</span></span>  | <span data-ttu-id="82380-120">開始色彩筆墨繪圖至紙張表面。</span><span class="sxs-lookup"><span data-stu-id="82380-120">Starts color ink drawing to the paper surface.</span></span>                      |
| <span data-ttu-id="82380-121">InkDraw</span><span class="sxs-lookup"><span data-stu-id="82380-121">InkDraw</span></span>   | <span data-ttu-id="82380-122">將筆墨資料點放在電子紙張表面上。</span><span class="sxs-lookup"><span data-stu-id="82380-122">Puts ink data points on the electronic paper surface.</span></span>               |
| <span data-ttu-id="82380-123">InkStop</span><span class="sxs-lookup"><span data-stu-id="82380-123">InkStop</span></span>   | <span data-ttu-id="82380-124">停止筆墨繪圖至紙張表面。</span><span class="sxs-lookup"><span data-stu-id="82380-124">Stops ink drawing to the paper surface.</span></span>                             |
| <span data-ttu-id="82380-125">清除</span><span class="sxs-lookup"><span data-stu-id="82380-125">Erase</span></span>     | <span data-ttu-id="82380-126">清除目前的紙張內容，並通知接收。</span><span class="sxs-lookup"><span data-stu-id="82380-126">Erase the current paper content and notifies sinks.</span></span>                 |
| <span data-ttu-id="82380-127">調整大小</span><span class="sxs-lookup"><span data-stu-id="82380-127">Resize</span></span>    | <span data-ttu-id="82380-128">調整繪圖紙張的矩形大小，並通知接收。</span><span class="sxs-lookup"><span data-stu-id="82380-128">Resizes the drawing paper rectangle size and notifies sinks.</span></span>        |
| <span data-ttu-id="82380-129">重 繪</span><span class="sxs-lookup"><span data-stu-id="82380-129">Redraw</span></span>    | <span data-ttu-id="82380-130">重新繪製紙張物件的內容，並通知接收。</span><span class="sxs-lookup"><span data-stu-id="82380-130">Redraws contents of paper object and notifies sinks.</span></span>                |



 

<span data-ttu-id="82380-131">這個程式碼範例在複合檔案上的相關方法是 [**載入**](ipaper--load.md)、 [**儲存**](ipaper--save.md)和 [**重繪**](ipaper--redraw.md)。</span><span class="sxs-lookup"><span data-stu-id="82380-131">Methods of interest for this code sample on compound files are [**Load**](ipaper--load.md), [**Save**](ipaper--save.md), and [**Redraw**](ipaper--redraw.md).</span></span>

<span data-ttu-id="82380-132">[**InkStart**](inkstart-method.md)、 [**InkDraw**](inkdraw-method.md)和 [**InkStop**](cguipaper-methods.md) 是用戶端用來記錄筆墨繪圖順序之命令 COPaper 的方法。</span><span class="sxs-lookup"><span data-stu-id="82380-132">[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) are methods used by clients to command COPaper to record ink drawing sequences.</span></span> <span data-ttu-id="82380-133">用戶端通常會在 \_ COPaper 上呼叫 **InkStart** ，以回應 WM LBUTTONDOWN 訊息作為筆墨繪圖順序的開頭。</span><span class="sxs-lookup"><span data-stu-id="82380-133">The client will typically respond to a WM\_LBUTTONDOWN message as the start of an ink drawing sequence by calling **InkStart** on COPaper.</span></span> <span data-ttu-id="82380-134">當使用者將滑鼠或畫筆移至按住左按鈕時，用戶端將會 \_ 使用對應的 **InkDraw** 呼叫來回應重複的 WM MOUSEMOVE 訊息。</span><span class="sxs-lookup"><span data-stu-id="82380-134">As the user moves the mouse or pen to draw while holding down the left button, the client will respond to repeated WM\_MOUSEMOVE messages with corresponding calls to **InkDraw**.</span></span> <span data-ttu-id="82380-135">當使用者放開滑鼠左鍵時，用戶端會使用 InkStop 的呼叫來回應 WM \_ LBUTTONUP 訊息，此訊息會標示筆墨繪圖順序的結尾。</span><span class="sxs-lookup"><span data-stu-id="82380-135">When the user releases the left mouse button, the client will respond to a WM\_LBUTTONUP message with a call to **InkStop**, which marks the end of the ink drawing sequence.</span></span>

<span data-ttu-id="82380-136">[**InkStart**](inkstart-method.md) 會在用戶端視窗座標中告訴 COPaper 繪圖順序的開始位置。</span><span class="sxs-lookup"><span data-stu-id="82380-136">[**InkStart**](inkstart-method.md) tells COPaper the start position for the drawing sequence in client window coordinates.</span></span> <span data-ttu-id="82380-137">它也會傳遞目前選取的筆墨色彩和寬度。</span><span class="sxs-lookup"><span data-stu-id="82380-137">It also passes the currently selected ink color and width.</span></span> <span data-ttu-id="82380-138">用戶端會維護這些選項;COPaper 只會在進行 **InkStart** 呼叫時記錄它們。</span><span class="sxs-lookup"><span data-stu-id="82380-138">The client maintains these selections; COPaper merely records them when the **InkStart** call is made.</span></span> <span data-ttu-id="82380-139">重複呼叫 [**InkDraw**](inkdraw-method.md) ，以指示 COPaper 連續的視窗座標，代表滑鼠或畫筆的繪製動作。</span><span class="sxs-lookup"><span data-stu-id="82380-139">[**InkDraw**](inkdraw-method.md) is called repeatedly to tell COPaper the succession of window coordinates that represent the drawing motion of the mouse or pen.</span></span> <span data-ttu-id="82380-140">[**InkStop**](cguipaper-methods.md) 會指示 COPaper 標示繪圖順序的結尾。</span><span class="sxs-lookup"><span data-stu-id="82380-140">[**InkStop**](cguipaper-methods.md) instructs COPaper to mark the end of a drawing sequence.</span></span>

 

 




