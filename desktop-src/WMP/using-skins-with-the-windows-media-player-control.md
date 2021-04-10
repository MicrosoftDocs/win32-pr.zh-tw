---
title: 搭配 Windows Media Player 控制項使用外觀
description: 搭配 Windows Media Player 控制項使用外觀
ms.assetid: 0381e0e4-c686-4ab4-b947-b883b6f4e06e
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player，c + +
- Windows Media Player 物件模型，c + +
- 物件模型，c + +
- Windows Media Player Mobile，c + +
- Windows Media Player 的 ActiveX 控制項，c + +
- Windows Media Player 的行動 ActiveX 控制項，c + +
- ActiveX 控制項，c + +
- C + + 程式內嵌
- 內嵌，c + + 程式
- Windows Media Player ActiveX 控制項，外觀
- Windows Media Player 的行動 ActiveX 控制項、外觀
- ActiveX 控制項，外觀
- 外觀，內嵌 ActiveX 控制項
- Windows Media Player 的外觀，內嵌 ActiveX 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714a8be9e471541d008fcb76a4b0398dba2162b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183542"
---
# <a name="using-skins-with-the-windows-media-player-control"></a><span data-ttu-id="d4638-124">搭配 Windows Media Player 控制項使用外觀</span><span class="sxs-lookup"><span data-stu-id="d4638-124">Using Skins with the Windows Media Player Control</span></span>

<span data-ttu-id="d4638-125">當您在 c + + 程式中內嵌 Windows Media Player 控制項時，您可以透過將面板定義檔套用至該應用程式， (UI) 自訂播放機使用者介面。</span><span class="sxs-lookup"><span data-stu-id="d4638-125">When you embed the Windows Media Player control in a C++ program, you can customize the Player user interface (UI) by applying a skin definition file to it.</span></span> <span data-ttu-id="d4638-126">面板定義檔是以 XML 為基礎的檔，指定標準和可自訂 UI 元件的配置和任何隨附的圖形。</span><span class="sxs-lookup"><span data-stu-id="d4638-126">A skin definition file is an XML-based document specifying the layout of standard and customizable UI components and any accompanying graphics.</span></span> <span data-ttu-id="d4638-127">您可以使用 Microsoft JScript 來指定這些元件的行為，並操作 Windows Media Player 控制項，而不會產生 c + + 和 COM 語法的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="d4638-127">Using Microsoft JScript, you can specify the behavior of these components and manipulate the Windows Media Player control without the overhead of C++ and COM syntax.</span></span>

<span data-ttu-id="d4638-128">面板提供簡單的方法，讓您的使用者介面程式碼和主要程式碼分開，讓它們可以獨立維護和開發。</span><span class="sxs-lookup"><span data-stu-id="d4638-128">Skins provide an easy way to keep your user interface code and your main program code separate so that they can be maintained and developed independently.</span></span> <span data-ttu-id="d4638-129">您也可以重複使用原本設計的面板，以便在面板模式中供獨立播放程式使用。</span><span class="sxs-lookup"><span data-stu-id="d4638-129">You can also reuse skins originally designed for use by the standalone Player in skin mode.</span></span> <span data-ttu-id="d4638-130">您專為 c + + 程式設計的面板程式碼可透過程式可提供的可編寫腳本的物件與程式互動。</span><span class="sxs-lookup"><span data-stu-id="d4638-130">Skin code that you design specifically for C++ programs can interact with your programs through a scriptable object that your program can provide.</span></span>

<span data-ttu-id="d4638-131">若要啟用 Windows Media Player 控制項的面板模式，您的程式必須執行 **IWMPRemoteMediaServices** 介面。</span><span class="sxs-lookup"><span data-stu-id="d4638-131">To enable skin mode for the Windows Media Player control, your program must implement the **IWMPRemoteMediaServices** interface.</span></span> <span data-ttu-id="d4638-132">雖然您可以同時使用具有控制項和遠端控制項的面板，但您可以使用這個介面來啟用任一個功能，而不需要啟用另一個功能。</span><span class="sxs-lookup"><span data-stu-id="d4638-132">Although you can use skins with the control and remote the control at the same time, you can use this interface to enable either feature without enabling the other.</span></span> <span data-ttu-id="d4638-133">若要停用遠端處理，只要傳遞 "Local" 的值做為 **GetServiceType** 方法的 out 參數，並 \_ 從 **GetApplicationName** 方法傳回 E >notimpl 的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="d4638-133">To disable remoting, simply pass a value of "Local" as the out parameter of the **GetServiceType** method, and return an HRESULT of E\_NOTIMPL from the **GetApplicationName** method.</span></span>

<span data-ttu-id="d4638-134">若要將 Windows Media Player 控制項切換至面板模式，請呼叫 **IWMPPlayer：:p 的 \_ uiMode** 方法，並傳入 "custom" 的值。</span><span class="sxs-lookup"><span data-stu-id="d4638-134">To switch the Windows Media Player control to skin mode, call the **IWMPPlayer::put\_uiMode** method, passing in a value of "custom".</span></span> <span data-ttu-id="d4638-135">從 **IWMPRemoteMediaServices：： GetCustomUIMode** 方法傳回，以指定要使用之面板定義檔的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="d4638-135">Specify the path and file name of the skin definition file to use by returning it from the **IWMPRemoteMediaServices::GetCustomUIMode** method.</span></span>

<span data-ttu-id="d4638-136">如果您想要為您的面板和程式之間的通訊提供可編寫腳本的物件，請將名稱和指標傳遞至 **IDispatch** 指標，作為 **IWMPRemoteMediaServices：： GetScriptableObject** 方法的兩個 out 參數。</span><span class="sxs-lookup"><span data-stu-id="d4638-136">If you want to provide a scriptable object for communication between your skin and your program, pass a name and a pointer to an **IDispatch** pointer as the two out parameters of the **IWMPRemoteMediaServices::GetScriptableObject** method.</span></span> <span data-ttu-id="d4638-137">然後，您的面板就可以使用指定的名稱來呼叫可編寫腳本的物件，就像是類似于 **player** global 屬性的全域屬性一樣。</span><span class="sxs-lookup"><span data-stu-id="d4638-137">Your skin can then make calls to the scriptable object by using the name specified as though it were a global attribute similar to the **player** global attribute.</span></span>

<span data-ttu-id="d4638-138">套用至遠端 Windows Media Player 控制項的面板，可以使用名為 **PlayerApplication** 的另一個全域屬性來存取 **PlayerApplication** 物件。</span><span class="sxs-lookup"><span data-stu-id="d4638-138">A skin applied to a remoted Windows Media Player control can access the **PlayerApplication** object using another global attribute called **playerApplication**.</span></span> <span data-ttu-id="d4638-139">由於 **playerApplication** 屬性無法由外觀存取，因此當您想要讓面板程式碼管理停駐和移除時，您必須使用這個全域屬性。</span><span class="sxs-lookup"><span data-stu-id="d4638-139">Because the **Player.playerApplication** property cannot be accessed by skins, you must use this global attribute when you want your skin code to manage docking and undocking.</span></span>

## <a name="samples"></a><span data-ttu-id="d4638-140">範例</span><span class="sxs-lookup"><span data-stu-id="d4638-140">Samples</span></span>

<span data-ttu-id="d4638-141">Windows Media Player SDK 安裝程式套件會安裝示範將面板套用至 Windows Media Player 控制項的範例。</span><span class="sxs-lookup"><span data-stu-id="d4638-141">The Windows Media Player SDK setup package installs a sample that demonstrates applying a skin to the Windows Media Player control.</span></span> <span data-ttu-id="d4638-142">如需詳細資訊，請參閱 RemoteSkin 範例。</span><span class="sxs-lookup"><span data-stu-id="d4638-142">See the RemoteSkin sample for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4638-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="d4638-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4638-144">**範例**</span><span class="sxs-lookup"><span data-stu-id="d4638-144">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="d4638-145">**在 c + + 程式中使用 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="d4638-145">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




