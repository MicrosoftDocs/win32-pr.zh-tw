---
title: 在 Web 網頁中使用 Windows Media Player 控制項
description: 在 Web 網頁中使用 Windows Media Player 控制項
ms.assetid: 70616985-86e2-48df-a9e1-89caa11b4bd1
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
- 網頁內嵌，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9cb69b2afa519091d8d729445cb87f02b9461a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183803"
---
# <a name="using-the-windows-media-player-control-in-a-web-page"></a><span data-ttu-id="4a534-115">在 Web 網頁中使用 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="4a534-115">Using the Windows Media Player Control in a Web Page</span></span>

<span data-ttu-id="4a534-116">在網頁中內嵌 Windows Media Player 控制項可讓您完全自訂使用者與控制項互動的方式。</span><span class="sxs-lookup"><span data-stu-id="4a534-116">Embedding the Windows Media Player control in a webpage lets you completely customize the way the user interacts with the control.</span></span> <span data-ttu-id="4a534-117">您可以使用控制項所提供的介面，也可以隱藏它並顯示您自己的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="4a534-117">You can use the interface provided by the control, or you can hide it and display your own user interface.</span></span> <span data-ttu-id="4a534-118">您可以在內嵌控制項的位置指定多個 Windows Media Player 控制項屬性，也可以在腳本中設定玩家屬性和呼叫 Player 方法。</span><span class="sxs-lookup"><span data-stu-id="4a534-118">You can specify multiple Windows Media Player control properties at the point where you embed the control, or you can set Player properties and call Player methods in script code.</span></span>

<span data-ttu-id="4a534-119">下列各節說明在網頁中內嵌控制項的基本概念。</span><span class="sxs-lookup"><span data-stu-id="4a534-119">The following sections describe the basics of embedding the control in a webpage.</span></span>



| <span data-ttu-id="4a534-120">區段</span><span class="sxs-lookup"><span data-stu-id="4a534-120">Section</span></span>                                                                                                        | <span data-ttu-id="4a534-121">描述</span><span class="sxs-lookup"><span data-stu-id="4a534-121">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a534-122">隱藏 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="4a534-122">Hiding the Windows Media Player Control</span></span>](hiding-the-windows-media-player-control.md)                         | <span data-ttu-id="4a534-123">描述當您想要提供您自己的使用者介面時，隱藏 Windows Media Player 控制項的選項。</span><span class="sxs-lookup"><span data-stu-id="4a534-123">Describes the options for hiding the Windows Media Player control when you want to provide your own user interface.</span></span>               |
| [<span data-ttu-id="4a534-124">OBJECT 元素中的 PARAM 元素</span><span class="sxs-lookup"><span data-stu-id="4a534-124">PARAM Elements in an OBJECT Element</span></span>](param-elements-in-an-object-element.md)                                 | <span data-ttu-id="4a534-125">描述如何在內嵌 Windows Media Player 控制項時將它初始化。</span><span class="sxs-lookup"><span data-stu-id="4a534-125">Describes how to initialize the Windows Media Player control when you embed it.</span></span>                                                   |
| [<span data-ttu-id="4a534-126">在網頁中編寫腳本的簡單範例</span><span class="sxs-lookup"><span data-stu-id="4a534-126">Simple Example of Scripting in a Web Page</span></span>](simple-example-of-scripting-in-a-web-page.md)                     | <span data-ttu-id="4a534-127">描述簡單但完整的內嵌播放機控制項與自訂使用者介面的範例。</span><span class="sxs-lookup"><span data-stu-id="4a534-127">Describes a simple, but complete, example of an embedded Player control with a custom user interface.</span></span>                             |
| [<span data-ttu-id="4a534-128">搭配 Firefox 使用 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="4a534-128">Using the Windows Media Player Control with Firefox</span></span>](using-the-windows-media-player-control-with-firefox.md) | <span data-ttu-id="4a534-129">說明如何將 Windows Media Player 控制項內嵌在網頁中，以供 Firefox 瀏覽器正確顯示。</span><span class="sxs-lookup"><span data-stu-id="4a534-129">Describes how to embed the Windows Media Player control in a webpage so that it will be displayed correctly by a Firefox browser.</span></span> |
| [<span data-ttu-id="4a534-130">使用 Windows Media Player 搭配 Netscape 7.1</span><span class="sxs-lookup"><span data-stu-id="4a534-130">Using Windows Media Player with Netscape 7.1</span></span>](using-windows-media-player-with-netscape-7-1.md)               | <span data-ttu-id="4a534-131">說明如何搭配使用 Windows Media Player 控制項與 Netscape 7.1 和其他以 Gecko 為基礎的網頁瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="4a534-131">Describes how to use the Windows Media Player control with Netscape 7.1 and other Gecko-based Web browsers.</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="4a534-132">Windows Media Player 10 行動裝置版控制項包含的功能，是以 Windows Media Player 控制項的桌上出版本提供的功能子集為基礎。</span><span class="sxs-lookup"><span data-stu-id="4a534-132">The Windows Media Player 10 Mobile control contains functionality based on a subset of the functionality provided in the desktop version of the Windows Media Player control.</span></span> <span data-ttu-id="4a534-133">因此，它可以內嵌于 Pocket Internet Explorer 網頁，就像桌面控制項內嵌在 Internet Explorer 網頁中一樣。</span><span class="sxs-lookup"><span data-stu-id="4a534-133">Therefore, it can be embedded in a Pocket Internet Explorer webpage the same way the desktop control is embedded in an Internet Explorer webpage.</span></span> <span data-ttu-id="4a534-134">若要瞭解 Windows Media Player 10 個行動控制項是否支援特定的方法、屬性或事件，請參閱 [腳本的物件模型參考](object-model-reference-for-scripting.md)。</span><span class="sxs-lookup"><span data-stu-id="4a534-134">To find out whether a particular method, property, or event is supported for the Windows Media Player 10 Mobile control, see [Object Model Reference for Scripting](object-model-reference-for-scripting.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4a534-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a534-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a534-136">**播放機控制指南**</span><span class="sxs-lookup"><span data-stu-id="4a534-136">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




