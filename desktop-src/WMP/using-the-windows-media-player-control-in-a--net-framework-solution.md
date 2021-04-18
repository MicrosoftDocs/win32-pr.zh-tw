---
title: 在 .NET Framework 方案中使用 Windows Media Player 控制項
description: 在 .NET Framework 方案中使用 Windows Media Player 控制項
ms.assetid: f1cc2ef0-a341-402f-bf7c-2ba07eea1f6a
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
- .NET Framework，關於內嵌 ActiveX 控制項
- 內嵌、.NET Framework 方案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0e6b09474c9340733cf45fb7c49a57100a1b11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965592"
---
# <a name="using-the-windows-media-player-control-in-a-net-framework-solution"></a><span data-ttu-id="3713b-119">在 .NET Framework 方案中使用 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="3713b-119">Using the Windows Media Player Control in a .NET Framework Solution</span></span>

<span data-ttu-id="3713b-120">Windows Media Player 9 系列或更新版本的 ActiveX 控制項支援在 .NET Framework 應用程式中內嵌。</span><span class="sxs-lookup"><span data-stu-id="3713b-120">The Windows Media Player 9 Series or later ActiveX control supports embedding in .NET Framework applications.</span></span> <span data-ttu-id="3713b-121">下列各節提供使用 Windows Media Player 控制項搭配 .NET Framework 的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="3713b-121">The following sections provide information specific to using the Windows Media Player control with the .NET Framework.</span></span>



| <span data-ttu-id="3713b-122">區段</span><span class="sxs-lookup"><span data-stu-id="3713b-122">Section</span></span>                                                                                                                                                      | <span data-ttu-id="3713b-123">描述</span><span class="sxs-lookup"><span data-stu-id="3713b-123">Description</span></span>                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3713b-124">使用 Windows Media Player 控制項搭配 Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3713b-124">Using the Windows Media Player Control with Microsoft Visual Studio</span></span>](using-the-windows-media-player-control-with-microsoft-visual-studio.md)               | <span data-ttu-id="3713b-125">提供有關將 Windows Media Player 9 系列或更新版本的控制項新增至 Visual Studio 方案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3713b-125">Provides details about adding the Windows Media Player 9 Series or later control to a Visual Studio solution.</span></span>                |
| [<span data-ttu-id="3713b-126">在 c # 方案中內嵌 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="3713b-126">Embedding the Windows Media Player Control in a C# Solution</span></span>](embedding-the-windows-media-player-control-in-a-c--solution.md)                              | <span data-ttu-id="3713b-127">提供建立使用 Windows Media Player 控制項之簡單 c # 應用程式的指示。</span><span class="sxs-lookup"><span data-stu-id="3713b-127">Provides instructions for creating a simple C# application that uses the Windows Media Player control.</span></span>                      |
| [<span data-ttu-id="3713b-128">在 Visual Basic .NET 方案中內嵌 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="3713b-128">Embedding the Windows Media Player Control in a Visual Basic .NET Solution</span></span>](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md) | <span data-ttu-id="3713b-129">提供如何建立使用 Windows Media Player 控制項之簡單 Visual Basic .NET 應用程式的指示。</span><span class="sxs-lookup"><span data-stu-id="3713b-129">Provides instructions for creating a simple Visual Basic .NET application that uses the Windows Media Player control.</span></span>        |
| [<span data-ttu-id="3713b-130">以程式設計方式建立 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="3713b-130">Creating the Windows Media Player Control Programmatically</span></span>](creating-the-windows-media-player-control-programmatically.md)                                 | <span data-ttu-id="3713b-131">描述如何在不使用 Visual Studio 工具箱的情況下，在應用程式中建立 Windows Media Player 控制項。</span><span class="sxs-lookup"><span data-stu-id="3713b-131">Describes how to create a Windows Media Player control in an application without using the Visual Studio Toolbox.</span></span>            |
| [<span data-ttu-id="3713b-132">關於 .NET Framework 資料類型</span><span class="sxs-lookup"><span data-stu-id="3713b-132">About .NET Framework Data Types</span></span>](about--net-framework-data-types.md)                                                                                       | <span data-ttu-id="3713b-133">提供將腳本導向的物件模型參考轉譯成 .NET Framework 基底資料類型所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="3713b-133">Provides the information needed to translate the script-oriented Object Model Reference into .NET Framework base data types.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3713b-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="3713b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3713b-135">**播放機控制指南**</span><span class="sxs-lookup"><span data-stu-id="3713b-135">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




