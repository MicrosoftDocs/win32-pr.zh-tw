---
title: 符合 Windows Media Player 色彩
description: 符合 Windows Media Player 色彩
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player 線上商店，符合 Windows Media Player 色彩
- 線上商店，符合 Windows Media Player 色彩
- 輸入1個線上商店，符合 Windows Media Player 色彩
- 輸入2個線上商店，符合 Windows Media Player 色彩
- Windows Media Player 線上商店，Windows Media Player 色彩比對
- 線上商店、Windows Media Player 色彩比對
- 輸入1個線上商店，Windows Media Player 色彩比對
- 輸入2個線上商店，Windows Media Player 色彩比對
- Windows Media Player 線上商店、Windows Media Player 的色彩比對
- 線上商店、Windows Media Player 的色彩對應
- 輸入1個線上商店、Windows Media Player 的色彩對應
- 輸入2個線上商店、Windows Media Player 的色彩對應
- Windows Media Player 的色彩比對
- 符合 Windows Media Player 色彩
- Windows Media Player，相符的色彩
- Windows Media Player，色彩比對
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965996"
---
# <a name="matching-the-windows-media-player-colors"></a><span data-ttu-id="855e8-119">符合 Windows Media Player 色彩</span><span class="sxs-lookup"><span data-stu-id="855e8-119">Matching the Windows Media Player Colors</span></span>

<span data-ttu-id="855e8-120">讓您的線上商店網頁符合 Windows Media Player 色彩配置很簡單。</span><span class="sxs-lookup"><span data-stu-id="855e8-120">Making your online store webpage match the Windows Media Player color scheme is easy.</span></span> <span data-ttu-id="855e8-121">只要處理 **OnColorChange** 事件即可。</span><span class="sxs-lookup"><span data-stu-id="855e8-121">Simply handle the **External.OnColorChange** event.</span></span> <span data-ttu-id="855e8-122">若要指定函式來處理事件，請在您的網頁載入時使用如下的程式碼：</span><span class="sxs-lookup"><span data-stu-id="855e8-122">To specify a function to handle the event, use code like the following when your webpage loads:</span></span>


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



<span data-ttu-id="855e8-123">每次使用者變更 Windows Media Player 的色彩配置時，播放程式就會呼叫您的函式。</span><span class="sxs-lookup"><span data-stu-id="855e8-123">Each time the user changes the color scheme of Windows Media Player, the Player will call your function.</span></span> <span data-ttu-id="855e8-124">下列範例顯示一個簡單的函式，它會將網頁背景設定為符合 **appColorLight** 屬性：</span><span class="sxs-lookup"><span data-stu-id="855e8-124">The following example shows a simple function that sets the webpage background to match the **External.appColorLight** property:</span></span>


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



<span data-ttu-id="855e8-125">您也可以使用其他的色彩屬性。</span><span class="sxs-lookup"><span data-stu-id="855e8-125">There are other color properties available for your use as well.</span></span> <span data-ttu-id="855e8-126">請參閱 [類型2線上商店的外部物件](external-object-for-type-2-online-stores.md)。</span><span class="sxs-lookup"><span data-stu-id="855e8-126">See [External Object for Type 2 Online Stores](external-object-for-type-2-online-stores.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="855e8-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="855e8-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="855e8-128">**AppColorLight**</span><span class="sxs-lookup"><span data-stu-id="855e8-128">**External.appColorLight**</span></span>](external-appcolorlight.md)
</dt> <dt>

[<span data-ttu-id="855e8-129">**OnColorChange 事件**</span><span class="sxs-lookup"><span data-stu-id="855e8-129">**External.OnColorChange Event**</span></span>](external-oncolorchange-event.md)
</dt> <dt>

[<span data-ttu-id="855e8-130">**Type 1 和 Type 2 線上商店的一般資訊**</span><span class="sxs-lookup"><span data-stu-id="855e8-130">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




