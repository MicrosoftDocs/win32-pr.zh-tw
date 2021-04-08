---
title: 控制流程
description: 控制流程
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- 視覺效果，程式流程
- 自訂視覺效果，程式流程
- 視覺效果，控制流程
- 自訂視覺效果，控制流程
- 視覺效果，計時事件
- 自訂視覺效果，計時事件
- 視覺效果，轉譯函數
- 自訂視覺效果，轉譯函數
- 視覺效果，RenderWindow 函式
- 自訂視覺效果，RenderWindow 函式
- 轉譯函式，視覺效果程式流程
- RenderWindow 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca09760d958da045c4bbf60ae122a9d0ae4c71c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931974"
---
# <a name="flow-of-control"></a><span data-ttu-id="d997e-115">控制流程</span><span class="sxs-lookup"><span data-stu-id="d997e-115">Flow of Control</span></span>

<span data-ttu-id="d997e-116">音訊資料會透過檔案或資料流程持續進入 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="d997e-116">Audio data comes into Windows Media Player continuously through a file or a stream.</span></span> <span data-ttu-id="d997e-117">這項資料會傳遞至您的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="d997e-117">That data is passed to your visualization.</span></span> <span data-ttu-id="d997e-118">您可以在定義的介面上繪製，並將該介面傳回 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="d997e-118">You draw on a defined surface and pass that surface back to Windows Media Player.</span></span> <span data-ttu-id="d997e-119">此交換會在一秒內發生數次，而且對使用者而言，結果會是可即時移至音樂的滿意動畫。</span><span class="sxs-lookup"><span data-stu-id="d997e-119">This interchange happens several times a second, and to the user, the result is a pleasing animation that moves in time to the music.</span></span>

<span data-ttu-id="d997e-120">以下是視覺效果程式流程的特定順序：</span><span class="sxs-lookup"><span data-stu-id="d997e-120">Here is the specific sequence of the visualization program flow:</span></span>

1.  <span data-ttu-id="d997e-121">在時間間隔內，Windows Media Player 會取得現正播放之音訊的快照。</span><span class="sxs-lookup"><span data-stu-id="d997e-121">At a timed interval, Windows Media Player takes a snapshot of the audio that is playing.</span></span>
2.  <span data-ttu-id="d997e-122">Windows Media Player 透過轉譯函數和 **RenderWindowed** 函式，將該快照集的資料提供給 **您的視覺** 效果。</span><span class="sxs-lookup"><span data-stu-id="d997e-122">Windows Media Player supplies the data from that snapshot to your visualization through the **Render** function and the **RenderWindowed** function.</span></span>
3.  <span data-ttu-id="d997e-123">您必須撰寫將在呼叫 **轉譯和** **RenderWindowed** 時執行的程式碼。</span><span class="sxs-lookup"><span data-stu-id="d997e-123">You must write code that will run when **Render** and **RenderWindowed** is called.</span></span> <span data-ttu-id="d997e-124">當轉譯無視窗時，您的程式碼會使用 Windows Media Player 所定義的裝置內容，或使用您在呈現視窗時所建立的視窗來繪製。</span><span class="sxs-lookup"><span data-stu-id="d997e-124">Your code draws by using a device context defined by Windows Media Player when rendering windowless, or by using a window that you create when rendering windowed.</span></span>
4.  <span data-ttu-id="d997e-125">在目前面板指定的區域中，Windows Media Player 會顯示程式碼所繪製的內容。</span><span class="sxs-lookup"><span data-stu-id="d997e-125">In a region specified by the current skin, Windows Media Player displays what your code drew.</span></span>
5.  <span data-ttu-id="d997e-126">此程式會一秒重複幾次，以建立會對音樂計時的圖形動畫。</span><span class="sxs-lookup"><span data-stu-id="d997e-126">This process repeats several times a second, creating graphical animations that are timed to the music.</span></span> <span data-ttu-id="d997e-127">當音樂停止播放時，視覺效果就會停止。</span><span class="sxs-lookup"><span data-stu-id="d997e-127">When the music stops playing, the visualization stops.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d997e-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="d997e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d997e-129">**開發人員總覽**</span><span class="sxs-lookup"><span data-stu-id="d997e-129">**Developer Overview**</span></span>](developer-overview.md)
</dt> </dl>

 

 




