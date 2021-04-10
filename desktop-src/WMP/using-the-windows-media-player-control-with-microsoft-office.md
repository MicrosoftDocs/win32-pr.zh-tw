---
title: 使用 Windows Media Player 控制項搭配 Microsoft Office
description: 使用 Windows Media Player 控制項搭配 Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player、Office
- Windows Media Player 物件模型，Office
- 物件模型、Office
- Windows Media Player Mobile、Office
- Windows Media Player ActiveX 控制項、Office
- Windows Media Player 的行動 ActiveX 控制項、Office
- ActiveX 控制項，Office
- Office 檔內嵌
- 內嵌、Office 檔
- Windows Media Player ActiveX 控制項，Excel
- Windows Media Player 的行動 ActiveX 控制項、Excel
- ActiveX 控制項，Excel
- 內嵌，Excel 試算表
- Excel 試算表嵌入
- Windows Media Player ActiveX 控制項，PowerPoint
- Windows Media Player Mobile ActiveX 控制項，PowerPoint
- ActiveX 控制項，PowerPoint
- 內嵌，PowerPoint 投影片放映
- PowerPoint 投影片放映內嵌
- Windows Media Player ActiveX 控制項，Word
- Windows Media Player 的行動 ActiveX 控制項，Word
- ActiveX 控制項，Word
- Word 檔內嵌
- 內嵌、Word 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504b46b4fb409dede108c41b43014c3aaeae5ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932274"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a><span data-ttu-id="9338b-134">使用 Windows Media Player 控制項搭配 Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="9338b-134">Using the Windows Media Player Control with Microsoft Office</span></span>

<span data-ttu-id="9338b-135">本節說明如何在使用 Microsoft Office XP 建立的各種檔中內嵌 Windows Media Player 9 系列或更新版本的 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="9338b-135">This section describes how to embed the Windows Media Player 9 Series or later ActiveX control in various documents created using Microsoft Office XP.</span></span>

<span data-ttu-id="9338b-136">在 Microsoft Word、Excel 和 PowerPoint®中，您可以從 [**插入**] 功能表選取 [**物件**]，然後從可用的物件類型清單中選擇 [ **Windows Media Player** ] 來內嵌控制項。</span><span class="sxs-lookup"><span data-stu-id="9338b-136">In Microsoft Word, Excel, and PowerPoint®, you embed the control by selecting **Object** from the **Insert** menu, then choosing **Windows Media Player** from the list of available object types.</span></span> <span data-ttu-id="9338b-137">Windows Media Player 控制項會出現在檔中的目前位置。</span><span class="sxs-lookup"><span data-stu-id="9338b-137">The Windows Media Player control appears in the document at the current location.</span></span> <span data-ttu-id="9338b-138">然後，您可以從控制項的快捷方式功能表，選取 [Excel) 中的 **格式控制項** ( **格式物件** ]，以調整配置、文字換行樣式和其他格式選項。</span><span class="sxs-lookup"><span data-stu-id="9338b-138">You can then select **Format Control** ( **Format Object** in Excel) from the shortcut menu for the control to adjust the layout, text wrapping style, and other format options.</span></span> <span data-ttu-id="9338b-139">在 Word 和 Excel 中，您必須處於設計模式才能完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="9338b-139">In Word and Excel, you must be in design mode to do this.</span></span>

<span data-ttu-id="9338b-140">一旦將控制項定位並格式化之後，您就可以使用 [ **屬性** ] 對話方塊進行設定，這個對話方塊可從 [ **控制項工具箱** ] 或 Word 和 Excel 的設計模式中的快捷方式功能表進行存取。</span><span class="sxs-lookup"><span data-stu-id="9338b-140">Once you have positioned and formatted the control, you can configure it using the **Properties** dialog box, which is accessible from the **Control Toolbox** or from the shortcut menu in design mode for Word and Excel.</span></span> <span data-ttu-id="9338b-141">您可以在這裡指定基本的播放程式控制項屬性，例如控制項名稱、數位媒體檔案的 URL，以及使用者介面模式。</span><span class="sxs-lookup"><span data-stu-id="9338b-141">Here you can specify basic Player control properties such as the control name, the URL of a digital media file, and the user interface mode.</span></span> <span data-ttu-id="9338b-142">將 [ **uiMode** ] 屬性設定為 [無] 會隱藏控制項中的所有專案，除了 [影片] 或 [視覺效果] 視窗之外，還可讓您使用 VISUAL BASIC FOR APPLICATIONS (VBA) 來處理按鈕點擊和播放機控制項事件，以新增您自己的按鈕及撰寫腳本程式碼。</span><span class="sxs-lookup"><span data-stu-id="9338b-142">Setting the **uiMode** property to "none" hides everything in the control except the video or visualization window, allowing you to add your own buttons and write script code using Visual Basic for Applications (VBA) to handle the button clicks and Player control events.</span></span>

<span data-ttu-id="9338b-143">在 [基本 **屬性** ] 對話方塊中，您也可以在選取該資料列之後，按兩下 [ (自訂) ] 資料列或按一下省略號 ( [...] ) 按鈕，以存取更精密的 **Windows Media Player 控制項屬性** 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="9338b-143">From the basic **Properties** dialog box, you can also access the more sophisticated **Windows Media Player Control Properties** dialog box by double-clicking the "(Custom)" row or by clicking the ellipsis ("...") button after selecting that row.</span></span> <span data-ttu-id="9338b-144">您可以從這個對話方塊修改所有可用的播放程式控制控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="9338b-144">From this dialog box, you can modify all available Player control properties.</span></span>

> [!Note]  
> <span data-ttu-id="9338b-145">您必須小心不要在播放程式控制項的事件處理常式中採取動作，這會導致控制項遭到終結。</span><span class="sxs-lookup"><span data-stu-id="9338b-145">You must be careful not to take actions in Player control event handlers that will result in the control being destroyed.</span></span> <span data-ttu-id="9338b-146">例如，如果您將 Windows Media Player 控制項內嵌在 PowerPoint 簡報中的投影片上，請不要從 Player **openStateChange** 事件或任何其他事件呼叫 PowerPoint **Next** 方法。</span><span class="sxs-lookup"><span data-stu-id="9338b-146">For example, if you embed the Windows Media Player control on a slide in a PowerPoint presentation, do not call the PowerPoint **Next** method from the Player **openStateChange** event or any other event.</span></span>

 

> [!Note]  
> <span data-ttu-id="9338b-147">此外，您不應該從 Player 控制項事件處理常式設定 **player. URL** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9338b-147">In addition, you should not set the **Player.URL** property from a Player control event handler.</span></span>

 

<span data-ttu-id="9338b-148">在 FrontPage 中，從 [**插入**] 功能表選取 [ **Web 元件**]，將 Windows Media Player 控制項新增至網頁。</span><span class="sxs-lookup"><span data-stu-id="9338b-148">In FrontPage, add the Windows Media Player control to a webpage by selecting **Web Component** from the **Insert** menu.</span></span> <span data-ttu-id="9338b-149">在 [**插入 Web 元件**] 對話方塊中，從 [**元件類型**] 清單中選取 [ **Advanced Controls** ]，然後從控制項選項清單中選取 [ **ActiveX 控制項**]。</span><span class="sxs-lookup"><span data-stu-id="9338b-149">In the **Insert Web Component** dialog box, select **Advanced Controls** from the **Component type** list, then select **ActiveX Control** from the list of control choices.</span></span> <span data-ttu-id="9338b-150">在對話方塊的下一個視窗中，選取 [ **Windows Media Player**]。</span><span class="sxs-lookup"><span data-stu-id="9338b-150">In the next window of the dialog box, select **Windows Media Player**.</span></span> <span data-ttu-id="9338b-151">如果未列出，請按一下 [**自訂**]，然後選取 **控制項** 清單中的 [ **Windows Media Player** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="9338b-151">If it is not listed, click **Customize** and select the **Windows Media Player** check box in the **Control** list.</span></span>

<span data-ttu-id="9338b-152">內嵌 Windows Media Player 控制項之後，您可以將其定位和調整大小，並從控制項的快捷方式功能表中選取 [ **ActiveX 控制項屬性** ] 來修改其屬性。</span><span class="sxs-lookup"><span data-stu-id="9338b-152">After the Windows Media Player control is embedded, you can position and resize it, and modify its properties by selecting **ActiveX Control Properties** from the shortcut menu for the control.</span></span> <span data-ttu-id="9338b-153">在 HTML 視圖中，您指定的屬性值會出現在代表 Windows Media Player 控制項的 OBJECT 元素中。</span><span class="sxs-lookup"><span data-stu-id="9338b-153">In the HTML view, the property values that you specify appear in the OBJECT element representing the Windows Media Player control.</span></span> <span data-ttu-id="9338b-154">物件名稱會顯示為 ID 屬性，而控制項屬性會顯示為 PARAM 標記。</span><span class="sxs-lookup"><span data-stu-id="9338b-154">The object name appears as the ID attribute, and the control properties appear as PARAM tags.</span></span> <span data-ttu-id="9338b-155">物件名稱可讓您存取 Windows Media Player 控制項物件模型，您可以使用 Microsoft JScript 進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="9338b-155">The object name gives you access to the Windows Media Player control object model, which you can program using Microsoft JScript.</span></span> <span data-ttu-id="9338b-156">如需詳細資訊，請參閱 [使用網頁中的 Windows Media Player 控制項](using-the-windows-media-player-control-in-a-web-page.md)。</span><span class="sxs-lookup"><span data-stu-id="9338b-156">For more information, see [Using the Windows Media Player Control in a Web Page](using-the-windows-media-player-control-in-a-web-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9338b-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="9338b-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9338b-158">**播放機控制指南**</span><span class="sxs-lookup"><span data-stu-id="9338b-158">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




