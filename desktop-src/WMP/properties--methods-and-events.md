---
title: 屬性、方法和事件
description: 屬性、方法和事件
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Windows Media Player，物件模型的屬性
- Windows Media Player，物件模型的方法
- Windows Media Player，物件模型的事件
- Windows Media Player 物件模型，屬性
- Windows Media Player 物件模型，方法
- Windows Media Player 物件模型，事件
- 物件模型，屬性
- 物件模型，方法
- 物件模型，事件
- Windows Media Player ActiveX 控制項，物件模型的屬性
- ActiveX 控制項，物件模型的屬性
- Windows Media Player 的行動 ActiveX 控制項、物件模型的屬性
- Windows Media Player 行動裝置，物件模型的屬性
- Windows Media Player ActiveX 控制項，物件模型的方法
- ActiveX 控制項，物件模型的方法
- Windows Media Player 的行動 ActiveX 控制項、物件模型的方法
- Windows Media Player 行動裝置，物件模型的方法
- Windows Media Player 的 ActiveX 控制項、物件模型的事件
- ActiveX 控制項，物件模型的事件
- Windows Media Player 的行動 ActiveX 控制項、物件模型的事件
- Windows Media Player 行動裝置，物件模型的事件
- 屬性，Windows Media Player 物件模型
- 方法，Windows Media Player 物件模型
- 事件，Windows Media Player 物件模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e06a860d04bfc1a5ccd5b33c0604a0ef818a0127
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092277"
---
# <a name="properties-methods-and-events"></a><span data-ttu-id="aa2ec-127">屬性、方法和事件</span><span class="sxs-lookup"><span data-stu-id="aa2ec-127">Properties, Methods and Events</span></span>

<span data-ttu-id="aa2ec-128">每個物件都有方法和屬性，您可以透過這些方法和屬性來程式設計 Windows Media Player 控制項。</span><span class="sxs-lookup"><span data-stu-id="aa2ec-128">Each object has methods and properties through which you can program the Windows Media Player control.</span></span> <span data-ttu-id="aa2ec-129">方法是物件可以採取的動作。</span><span class="sxs-lookup"><span data-stu-id="aa2ec-129">A method is an action that the object can take.</span></span> <span data-ttu-id="aa2ec-130">屬性是您可以讀取或變更的資料值。</span><span class="sxs-lookup"><span data-stu-id="aa2ec-130">A property is a data value that you can read or change.</span></span> <span data-ttu-id="aa2ec-131">例如， **Play** 方法會開始播放內容，而 [畫面格數 **] 屬性會** 指出目前播放內容的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="aa2ec-131">For example, the **Play** method starts the content playing, and the **frameRate** property indicates the current frame rate of the content that is playing.</span></span>

<span data-ttu-id="aa2ec-132">此外， **Player** 物件會引發事件，讓您有機會在特定時間執行動作。</span><span class="sxs-lookup"><span data-stu-id="aa2ec-132">In addition, the **Player** object raises events that give you the opportunity to carry out actions at specific times.</span></span> <span data-ttu-id="aa2ec-133">您會在事件處理常式中撰寫程式碼，當 Windows Media Player 引發對應的事件時會執行此程式碼。</span><span class="sxs-lookup"><span data-stu-id="aa2ec-133">You write code in an event handler that will execute when Windows Media Player raises the corresponding event.</span></span> <span data-ttu-id="aa2ec-134">例如，您可以在 **PlayStateChange** 事件處理常式中撰寫程式碼，以判斷狀態變更是否為媒體結束，如果是，則會顯示對話方塊，詢問使用者是否想要再次播放媒體。</span><span class="sxs-lookup"><span data-stu-id="aa2ec-134">For example, you can write code in a **PlayStateChange** event handler that determines whether the change in state is that the media ended and if so display a dialog box asking users if they want to play the media again.</span></span>

> [!Note]  
> <span data-ttu-id="aa2ec-135">Windows Media Player 物件模型中的所有方法都是非同步。</span><span class="sxs-lookup"><span data-stu-id="aa2ec-135">All of the methods in the Windows Media Player object model are asynchronous.</span></span> <span data-ttu-id="aa2ec-136">如果您在相同的程式中呼叫兩個方法，則第二個方法無法依賴已完成其動作的第一個方法。</span><span class="sxs-lookup"><span data-stu-id="aa2ec-136">If you call two methods in the same procedure, the second method cannot rely on the first method having completed its action.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="aa2ec-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa2ec-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa2ec-138">**關於 Player 物件模型**</span><span class="sxs-lookup"><span data-stu-id="aa2ec-138">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




