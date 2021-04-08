---
title: 使用 Windows Media Player 控制項搭配 Microsoft Visual Studio
description: 使用 Windows Media Player 控制項搭配 Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player，.NET Framework
- Windows Media Player 物件模型，.NET Framework
- 物件模型、.NET Framework
- Windows Media Player Mobile、.NET Framework
- Windows Media Player ActiveX 控制項，.NET Framework
- Windows Media Player 的行動 ActiveX 控制項，.NET Framework
- ActiveX 控制項，.NET Framework
- Windows Media Player ActiveX 控制項，Visual Studio
- Windows Media Player 的行動 ActiveX 控制項，Visual Studio
- ActiveX 控制項，Visual Studio
- .NET Framework，Visual Studio 程式嵌入
- 內嵌、Visual Studio 程式
- Visual Studio，程式內嵌
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b01fecd6acdfd5ccc9a7d823740ef3915bf9c6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "104022151"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a><span data-ttu-id="a8513-123">使用 Windows Media Player 控制項搭配 Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a8513-123">Using the Windows Media Player Control with Microsoft Visual Studio</span></span>

<span data-ttu-id="a8513-124">您可以透過 Visual Studio 中的 [工具箱]，將 Windows Media Player 9 系列或更新版本的 ActiveX 控制項新增至 .NET Framework 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a8513-124">You can add the Windows Media Player 9 Series or later ActiveX control to a .NET Framework application through the Toolbox in Visual Studio.</span></span>

## <a name="adding-the-windows-media-player-control"></a><span data-ttu-id="a8513-125">加入 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="a8513-125">Adding the Windows Media Player Control</span></span>

<span data-ttu-id="a8513-126">建立新專案之前，請確定您的電腦上已安裝最新版本的 Windows Media Player 和 Windows Media Player SDK。</span><span class="sxs-lookup"><span data-stu-id="a8513-126">Before creating a new project, make sure that the latest version of Windows Media Player and the Windows Media Player SDK is installed on your computer.</span></span>

<span data-ttu-id="a8513-127">開始 Visual Studio，然後建立新專案。</span><span class="sxs-lookup"><span data-stu-id="a8513-127">Start Visual Studio, then create a new project.</span></span>

<span data-ttu-id="a8513-128">在 Visual Studio 中，開啟 [工具箱]。</span><span class="sxs-lookup"><span data-stu-id="a8513-128">In Visual Studio, open the Toolbox.</span></span>

<span data-ttu-id="a8513-129">如果 Windows Media Player 未出現在 [工具箱] 的 [ **元件** ] 部分中，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="a8513-129">If Windows Media Player does not appear in the **Components** portion of the Toolbox, do the following:</span></span>

1.  <span data-ttu-id="a8513-130">在 [工具箱] 中按一下滑鼠右鍵，然後選取 **[選擇專案**]。</span><span class="sxs-lookup"><span data-stu-id="a8513-130">Right-click within the Toolbox, and then select **Choose Items**.</span></span> <span data-ttu-id="a8513-131">這會開啟 [ **自訂工具箱** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a8513-131">This opens the **Customize Toolbox** dialog box.</span></span>
2.  <span data-ttu-id="a8513-132">在 [ **COM 元件** ] 索引標籤上，選取 [Windows Media Player]。</span><span class="sxs-lookup"><span data-stu-id="a8513-132">On the **COM Components** tab, select Windows Media Player.</span></span>

    <span data-ttu-id="a8513-133">如果 Windows Media Player 未出現在清單中，請按一下 **[流覽]**，然後開啟 [Wmp.dll]，這應該會出現在 Windows [ \\ System32] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="a8513-133">If Windows Media Player does not appear in the list, click **Browse**, and then open Wmp.dll, which should be in the Windows\\System32 folder.</span></span>

3.  <span data-ttu-id="a8513-134">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="a8513-134">Click **OK**.</span></span> <span data-ttu-id="a8513-135">Windows Media Player 控制項將放置在目前的 [工具箱] 索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="a8513-135">The Windows Media Player control will be placed on the current Toolbox tab.</span></span>

<span data-ttu-id="a8513-136">您現在可以在 [工具箱] 中選取 Windows Media Player，並將其新增至表單。</span><span class="sxs-lookup"><span data-stu-id="a8513-136">You can now select Windows Media Player in the Toolbox and add it to a form.</span></span>

<span data-ttu-id="a8513-137">Visual Studio 提供 Windows Media Player 的控制項預設名稱，例如 "axWindowsMediaPlayer1"。</span><span class="sxs-lookup"><span data-stu-id="a8513-137">Visual Studio gives the Windows Media Player control a default name such as "axWindowsMediaPlayer1".</span></span> <span data-ttu-id="a8513-138">您可能會想要將名稱變更為更容易記住的名稱，例如「Player」。</span><span class="sxs-lookup"><span data-stu-id="a8513-138">You may want to change the name to something more easily remembered, such as "Player".</span></span>

<span data-ttu-id="a8513-139">從 [工具箱] 新增 Windows Media Player 控制項也會新增 Visual Studio、AxWMPLib 和 WMPLib 所建立之兩個程式庫的參考。</span><span class="sxs-lookup"><span data-stu-id="a8513-139">Adding the Windows Media Player control from the Toolbox also adds references to two libraries created by Visual Studio, AxWMPLib and WMPLib.</span></span> <span data-ttu-id="a8513-140">您可以在 [ **參考**] 下的方案總管中找到它們。</span><span class="sxs-lookup"><span data-stu-id="a8513-140">You can find them in the Solution Explorer under **References**.</span></span>

<span data-ttu-id="a8513-141">若要更輕鬆地使用 Player 命名空間中的物件，您應該在檔案的 using 或 imports 指示詞中包含命名空間，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a8513-141">To make using the objects in the Player namespace easier, you should include the namespace in the using or imports directives of your files, as follows:</span></span>


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



<span data-ttu-id="a8513-142">指示詞可確保您可以參考 **Player** 物件，而不需要完整限定其名稱。</span><span class="sxs-lookup"><span data-stu-id="a8513-142">The directive ensures that you can refer to **Player** objects without fully qualifying their names.</span></span>

> [!Note]  
> <span data-ttu-id="a8513-143">Windows Media Player 控制項是來自 **AxWMPLib** 命名空間的 **AxWindowsMediaPlayer** 物件。</span><span class="sxs-lookup"><span data-stu-id="a8513-143">The Windows Media Player control is an **AxWindowsMediaPlayer** object from the **AxWMPLib** namespace.</span></span> <span data-ttu-id="a8513-144">不過， **AxWindowsMediaPlayer** 類別會使用 **WMPLib** 命名空間中的資料類型、介面和其他元素。</span><span class="sxs-lookup"><span data-stu-id="a8513-144">However, the **AxWindowsMediaPlayer** class uses data types, interfaces, and other elements from the **WMPLib** namespace.</span></span>

 

## <a name="configuring-visibility-of-the-control"></a><span data-ttu-id="a8513-145">設定控制項的可見度</span><span class="sxs-lookup"><span data-stu-id="a8513-145">Configuring Visibility of the Control</span></span>

<span data-ttu-id="a8513-146">當您第一次將 Windows Media Player 控制項新增至表單時，就會顯示該控制項。</span><span class="sxs-lookup"><span data-stu-id="a8513-146">When you first add the Windows Media Player control to a form, it will be visible.</span></span> <span data-ttu-id="a8513-147">如果您不想要在應用程式中使用播放程式的可見影像，請設定下列其中一個屬性來隱藏預設播放程式：</span><span class="sxs-lookup"><span data-stu-id="a8513-147">If you do not want to use the visible image of the Player in your application, hide the default Player by setting any one of the following properties:</span></span>



| <span data-ttu-id="a8513-148">屬性</span><span class="sxs-lookup"><span data-stu-id="a8513-148">Property</span></span>        | <span data-ttu-id="a8513-149">值</span><span class="sxs-lookup"><span data-stu-id="a8513-149">Value</span></span>                                                 |
|-----------------|-------------------------------------------------------|
| <span data-ttu-id="a8513-150">**uiMode**</span><span class="sxs-lookup"><span data-stu-id="a8513-150">**uiMode**</span></span>      | <span data-ttu-id="a8513-151">「隱藏」 (查看 [uiMode](player-uimode.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="a8513-151">"invisible" (See [Player.uiMode](player-uimode.md).)</span></span> |
| <span data-ttu-id="a8513-152">**Visible**</span><span class="sxs-lookup"><span data-stu-id="a8513-152">**Visible**</span></span>     | <span data-ttu-id="a8513-153">"false"</span><span class="sxs-lookup"><span data-stu-id="a8513-153">"false"</span></span>                                               |
| <span data-ttu-id="a8513-154">**大小：寬度**</span><span class="sxs-lookup"><span data-stu-id="a8513-154">**Size.Width**</span></span>  | <span data-ttu-id="a8513-155">0</span><span class="sxs-lookup"><span data-stu-id="a8513-155">0</span></span>                                                     |
| <span data-ttu-id="a8513-156">**大小：高度**</span><span class="sxs-lookup"><span data-stu-id="a8513-156">**Size.Height**</span></span> | <span data-ttu-id="a8513-157">0</span><span class="sxs-lookup"><span data-stu-id="a8513-157">0</span></span>                                                     |



 

<span data-ttu-id="a8513-158">當表單設計工具中選取了 Windows Media Player 控制項時，您可以在程式碼或 [ **屬性** ] 視窗中設定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a8513-158">You can set these properties either in code or in the **Properties** window when the Windows Media Player control is selected in the form designer.</span></span>

## <a name="object-model-compatibility-of-the-control"></a><span data-ttu-id="a8513-159">控制項的物件模型相容性</span><span class="sxs-lookup"><span data-stu-id="a8513-159">Object Model Compatibility of the Control</span></span>

<span data-ttu-id="a8513-160">在與非受控碼和腳本相同的 .NET Framework 中，Windows Media Player 控制項的物件模型基本上是相同的。</span><span class="sxs-lookup"><span data-stu-id="a8513-160">The object model for the Windows Media Player control is basically the same in the .NET Framework as in unmanaged code and script.</span></span> <span data-ttu-id="a8513-161">不過，專案的公開方式有一些差異：</span><span class="sxs-lookup"><span data-stu-id="a8513-161">However, there are differences in how elements are exposed:</span></span>

-   <span data-ttu-id="a8513-162">大部分的物件都會在其基礎 COM 介面的名稱底下公開。</span><span class="sxs-lookup"><span data-stu-id="a8513-162">Most objects are exposed under the name of their underlying COM interface.</span></span> <span data-ttu-id="a8513-163">例如， **播放清單** 物件會公開為 **IWMPPlaylist**。</span><span class="sxs-lookup"><span data-stu-id="a8513-163">For example, the **Playlist** object is exposed as **IWMPPlaylist**.</span></span>
-   <span data-ttu-id="a8513-164">某些介面有較新的版本。</span><span class="sxs-lookup"><span data-stu-id="a8513-164">Some interfaces have later versions.</span></span> <span data-ttu-id="a8513-165">例如， **IWMPMedia** 在 **IWMPMedia2** 和 **IWMPMedia3** 中獲得額外的功能。</span><span class="sxs-lookup"><span data-stu-id="a8513-165">For example, **IWMPMedia** was given additional functionality in **IWMPMedia2** and **IWMPMedia3**.</span></span> <span data-ttu-id="a8513-166">如果您將物件宣告為 **IWMPMedia**，通常就可以存取所有介面版本的功能。</span><span class="sxs-lookup"><span data-stu-id="a8513-166">If you declare an object as **IWMPMedia**, you usually have access to the functionality of all versions of the interface.</span></span> <span data-ttu-id="a8513-167">不過，IntelliSense®將無法辨識較新版介面的方法或屬性，而 Visual Basic .NET 編輯器將不會自動校正大小寫。</span><span class="sxs-lookup"><span data-stu-id="a8513-167">However, IntelliSense® will not recognize the methods or properties of the later-version interfaces, and the Visual Basic .NET editor will not automatically correct capitalization.</span></span> <span data-ttu-id="a8513-168">若要取得 Visual Studio 的 IntelliSense 和其他功能的完整優點，請使用最新版本的介面（例如 **IWMPMedia3**）來宣告物件。</span><span class="sxs-lookup"><span data-stu-id="a8513-168">To get the full benefit of IntelliSense and other features of Visual Studio, declare the object by using the latest version of the interface, such as **IWMPMedia3**.</span></span>
-   <span data-ttu-id="a8513-169">沒有任何索引屬性 (c # ) 或 Visual Basic .NET)  (的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="a8513-169">There are no indexed properties (C#) or default properties (Visual Basic .NET).</span></span> <span data-ttu-id="a8513-170">例如，若要取出 **播放清單專案**，您必須在 c # 中呼叫 **IWMPlaylist \_** ，或在 Visual Basic .Net 中取出 **IWMPlayist. item** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a8513-170">For example, to retrieve a **Playlist.item**, you must call the **IWMPlaylist.get\_Item** accessor method in C# or retrieve the **IWMPlayist.Item** property in Visual Basic .NET.</span></span>
-   <span data-ttu-id="a8513-171">由於 Windows Media Player **Controls** 屬性和每個控制項公開的 **控制項** 屬性之間有命名衝突，所以此屬性的播放程式版本在 ActiveX 控制項的內容中稱為 **CtlControls** 。</span><span class="sxs-lookup"><span data-stu-id="a8513-171">Because of a naming conflict between the Windows Media Player **Controls** property and the **Controls** property exposed by every control, the Player version of this property is called **CtlControls** in the context of the ActiveX control.</span></span> <span data-ttu-id="a8513-172"> (不過，當您以程式設計的方式建立播放機而非 ActiveX 控制項時，就不會發生這種情況。 ) </span><span class="sxs-lookup"><span data-stu-id="a8513-172">(However, this is not the case when you create the Player programmatically rather than as an ActiveX control.)</span></span>

<span data-ttu-id="a8513-173">使用 Visual Studio 中的物件瀏覽器，在 **AxWMPLib** 和 **WMPLib** 命名空間中找出方法和物件的正確 API 名稱。</span><span class="sxs-lookup"><span data-stu-id="a8513-173">Use the Object Browser in Visual Studio to locate the correct API names for methods and objects in the **AxWMPLib** and **WMPLib** namespaces.</span></span>

## <a name="distributing-your-application"></a><span data-ttu-id="a8513-174">散發您的應用程式</span><span class="sxs-lookup"><span data-stu-id="a8513-174">Distributing Your Application</span></span>

<span data-ttu-id="a8513-175">當您散發應用程式時，請務必在應用程式資料夾中安裝 AxInterop.WMPLib.dll 和 Interop.WMPLib.dll。</span><span class="sxs-lookup"><span data-stu-id="a8513-175">When you distribute your application, be sure to install AxInterop.WMPLib.dll and Interop.WMPLib.dll in the application folder.</span></span> <span data-ttu-id="a8513-176">您也必須確定使用者的電腦上已安裝必要的 Windows Media Player 版本。</span><span class="sxs-lookup"><span data-stu-id="a8513-176">You will also need to make sure that the required Windows Media Player version is installed on the user's computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8513-177">相關主題</span><span class="sxs-lookup"><span data-stu-id="a8513-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8513-178">**以程式設計方式建立 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="a8513-178">**Creating the Windows Media Player Control Programmatically**</span></span>](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[<span data-ttu-id="a8513-179">**在 c # 方案中內嵌 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="a8513-179">**Embedding the Windows Media Player Control in a C# Solution**</span></span>](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[<span data-ttu-id="a8513-180">**在 Visual Basic .NET 方案中內嵌 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="a8513-180">**Embedding the Windows Media Player Control in a Visual Basic .NET Solution**</span></span>](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




