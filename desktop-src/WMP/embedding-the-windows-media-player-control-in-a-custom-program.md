---
title: 在自訂程式中嵌入 Windows Media Player 控制項
description: 在自訂程式中嵌入 Windows Media Player 控制項
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- 內嵌，自訂程式
- 自訂程式內嵌
- 內嵌、以 Visual Basic 為基礎的程式
- 以 Visual Basic 為基礎的程式內嵌
- 內嵌、手動使用 COM 方法
- 使用 COM 方法進行手動內嵌
- 內嵌，c + + 程式
- C + + 程式內嵌
- 內嵌、Visual Studio 程式
- Visual Studio，程式內嵌
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 441678e4b8db51040e18d9d31d2af78db134f74b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021224"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a><span data-ttu-id="0aa84-120">在自訂程式中嵌入 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="0aa84-120">Embedding the Windows Media Player Control in a Custom Program</span></span>

<span data-ttu-id="0aa84-121">由於 Windows Media Player ActiveX 控制項是以 Microsoft 元件物件模型 (COM) 技術為基礎，因此您可以將它內嵌在以許多不同的程式設計語言撰寫的程式中。</span><span class="sxs-lookup"><span data-stu-id="0aa84-121">Because the Windows Media Player ActiveX control is based on Microsoft Component Object Model (COM) technology, you can embed it in programs written with many different programming languages.</span></span> <span data-ttu-id="0aa84-122">Windows Media Player 控制項代表將複雜數位媒體功能新增至任何程式的簡單方法。</span><span class="sxs-lookup"><span data-stu-id="0aa84-122">The Windows Media Player control represents an easy way to add sophisticated digital media functionality to any program.</span></span>

<span data-ttu-id="0aa84-123">在 Microsoft Visual Basic 中，您可以將控制項加入至控制項工具箱、將控制項放在表單上，然後調整 [屬性] 視窗中的控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="0aa84-123">In Microsoft Visual Basic, you can add the control to the control toolbox, place it on a form, and adjust the control properties in the properties window.</span></span> <span data-ttu-id="0aa84-124">如果您想要自訂使用者介面，您可以將命令按鈕放在表單上，並加入管理 Windows Media Player 控制項的程式碼。</span><span class="sxs-lookup"><span data-stu-id="0aa84-124">If you want a custom user interface, you can place command buttons on the form and add code that manages the Windows Media Player control.</span></span> <span data-ttu-id="0aa84-125">在以 Visual Basic 為基礎的程式中內嵌控制項，與在 Office 檔中內嵌控制項並使用 VBA 進行程式設計的方式非常類似。</span><span class="sxs-lookup"><span data-stu-id="0aa84-125">Embedding the control in a Visual Basic-based program is very similar to embedding it in an Office document and programming it with VBA.</span></span>

<span data-ttu-id="0aa84-126">或者，您可以使用 COM 方法，以手動方式內嵌控制項，將控制項具現化，並存取 [c + + 的物件模型參考](object-model-reference-for-c.md)中記載的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="0aa84-126">Alternately, you can embed the control manually using COM methods to instantiate the control and access the COM interfaces documented in [Object Model Reference for C++](object-model-reference-for-c.md).</span></span>

<span data-ttu-id="0aa84-127">當您在 c + + 程式中內嵌 Windows Media Player 控制項時，您可以選擇執行允許控制項在遠端模式中執行的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="0aa84-127">When you embed the Windows Media Player control in a C++ program, you have the option of implementing COM interfaces that allow the control to run in remote mode.</span></span> <span data-ttu-id="0aa84-128">這表示嵌入的控制項會與播放程式的完整模式共用相同的播放引擎，而使用者可以在完整模式和停駐的狀態之間來回切換，而不會中斷數位媒體播放。</span><span class="sxs-lookup"><span data-stu-id="0aa84-128">This means that the embedded control shares the same playback engine as the full mode of the Player, and users can switch back and forth between the full mode and the docked state without interrupting digital media playback.</span></span> <span data-ttu-id="0aa84-129">您也可以控制當使用者切換至未移除狀態時，完整模式播放程式的各種窗格中所顯示的內容。</span><span class="sxs-lookup"><span data-stu-id="0aa84-129">You can also control what is displayed in the various panes of the full mode Player when your users switch to the undocked state.</span></span>

<span data-ttu-id="0aa84-130">使用 c + + 內嵌，您也可以選擇將面板定義檔套用到內嵌的播放機控制項。</span><span class="sxs-lookup"><span data-stu-id="0aa84-130">With C++ embedding, you also have the option of applying a skin definition file to the embedded Player control.</span></span> <span data-ttu-id="0aa84-131">這是建立輕量使用者介面程式碼的簡單方法，您可以將它與您的主要程式碼分開維護。</span><span class="sxs-lookup"><span data-stu-id="0aa84-131">This is an easy way to create lightweight user interface code that you can maintain separately from your main program code.</span></span>

<span data-ttu-id="0aa84-132">Microsoft Visual Studio 支援嵌入 ActiveX 控制項，包括 Windows Media Player 控制項。</span><span class="sxs-lookup"><span data-stu-id="0aa84-132">Microsoft Visual Studio supports embedding ActiveX controls, including the Windows Media Player control.</span></span> <span data-ttu-id="0aa84-133">當您選擇這麼做時，Visual Studio 會建立新的替代互通性 (interop) 元件，以管理 .NET Framework 與 Windows Media Player 控制項之間的互通性。</span><span class="sxs-lookup"><span data-stu-id="0aa84-133">When you choose to do this, Visual Studio creates a new alternate interoperability (interop) assembly to manage interoperability between the .NET Framework and the Windows Media Player control.</span></span> <span data-ttu-id="0aa84-134">Visual Studio 使用 .NET Framework tlbimp.exe 工具來建立 interop 元件。</span><span class="sxs-lookup"><span data-stu-id="0aa84-134">Visual Studio uses the .NET Framework tlbimp.exe tool to create the interop assembly.</span></span> <span data-ttu-id="0aa84-135">這表示使用 Visual Studio 中的 IntelliSense 功能時所顯示的簽章，會使用目前版本的 tlbimp 所決定的語法。</span><span class="sxs-lookup"><span data-stu-id="0aa84-135">This means that the signatures displayed when using the IntelliSense feature in Visual Studio use semantics determined by the current version of tlbimp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aa84-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="0aa84-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aa84-137">**內嵌 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="0aa84-137">**Embedding the Windows Media Player Control**</span></span>](embedding-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="0aa84-138">**在 c + + 程式中使用 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="0aa84-138">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[<span data-ttu-id="0aa84-139">**在 .NET Framework 方案中使用 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="0aa84-139">**Using the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[<span data-ttu-id="0aa84-140">**使用 Windows Media Player 控制項搭配 Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="0aa84-140">**Using the Windows Media Player Control with Visual Basic**</span></span>](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




