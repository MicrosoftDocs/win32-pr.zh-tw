---
title: 在 c + + 程式中使用 Windows Media Player 控制項
description: 在 c + + 程式中使用 Windows Media Player 控制項
ms.assetid: 2531ac25-5e9d-462e-a06a-6f81bf4ca33d
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02430dbdaba3bb2e8ea3ca6e46b202a289a096f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183804"
---
# <a name="using-the-windows-media-player-control-in-a-c-program"></a><span data-ttu-id="4d3b2-119">在 c + + 程式中使用 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="4d3b2-119">Using the Windows Media Player Control in a C++ Program</span></span>

> [!Note]  
> <span data-ttu-id="4d3b2-120">Windows Media Player 9 系列或更新版本支援使用 c + + 內嵌 Windows Media Player 控制項。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-120">Using C++ to embed the Windows Media Player control is supported for Windows Media Player 9 Series or later.</span></span>

 

<span data-ttu-id="4d3b2-121">有幾種不同的方式可以在 c + + 程式中使用 Windows Media Player 控制項。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-121">There are several different ways to use the Windows Media Player control in a C++ program.</span></span> <span data-ttu-id="4d3b2-122">您可以在主控台應用程式中建立控制項的實例，也可以將控制項內嵌在 Windows 應用程式中。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-122">You can create an instance of the control in a console application, or you can embed the control in a Windows application.</span></span> <span data-ttu-id="4d3b2-123">此外，您可以執行介面，讓您以遠端模式執行內嵌的播放機控制項。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-123">Also, you can implement interfaces that enable you to run an embedded Player control in remote mode.</span></span> <span data-ttu-id="4d3b2-124">您可以套用面板定義檔來自訂內嵌控制項的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-124">You can customize the user interface of an embedded control by applying a skin definition file.</span></span>

<span data-ttu-id="4d3b2-125">下列主題將說明這項資訊。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-125">This information is described in the following topics.</span></span>



| <span data-ttu-id="4d3b2-126">主題</span><span class="sxs-lookup"><span data-stu-id="4d3b2-126">Topic</span></span>                                                                                                                                      | <span data-ttu-id="4d3b2-127">描述</span><span class="sxs-lookup"><span data-stu-id="4d3b2-127">Description</span></span>                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d3b2-128">在主控台應用程式中使用 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="4d3b2-128">Using the Windows Media Player Control in a Console Application</span></span>](using-the-windows-media-player-control-in-a-console-application.md)     | <span data-ttu-id="4d3b2-129">描述可具現化 Windows Media Player 控制項以顯示版本的簡單 c + + 主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-129">Describes a simple C++ console application that instantiates the Windows Media Player control to display the version.</span></span>                                                       |
| [<span data-ttu-id="4d3b2-130">在 Windows 應用程式中裝載 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="4d3b2-130">Hosting the Windows Media Player Control in a Windows Application</span></span>](hosting-the-windows-media-player-control-in-a-windows-application.md) | <span data-ttu-id="4d3b2-131">描述如何使用 ATL ActiveX 主控制項視窗，在 Windows 程式中內嵌 Windows Media Player 控制項。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-131">Describes how to use the ATL ActiveX host window to embed the Windows Media Player control in a Windows program.</span></span>                                                            |
| [<span data-ttu-id="4d3b2-132">遠端處理 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="4d3b2-132">Remoting the Windows Media Player Control</span></span>](remoting-the-windows-media-player-control.md)                                                 | <span data-ttu-id="4d3b2-133">描述如何以遠端模式在 c + + 程式中內嵌 Windows Media Player 控制項，讓您的使用者取消停駐控制項，以切換到播放程式的完整模式。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-133">Describes how to embed the Windows Media Player control in a C++ program in remote mode, which lets your users undock the control to switch to the full mode of the Player.</span></span> |
| [<span data-ttu-id="4d3b2-134">在 c + + 中處理事件</span><span class="sxs-lookup"><span data-stu-id="4d3b2-134">Handling Events in C++</span></span>](handling-events-in-c.md)                                                                                         | <span data-ttu-id="4d3b2-135">說明如何從 Windows Media Player 接收事件通知。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-135">Describes how to receive event notifications from Windows Media Player.</span></span>                                                                                                     |
| [<span data-ttu-id="4d3b2-136">搭配 Windows Media Player 控制項使用外觀</span><span class="sxs-lookup"><span data-stu-id="4d3b2-136">Using Skins with the Windows Media Player Control</span></span>](using-skins-with-the-windows-media-player-control.md)                                 | <span data-ttu-id="4d3b2-137">描述如何將面板檔案套用至內嵌于 c + + 程式中的 Windows Media Player 控制項。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-137">Describes how to apply a skin file to a Windows Media Player control embedded in a C++ program.</span></span>                                                                             |



 

> [!Note]  
> <span data-ttu-id="4d3b2-138">您可以將 Windows Media Player 10 個行動控制項內嵌在 Windows CE 應用程式中。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-138">You can embed the Windows Media Player 10 Mobile control in a Windows CE application.</span></span> <span data-ttu-id="4d3b2-139">您用來執行此動作的技巧，類似于桌面 Windows Media Player 控制項所使用的技巧。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-139">The techniques you use to do this are similar to those used with the desktop Windows Media Player control.</span></span> <span data-ttu-id="4d3b2-140">不過，Windows 的 ATL 和 Windows CE 的 ATL 之間有一些差異。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-140">However, there are differences between ATL for Windows and ATL for Windows CE.</span></span> <span data-ttu-id="4d3b2-141">本檔說明這些執行的差異（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="4d3b2-141">This documentation describes the differences between these implementations, where appropriate.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4d3b2-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d3b2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d3b2-143">**C + + 的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="4d3b2-143">**Object Model Reference for C++**</span></span>](object-model-reference-for-c.md)
</dt> <dt>

[<span data-ttu-id="4d3b2-144">**播放機控制指南**</span><span class="sxs-lookup"><span data-stu-id="4d3b2-144">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




