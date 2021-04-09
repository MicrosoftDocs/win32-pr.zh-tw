---
title: 設計介面
description: 設計介面
ms.assetid: 7b87bab4-8246-461a-a9cd-2d348e7f0d48
keywords:
- Windows Media Player 行動外觀、使用者介面
- 外觀，使用者介面
- 建立外觀，使用者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8070ef6fd4589f762624d7a0b5ee1d380a264066
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092299"
---
# <a name="designing-the-interface"></a><span data-ttu-id="7ada1-106">設計介面</span><span class="sxs-lookup"><span data-stu-id="7ada1-106">Designing the Interface</span></span>

<span data-ttu-id="7ada1-107">一旦選擇了函數之後，就可以設計介面。</span><span class="sxs-lookup"><span data-stu-id="7ada1-107">Once the functions have been chosen, the interface can be designed.</span></span> <span data-ttu-id="7ada1-108">已選擇簡單的介面來符合功能。</span><span class="sxs-lookup"><span data-stu-id="7ada1-108">A simple interface was chosen to match the functionality.</span></span> <span data-ttu-id="7ada1-109">這些控制項的符號是從標準的 VCR 控制項所選擇。</span><span class="sxs-lookup"><span data-stu-id="7ada1-109">Symbols for the controls were chosen from standard VCR controls.</span></span>

<span data-ttu-id="7ada1-110">下圖顯示介面看起來的樣子。</span><span class="sxs-lookup"><span data-stu-id="7ada1-110">The following image shows what the interface will look like.</span></span>

![範例介面](images/ceswmful.png)

-   <span data-ttu-id="7ada1-112">**[PlayPause] 或 [PlayPauseStop] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="7ada1-112">**PlayPause or PlayPauseStop button.**</span></span> <span data-ttu-id="7ada1-113">使用者將最常使用此按鈕，因此您可能會考慮使用較大的按鈕。</span><span class="sxs-lookup"><span data-stu-id="7ada1-113">The user will be tapping this the most, so you might consider a larger button.</span></span> <span data-ttu-id="7ada1-114">右上角可讓使用者快速找到適當的位置。</span><span class="sxs-lookup"><span data-stu-id="7ada1-114">The upper-right corner makes a good location that the user can find quickly.</span></span> <span data-ttu-id="7ada1-115">實心箭號可用來指出播放和兩個垂直線 (此處未顯示) 將用來表示暫停。</span><span class="sxs-lookup"><span data-stu-id="7ada1-115">A solid arrow is used to indicate play and two vertical bars (not shown here) will be used to indicate pause.</span></span>
    > [!Note]  
    > <span data-ttu-id="7ada1-116">只有在建立 Windows Media Player 10 行動裝置版或更新版本的面板時，才能使用 [PlayPauseStop] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="7ada1-116">The PlayPauseStop button can only be used when creating a skin for Windows Media Player 10 Mobile or later.</span></span>

     

-   <span data-ttu-id="7ada1-117">**停止按鈕。**</span><span class="sxs-lookup"><span data-stu-id="7ada1-117">**Stop button.**</span></span> <span data-ttu-id="7ada1-118">為了讓您輕鬆找到，它會放在左上角。</span><span class="sxs-lookup"><span data-stu-id="7ada1-118">To make this easy to find, it is placed at the upper-left corner.</span></span> <span data-ttu-id="7ada1-119">使用正方形表示停止。</span><span class="sxs-lookup"><span data-stu-id="7ada1-119">A square is used to indicate stop.</span></span> <span data-ttu-id="7ada1-120">如果您要建立 Windows Media Player 10 行動裝置版或更新版本的面板，[PlayPauseStop] 按鈕已經提供此功能。</span><span class="sxs-lookup"><span data-stu-id="7ada1-120">If you are creating a skin for Windows Media Player 10 Mobile or later, the PlayPauseStop button already provides this functionality.</span></span>
-   <span data-ttu-id="7ada1-121">**Next 和上一頁按鈕。**</span><span class="sxs-lookup"><span data-stu-id="7ada1-121">**Next and Prev buttons.**</span></span> <span data-ttu-id="7ada1-122">因為它們不會經常使用，所以會放在左側。</span><span class="sxs-lookup"><span data-stu-id="7ada1-122">Since these will not be used as often, they are placed on the left.</span></span> <span data-ttu-id="7ada1-123">下一步是在上一個按鈕的上方，因為人們很可能想要在播放清單中向前移動。</span><span class="sxs-lookup"><span data-stu-id="7ada1-123">The Next is above the Prev button because people will more likely want to move forward in a playlist.</span></span> <span data-ttu-id="7ada1-124">使用雙箭號，因為它們在函式中類似于向前快轉控制項。</span><span class="sxs-lookup"><span data-stu-id="7ada1-124">The double-arrow symbols are used because they are similar in function to a fast-forward control.</span></span>
-   <span data-ttu-id="7ada1-125">**磁片區的跟蹤。**</span><span class="sxs-lookup"><span data-stu-id="7ada1-125">**Volume trackbar.**</span></span> <span data-ttu-id="7ada1-126">這是放在畫面底部，而且是一個簡單的線條，其頂端有一個 thumb 按鈕。</span><span class="sxs-lookup"><span data-stu-id="7ada1-126">This is placed at the bottom of the screen and is a simple line with a thumb button on top of it.</span></span>
-   <span data-ttu-id="7ada1-127">**[字幕] 文字方塊。**</span><span class="sxs-lookup"><span data-stu-id="7ada1-127">**Marquee text box.**</span></span> <span data-ttu-id="7ada1-128">這會放置在 [PlayPause] 或 [PlayPauseStop] 按鈕底下，讓您很容易看到。</span><span class="sxs-lookup"><span data-stu-id="7ada1-128">This is placed under the PlayPause or PlayPauseStop button so that it is easy to see.</span></span>

<span data-ttu-id="7ada1-129">您可能會想要先將其繪製，並試驗每個使用者介面元素的位置。</span><span class="sxs-lookup"><span data-stu-id="7ada1-129">You may want to sketch this first and experiment with the placement of each user interface element.</span></span> <span data-ttu-id="7ada1-130">此處所示的設計是為了簡單且便於使用而選擇的。</span><span class="sxs-lookup"><span data-stu-id="7ada1-130">The design shown here was chosen for simplicity and ease of use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ada1-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="7ada1-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ada1-132">**外觀指南**</span><span class="sxs-lookup"><span data-stu-id="7ada1-132">**Skin Guide**</span></span>](skin-guide.md)
</dt> </dl>

 

 




