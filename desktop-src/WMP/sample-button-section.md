---
title: 範例按鈕區段
description: 範例按鈕區段
ms.assetid: 52358f83-8c74-4957-87c4-ca1ed7f667fc
keywords:
- Windows Media Player 行動外觀、按鈕區段
- 外觀、按鈕區段
- 外觀、按鈕區段的參考
- 面板中的按鈕，按鈕區段
- 外觀定義檔，按鈕區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c35a4efd0e52dd7f5fd0cf87fc269eb4a9f4c27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021691"
---
# <a name="sample-button-section"></a><span data-ttu-id="a058f-108">範例按鈕區段</span><span class="sxs-lookup"><span data-stu-id="a058f-108">Sample Button Section</span></span>

<span data-ttu-id="a058f-109">下列各行顯示面板定義檔案的一般按鈕區段：</span><span class="sxs-lookup"><span data-stu-id="a058f-109">The following lines show a typical Buttons section of a skin definition file:</span></span>


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98
    Info       PushHit    97,49,43,43    Pushed @ 57,0     Disabled @ 57,0      0,  0,  0
    Stop       PushHit    97,173,43,43   Pushed @ 57,124   Disabled @ 57,124  255,255,  0
    Prev       PushHit    40,83,43,43    Pushed @ 0,34     Disabled @ 0,34      0,  0,255
    Next       PushHit    153,83,43,43   Pushed @ 113,34   Disabled @ 113,34  255,  0,  0
    Shuffle    ToggleHit  40,136,43,43   Pushed @ 0,87     Disabled @ 0,87      0,255,  0
    Repeat     ToggleHit  153,136,43,43  Pushed @ 113,87   Disabled @ 113,87  255,  0,255
    Mute       Toggle     5,220,24,23    Super @ 247,29    Super @ 4,28         0,  0,  0

```



<span data-ttu-id="a058f-110">這段程式碼定義了八個按鈕，可用來提供面板中的下列所有功能：</span><span class="sxs-lookup"><span data-stu-id="a058f-110">This code defines eight buttons that are used to provide all of the following functions in a skin:</span></span>

-   <span data-ttu-id="a058f-111">播放、暫停和停止媒體專案。</span><span class="sxs-lookup"><span data-stu-id="a058f-111">Play, pause, and stop media items.</span></span>
-   <span data-ttu-id="a058f-112">隨機播放、重複和移動播放清單。</span><span class="sxs-lookup"><span data-stu-id="a058f-112">Shuffle, repeat, and move through the playlist.</span></span>
-   <span data-ttu-id="a058f-113">將音量靜音。</span><span class="sxs-lookup"><span data-stu-id="a058f-113">Mute the volume.</span></span>

<span data-ttu-id="a058f-114">除了 [靜音] 按鈕以外的所有按鈕都是 [區域] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="a058f-114">All the buttons except the mute button are region buttons.</span></span> <span data-ttu-id="a058f-115">為了方便起見，[靜音] 按鈕會從超級點陣圖取得其已推送和已停用的影像。</span><span class="sxs-lookup"><span data-stu-id="a058f-115">The mute button gets its Pushed and Disabled images from the Super bitmap for convenience.</span></span>

> [!Note]  
> <span data-ttu-id="a058f-116">在 Windows Media Player 10 行動裝置版或更新版本的面板中，按鈕類型已被取代。</span><span class="sxs-lookup"><span data-stu-id="a058f-116">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span> <span data-ttu-id="a058f-117">請為每個類型輸入 "NA"，而不是在您的面板檔案中宣告的按鈕類型。</span><span class="sxs-lookup"><span data-stu-id="a058f-117">Instead of a button type declared in your skin file, enter "NA" for each type.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a058f-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="a058f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a058f-119">**按鈕**</span><span class="sxs-lookup"><span data-stu-id="a058f-119">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




