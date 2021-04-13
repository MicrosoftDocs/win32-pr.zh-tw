---
title: 使用 Windows Media Player 控制項搭配 Visual Basic
description: 使用 Windows Media Player 控制項搭配 Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player，Visual Basic
- Windows Media Player 物件模型，Visual Basic
- 物件模型，Visual Basic
- Windows Media Player 行動裝置，Visual Basic
- Windows Media Player ActiveX 控制項，Visual Basic
- Windows Media Player 的行動 ActiveX 控制項，Visual Basic
- ActiveX 控制項，Visual Basic
- 以 Visual Basic 為基礎的程式內嵌
- 內嵌、以 Visual Basic 為基礎的程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f2ddd78fe5a254f5bf699fbd2557f1e8700c73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301296"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a><span data-ttu-id="264a4-119">使用 Windows Media Player 控制項搭配 Visual Basic</span><span class="sxs-lookup"><span data-stu-id="264a4-119">Using the Windows Media Player Control with Visual Basic</span></span>

<span data-ttu-id="264a4-120">本節說明如何在使用 Microsoft Visual Basic 6.0 所建立的應用程式中，使用 Windows Media Player 9 系列或更新版本的 ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="264a4-120">This section describes how to use the Windows Media Player 9 Series or later ActiveX control in applications created with Microsoft Visual Basic 6.0.</span></span>

## <a name="getting-started"></a><span data-ttu-id="264a4-121">開始使用</span><span class="sxs-lookup"><span data-stu-id="264a4-121">Getting Started</span></span>

<span data-ttu-id="264a4-122">若要將 Windows Media Player 控制項新增至 [工具箱]，請先從 [**專案**] 功能表選取 [**元件**]。</span><span class="sxs-lookup"><span data-stu-id="264a4-122">To add the Windows Media Player control to the toolbox, first select **Components** from the **Project** menu.</span></span> <span data-ttu-id="264a4-123">在 [元件] 對話方塊中，選取 [Windows Media Player] 旁的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="264a4-123">In the Components dialog box, select the check box next to "Windows Media Player".</span></span> <span data-ttu-id="264a4-124">在對話方塊底部，確認選取的檔案是 wmp.dll。</span><span class="sxs-lookup"><span data-stu-id="264a4-124">At the bottom of the dialog box, confirm that the selected file is wmp.dll.</span></span> <span data-ttu-id="264a4-125">關閉對話方塊之後，您可以使用一般方式將 Windows Media Player 控制項的實例放在表單上。</span><span class="sxs-lookup"><span data-stu-id="264a4-125">After closing the dialog box, you can place an instance of the Windows Media Player control on your form in the usual ways.</span></span>

<span data-ttu-id="264a4-126">您可以使用屬性視窗來設定許多控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="264a4-126">You can set many control properties using the Properties window.</span></span> <span data-ttu-id="264a4-127">若要設定某些屬性，您必須使用 [Windows Media Player 屬性] 對話方塊，您可以使用屬性視窗中的「 (自訂) 」專案來開啟此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="264a4-127">To set some properties you must use the Windows Media Player Properties dialog box, which you open using the "(Custom)" item in the Properties window.</span></span>

## <a name="object-references"></a><span data-ttu-id="264a4-128">物件參考</span><span class="sxs-lookup"><span data-stu-id="264a4-128">Object References</span></span>

<span data-ttu-id="264a4-129">您可以使用特定的播放機控制項屬性來取得特定物件的參考。</span><span class="sxs-lookup"><span data-stu-id="264a4-129">You use certain Player control properties to get references to particular objects.</span></span> <span data-ttu-id="264a4-130">例如， **cdromCollection** 屬性會傳回 **cdromCollection** 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="264a4-130">For example, the **cdromCollection** property returns a reference to a **CdromCollection** object.</span></span> <span data-ttu-id="264a4-131">您必須將這類參考指派給宣告為對應介面的變數。</span><span class="sxs-lookup"><span data-stu-id="264a4-131">You must assign such a reference to a variable that you declared as the corresponding interface.</span></span> <span data-ttu-id="264a4-132">例如，在 **cdromCollection** 屬性的情況下，您會將其傳回值指派給 **IWMPCdromCollection** 類型的變數。</span><span class="sxs-lookup"><span data-stu-id="264a4-132">In the case of the **cdromCollection** property, for example, you assign its return value to a variable of type **IWMPCdromCollection**.</span></span>

<span data-ttu-id="264a4-133">閱讀[c + + 物件模型參考](object-model-reference-for-c.md)中的[介面](interfaces.md)主題，以識別哪些物件會執行多個介面。</span><span class="sxs-lookup"><span data-stu-id="264a4-133">Read the [Interfaces](interfaces.md) topic in the [Object Model Reference for C++](object-model-reference-for-c.md) to identify which objects implement multiple interfaces.</span></span> <span data-ttu-id="264a4-134">在這些情況下，您必須將物件變數宣告為此 SDK 中記載的最高編號介面，才能存取該物件的所有屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="264a4-134">In those cases, you must declare an object variable as the highest-numbered interface documented in this SDK to have access to all of the properties and methods of that object.</span></span> <span data-ttu-id="264a4-135">例如，您應該將 Windows Media Player control **currentMedia** 屬性的值指派給宣告為 **IWMPMedia3** 的變數，以確保您可以存取 **getAttributeCountByType** 和 **getItemInfoByType** 方法。</span><span class="sxs-lookup"><span data-stu-id="264a4-135">For example, you should assign the value of the Windows Media Player control **currentMedia** property to a variable declared as **IWMPMedia3** to assure that you have access to the **getAttributeCountByType** and **getItemInfoByType** methods.</span></span>

> [!Note]  
> <span data-ttu-id="264a4-136">**WindowsMediaPlayer** 物件會實 **IWMPCore**、 **IWMPCore2**、 **IWMPCore3**、 **IWMPPlayer**、 **IWMPPlayer2**、 **IWMPPlayer3** 和 **IWMPPlayer4** 介面的所有屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="264a4-136">The **WindowsMediaPlayer** object implements all of the properties and methods of the **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3**, and **IWMPPlayer4** interfaces.</span></span> <span data-ttu-id="264a4-137">您不需要為這些介面的任何一個宣告個別的變數。</span><span class="sxs-lookup"><span data-stu-id="264a4-137">You do not need to declare separate variables for any of these interfaces.</span></span> <span data-ttu-id="264a4-138">您可以使用指派給 **WindowsMediaPlayer** 實例的名稱來存取其所有成員。</span><span class="sxs-lookup"><span data-stu-id="264a4-138">You can access all of their members using the name you assigned to your **WindowsMediaPlayer** instance.</span></span>

 

<span data-ttu-id="264a4-139">在 Visual Basic 的物件瀏覽器中，您會看到許多用於 Windows Media Player 控制項私用的介面，包括支援面板開發人員的部分。</span><span class="sxs-lookup"><span data-stu-id="264a4-139">In the Visual Basic Object Browser you will see many interfaces that are intended for private use by the Windows Media Player control, including some that support skin developers.</span></span> <span data-ttu-id="264a4-140">您應該只使用此 SDK 中記載的物件、屬性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="264a4-140">You should use only the objects, properties, methods, and events that are documented in this SDK.</span></span>

## <a name="additional-tips"></a><span data-ttu-id="264a4-141">其他秘訣</span><span class="sxs-lookup"><span data-stu-id="264a4-141">Additional Tips</span></span>

-   <span data-ttu-id="264a4-142">參考檔會顯示 JScript 語法。</span><span class="sxs-lookup"><span data-stu-id="264a4-142">The reference documentation shows JScript syntax.</span></span> <span data-ttu-id="264a4-143">在 JScript 中，傳遞給方法的引數一律會以括弧括住。</span><span class="sxs-lookup"><span data-stu-id="264a4-143">In JScript, arguments passed to methods are always enclosed in parentheses.</span></span> <span data-ttu-id="264a4-144">在 Visual Basic 6.0 中，傳遞至未傳回值之方法的引數不能以括弧括住。</span><span class="sxs-lookup"><span data-stu-id="264a4-144">In Visual Basic 6.0, arguments passed to methods that do not return a value must not be enclosed in parentheses.</span></span>
-   <span data-ttu-id="264a4-145">某些屬性或方法可能不會出現在 [Visual Basic 程式碼編輯器] 的 [自動清單程式碼-自動完成] 功能中。</span><span class="sxs-lookup"><span data-stu-id="264a4-145">Some properties or methods may not appear in the Auto List code-completion feature in the Visual Basic code editor.</span></span> <span data-ttu-id="264a4-146">您仍然可以使用這些成員的名稱，如同在本檔中所顯示的名稱一樣。</span><span class="sxs-lookup"><span data-stu-id="264a4-146">You can still use those members by typing their names exactly as they appear in this documentation.</span></span>
-   <span data-ttu-id="264a4-147">使用 **uimode** 屬性管理控制項的視覺外觀。</span><span class="sxs-lookup"><span data-stu-id="264a4-147">Manage the visual appearance of the control using the **uimode** property.</span></span> <span data-ttu-id="264a4-148">您可以透過兩種方式來這麼做。</span><span class="sxs-lookup"><span data-stu-id="264a4-148">You can do so in two ways.</span></span> <span data-ttu-id="264a4-149">您可以使用 [Windows Media Player 屬性] 對話方塊中的 [ **選取模式** ] 下拉式清單，也可以在屬性視窗中輸入正確的值。</span><span class="sxs-lookup"><span data-stu-id="264a4-149">You can use the **Select a mode** drop-down list in the Windows Media Player Properties dialog box, or you can type the correct value in the Properties window.</span></span>

    <span data-ttu-id="264a4-150">尤其是，請勿使用 **visible** 屬性來隱藏控制項;相反地，請將值「隱藏」指派給 **uimode** 屬性。</span><span class="sxs-lookup"><span data-stu-id="264a4-150">In particular, do not use the **visible** property to hide the control; instead, assign the value "invisible" to the **uimode** property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="264a4-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="264a4-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="264a4-152">**播放機控制指南**</span><span class="sxs-lookup"><span data-stu-id="264a4-152">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




