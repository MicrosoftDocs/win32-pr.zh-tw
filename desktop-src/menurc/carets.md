---
title: 游標
description: 本節討論視窗工作區中的閃爍線、區塊或點陣圖游標。
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- 資源，游標
- 游標，關於
- 閃爍線
- 閃爍的區塊
- 閃爍的點陣圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb99dfc324aa039924fa26683ab0a7674706ea
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104386308"
---
# <a name="carets"></a><span data-ttu-id="4aff6-108">游標</span><span class="sxs-lookup"><span data-stu-id="4aff6-108">Carets</span></span>

<span data-ttu-id="4aff6-109">*插入* 點是視窗工作區中的閃爍線、區塊或點陣圖。</span><span class="sxs-lookup"><span data-stu-id="4aff6-109">A *caret* is a blinking line, block, or bitmap in the client area of a window.</span></span> <span data-ttu-id="4aff6-110">插入號通常表示將插入文字或圖形的位置。</span><span class="sxs-lookup"><span data-stu-id="4aff6-110">The caret typically indicates the place at which text or graphics will be inserted.</span></span>

<span data-ttu-id="4aff6-111">下圖顯示插入點外觀的一些常見變化。</span><span class="sxs-lookup"><span data-stu-id="4aff6-111">The following illustration shows some common variations in the appearance of the caret.</span></span>

![顯示五種不同的插入號可以出現方式。](images/cscrt-01.png)

<span data-ttu-id="4aff6-113">應用程式可以建立插入號、變更其閃爍時間，以及顯示、隱藏或重新放置插入號。</span><span class="sxs-lookup"><span data-stu-id="4aff6-113">Applications can create a caret, change its blink time, and display, hide, or relocate the caret.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="4aff6-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="4aff6-114">In This Section</span></span>



| <span data-ttu-id="4aff6-115">Name</span><span class="sxs-lookup"><span data-stu-id="4aff6-115">Name</span></span>                                   | <span data-ttu-id="4aff6-116">描述</span><span class="sxs-lookup"><span data-stu-id="4aff6-116">Description</span></span>                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="4aff6-117">關於游標</span><span class="sxs-lookup"><span data-stu-id="4aff6-117">About Carets</span></span>](about-carets.md)       | <span data-ttu-id="4aff6-118">討論游標。</span><span class="sxs-lookup"><span data-stu-id="4aff6-118">Discusses carets.</span></span><br/>                                              |
| [<span data-ttu-id="4aff6-119">使用游標</span><span class="sxs-lookup"><span data-stu-id="4aff6-119">Using Carets</span></span>](using-carets.md)       | <span data-ttu-id="4aff6-120">示範如何執行與游標相關之工作的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="4aff6-120">Code samples that show how to perform tasks related to carets.</span></span><br/> |
| [<span data-ttu-id="4aff6-121">插入號參考</span><span class="sxs-lookup"><span data-stu-id="4aff6-121">Caret Reference</span></span>](caret-reference.md) | <span data-ttu-id="4aff6-122">包含 API 參考。</span><span class="sxs-lookup"><span data-stu-id="4aff6-122">Contains the API reference.</span></span><br/>                                    |



 

### <a name="caret-functions"></a><span data-ttu-id="4aff6-123">插入號函式</span><span class="sxs-lookup"><span data-stu-id="4aff6-123">Caret Functions</span></span>



| <span data-ttu-id="4aff6-124">Name</span><span class="sxs-lookup"><span data-stu-id="4aff6-124">Name</span></span>                                           | <span data-ttu-id="4aff6-125">描述</span><span class="sxs-lookup"><span data-stu-id="4aff6-125">Description</span></span>                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4aff6-126">**CreateCaret**</span><span class="sxs-lookup"><span data-stu-id="4aff6-126">**CreateCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | <span data-ttu-id="4aff6-127">建立系統插入號的新圖形，並將插入號的擁有權指派給指定的視窗。</span><span class="sxs-lookup"><span data-stu-id="4aff6-127">Creates a new shape for the system caret and assigns ownership of the caret to the specified window.</span></span> <span data-ttu-id="4aff6-128">插入號圖形可以是線條、區塊或點陣圖。</span><span class="sxs-lookup"><span data-stu-id="4aff6-128">The caret shape can be a line, a block, or a bitmap.</span></span> <br/>                                                                                         |
| [<span data-ttu-id="4aff6-129">**DestroyCaret**</span><span class="sxs-lookup"><span data-stu-id="4aff6-129">**DestroyCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | <span data-ttu-id="4aff6-130">終結插入號的目前圖形，從視窗釋出插入號，然後從畫面中移除插入號。</span><span class="sxs-lookup"><span data-stu-id="4aff6-130">Destroys the caret's current shape, frees the caret from the window, and removes the caret from the screen.</span></span> <br/>                                                                                                                                       |
| [<span data-ttu-id="4aff6-131">**GetCaretBlinkTime**</span><span class="sxs-lookup"><span data-stu-id="4aff6-131">**GetCaretBlinkTime**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | <span data-ttu-id="4aff6-132">抓取將插入號的圖元進行反轉所需的時間。</span><span class="sxs-lookup"><span data-stu-id="4aff6-132">Retrieves the time required to invert the caret's pixels.</span></span> <span data-ttu-id="4aff6-133">使用者可以設定此值。</span><span class="sxs-lookup"><span data-stu-id="4aff6-133">The user can set this value.</span></span> <br/>                                                                                                                                                            |
| [<span data-ttu-id="4aff6-134">**GetCaretPos**</span><span class="sxs-lookup"><span data-stu-id="4aff6-134">**GetCaretPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | <span data-ttu-id="4aff6-135">將插入號的位置複製到指定的 [**點**](/previous-versions//dd162805(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="4aff6-135">Copies the caret's position to the specified [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <br/>                                                                                                                                                                    |
| [<span data-ttu-id="4aff6-136">**HideCaret**</span><span class="sxs-lookup"><span data-stu-id="4aff6-136">**HideCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | <span data-ttu-id="4aff6-137">從畫面移除插入號。</span><span class="sxs-lookup"><span data-stu-id="4aff6-137">Removes the caret from the screen.</span></span> <span data-ttu-id="4aff6-138">隱藏插入號不會終結其目前的形狀或使插入點失效。</span><span class="sxs-lookup"><span data-stu-id="4aff6-138">Hiding a caret does not destroy its current shape or invalidate the insertion point.</span></span> <br/>                                                                                                                           |
| [<span data-ttu-id="4aff6-139">**SetCaretBlinkTime**</span><span class="sxs-lookup"><span data-stu-id="4aff6-139">**SetCaretBlinkTime**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | <span data-ttu-id="4aff6-140">將插入號閃爍時間設定為指定的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="4aff6-140">Sets the caret blink time to the specified number of milliseconds.</span></span> <span data-ttu-id="4aff6-141">閃爍時間是反轉插入號圖元所需的經過時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="4aff6-141">The blink time is the elapsed time, in milliseconds, required to invert the caret's pixels.</span></span> <br/>                                                                                    |
| [<span data-ttu-id="4aff6-142">**SetCaretPos**</span><span class="sxs-lookup"><span data-stu-id="4aff6-142">**SetCaretPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | <span data-ttu-id="4aff6-143">將插入點移至指定的座標。</span><span class="sxs-lookup"><span data-stu-id="4aff6-143">Moves the caret to the specified coordinates.</span></span> <span data-ttu-id="4aff6-144">如果擁有插入號的視窗是使用 **CS \_ OWNDC** 類別樣式所建立，則指定的座標會受限於與該視窗相關聯之裝置內容的對應模式。</span><span class="sxs-lookup"><span data-stu-id="4aff6-144">If the window that owns the caret was created with the **CS\_OWNDC** class style, then the specified coordinates are subject to the mapping mode of the device context associated with that window.</span></span> <br/> |
| [<span data-ttu-id="4aff6-145">**ShowCaret**</span><span class="sxs-lookup"><span data-stu-id="4aff6-145">**ShowCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | <span data-ttu-id="4aff6-146">讓插入號顯示在畫面上插入號的目前位置。</span><span class="sxs-lookup"><span data-stu-id="4aff6-146">Makes the caret visible on the screen at the caret's current position.</span></span> <span data-ttu-id="4aff6-147">當插入號變成可見時，它會自動開始閃爍。</span><span class="sxs-lookup"><span data-stu-id="4aff6-147">When the caret becomes visible, it begins flashing automatically.</span></span> <br/>                                                                                                          |



 

 

