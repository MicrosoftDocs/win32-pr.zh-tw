---
title: 隱藏 Windows Media Player 控制項
description: 隱藏 Windows Media Player 控制項
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player ActiveX 控制項、網頁
- Windows Media Player 的行動 ActiveX 控制項、網頁
- ActiveX 控制項，網頁
- 內嵌、網頁
- Windows Media Player，隱藏 ActiveX 控制項
- Windows Media Player 物件模型，隱藏 ActiveX 控制項
- 物件模型，隱藏 ActiveX 控制項
- Windows Media Player Mobile，hidingActiveX 控制項
- Windows Media Player ActiveX 控制項，隱藏
- Windows Media Player 的行動 ActiveX 控制項，隱藏
- ActiveX 控制項，隱藏
- Windows Media Player ActiveX 控制項、網頁
- Windows Media Player 的行動 ActiveX 控制項、網頁
- ActiveX 控制項，網頁
- 網頁內嵌，隱藏 ActiveX 控制項
- 隱藏 Windows Media Player ActiveX 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1add2b8f09829ad165f152c26c184d68ac183
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301607"
---
# <a name="hiding-the-windows-media-player-control"></a><span data-ttu-id="db351-126">隱藏 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="db351-126">Hiding the Windows Media Player Control</span></span>

<span data-ttu-id="db351-127">Windows Media Player 的 ActiveX 物件會使用 OBJECT 元素內嵌到網頁中。</span><span class="sxs-lookup"><span data-stu-id="db351-127">The Windows Media Player ActiveX object is embedded in a webpage using the OBJECT element.</span></span> <span data-ttu-id="db351-128">不同于較早的版本，定義 Windows Media Player 的物件專案必須放在網頁的 [內文] 區段中， <BODY> 以及和 </BODY> 標記之間。</span><span class="sxs-lookup"><span data-stu-id="db351-128">Unlike earlier versions, the OBJECT element that defines Windows Media Player must be placed in the BODY section of a webpage, between the <BODY> and </BODY> tags.</span></span> <span data-ttu-id="db351-129">將 Windows Media Player 的 ActiveX 物件放在網頁的標頭區段中，以隱藏使用者介面可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="db351-129">Placing the Windows Media Player ActiveX object in the HEAD section of a webpage to hide the user interface can produce unexpected results.</span></span>

<span data-ttu-id="db351-130">如果您將 Windows Media Player ActiveX 控制項放在網頁的 [主體] 區段中，將會顯示控制項使用者介面。</span><span class="sxs-lookup"><span data-stu-id="db351-130">If you put the Windows Media Player ActiveX control in the BODY section of a webpage, the control user interface will be displayed.</span></span> <span data-ttu-id="db351-131">如果您不想要顯示它，而且想要建立自己的使用者介面，請將物件元素的高度和寬度屬性設定為零。</span><span class="sxs-lookup"><span data-stu-id="db351-131">If you do not want it to be displayed, and wish to create your own user interface, set the height and width attributes of the OBJECT element to zero.</span></span>

<span data-ttu-id="db351-132">藉由設定 *播放* 程式，也可以隱藏控制項。**uiMode** 屬性設為「隱藏」。</span><span class="sxs-lookup"><span data-stu-id="db351-132">The control can also be made invisible by setting the *Player*.**uiMode** property to "invisible".</span></span> <span data-ttu-id="db351-133">您可以使用下一節所討論的 PARAM 標記來完成這項操作。</span><span class="sxs-lookup"><span data-stu-id="db351-133">This can be done using a PARAM tag as discussed in the next section.</span></span> <span data-ttu-id="db351-134">在此情況下，會使用高度和寬度為控制項保留空間，但在 **uiMode** 變更為「不可見」的專案之前，不會在保留空間中顯示任何內容。</span><span class="sxs-lookup"><span data-stu-id="db351-134">In this case, space is reserved for the control using height and width, but nothing is displayed in the reserved space until **uiMode** is changed to something other than "invisible".</span></span>

## <a name="related-topics"></a><span data-ttu-id="db351-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="db351-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db351-136">**在 Web 網頁中使用 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="db351-136">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




