---
title: 關於 Player 物件模型
description: 關於 Player 物件模型
ms.assetid: 41a9cbce-b982-4377-a0ee-b0ca735954f5
keywords:
- Windows Media Player，物件模型
- Windows Media Player 物件模型，關於
- 物件模型，關於
- Windows Media Player ActiveX 控制項，物件模型
- ActiveX 控制項，物件模型
- Windows Media Player Mobile ActiveX 控制項，物件模型
- Windows Media Player 行動裝置，物件模型
- 軟體發展工具組 (SDK) ，Windows Media Player ActiveX 控制項物件模型
- SDK (軟體發展工具組) ，Windows Media Player ActiveX 控制項物件模型
- 檔，Windows Media Player ActiveX 控制項物件模型
- Player 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a0ded1f25d8d08bd9e588b5384a171698d2ea2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968427"
---
# <a name="about-the-player-object-model"></a><span data-ttu-id="68236-114">關於 Player 物件模型</span><span class="sxs-lookup"><span data-stu-id="68236-114">About the Player Object Model</span></span>

<span data-ttu-id="68236-115">Microsoft Windows Media Player 控制項是一種標準的 ActiveX 控制項，使用 Microsoft 元件物件模型 (COM) 技術。</span><span class="sxs-lookup"><span data-stu-id="68236-115">The Microsoft Windows Media Player control is a standard ActiveX control that uses Microsoft Component Object Model (COM) technology.</span></span> <span data-ttu-id="68236-116">Windows Media Player 的功能會在一組遵循標準 COM 指導方針的程式設計介面中。</span><span class="sxs-lookup"><span data-stu-id="68236-116">The Windows Media Player functionality is distilled into a set of programming interfaces that follows standard COM guidelines.</span></span> <span data-ttu-id="68236-117">您可以使用 Player 控制項物件模型搭配 Microsoft JScript 或 Microsoft Visual Basic Scripting Edition (VBScript) ，在標準的 HTML 網頁上撰寫這些介面的程式。</span><span class="sxs-lookup"><span data-stu-id="68236-117">You can program these interfaces on a standard HTML webpage using the Player control object model with Microsoft JScript or Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="68236-118">您也可以使用 Microsoft JScript 在面板中進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="68236-118">You can also program them in skins by using Microsoft JScript.</span></span> <span data-ttu-id="68236-119">如果您想要建立內嵌控制項的自訂程式，您可以使用數種語言的其中一種，包括 Visual Basic、c + + 和 c #。</span><span class="sxs-lookup"><span data-stu-id="68236-119">If you want to create a custom program that embeds the control, you can use one of several languages, including Visual Basic, C++, and C#.</span></span>

<span data-ttu-id="68236-120">Windows Media Player 的 ActiveX 控制項與 Windows Media Player 一起安裝。</span><span class="sxs-lookup"><span data-stu-id="68236-120">The Windows Media Player ActiveX control is installed with Windows Media Player.</span></span> <span data-ttu-id="68236-121">播放機控制項不會隨 Windows Media Player SDK 一起安裝，也不能另外再散發。</span><span class="sxs-lookup"><span data-stu-id="68236-121">The Player control is not installed with the Windows Media Player SDK and cannot be redistributed separately.</span></span> <span data-ttu-id="68236-122">您的程式碼可用的特定功能，取決於使用者所安裝的 Windows Media Player 版本。</span><span class="sxs-lookup"><span data-stu-id="68236-122">The particular features available to your code depend on which version of Windows Media Player the user has installed.</span></span> <span data-ttu-id="68236-123">[C + + 的腳本和物件模型參考](object-model-reference-for-c.md)的[物件模型參考](object-model-reference-for-scripting.md)包含每個屬性、方法和事件的版本需求資訊。</span><span class="sxs-lookup"><span data-stu-id="68236-123">The [Object Model Reference for Scripting](object-model-reference-for-scripting.md) and [Object Model Reference for C++](object-model-reference-for-c.md) include version requirement information for each property, method, and event.</span></span>

<span data-ttu-id="68236-124">下列各節提供有關 Windows Media Player 物件模型的總覽資訊。</span><span class="sxs-lookup"><span data-stu-id="68236-124">The following sections provide overview information about the Windows Media Player object model.</span></span>



| <span data-ttu-id="68236-125">區段</span><span class="sxs-lookup"><span data-stu-id="68236-125">Section</span></span>                                                                                        | <span data-ttu-id="68236-126">描述</span><span class="sxs-lookup"><span data-stu-id="68236-126">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68236-127">指令碼語言的播放程式物件模型</span><span class="sxs-lookup"><span data-stu-id="68236-127">Player Object Model for Scripting Languages</span></span>](player-object-model-for-scripting-languages.md) | <span data-ttu-id="68236-128">本節說明物件模型中可用的物件。</span><span class="sxs-lookup"><span data-stu-id="68236-128">This section describes the objects available in the object model.</span></span>                                                                                             |
| [<span data-ttu-id="68236-129">關於物件模型版本</span><span class="sxs-lookup"><span data-stu-id="68236-129">About the Object Model Versions</span></span>](about-the-object-model-versions.md)                         | <span data-ttu-id="68236-130">本節詳細說明自 Windows Media Player 7.0 推出之後，每個版本中已加入的物件模型專案。</span><span class="sxs-lookup"><span data-stu-id="68236-130">This section details which object model items have been added in each version since the introduction of Windows Media Player 7.0.</span></span>                             |
| [<span data-ttu-id="68236-131">屬性、方法和事件</span><span class="sxs-lookup"><span data-stu-id="68236-131">Properties, Methods, and Events</span></span>](properties--methods-and-events.md)                          | <span data-ttu-id="68236-132">本節說明屬性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="68236-132">This section explains properties, methods, and events.</span></span>                                                                                                        |
| [<span data-ttu-id="68236-133">支援的通訊協定和檔案類型</span><span class="sxs-lookup"><span data-stu-id="68236-133">Supported Protocols and File Types</span></span>](supported-protocols-and-file-types.md)                   | <span data-ttu-id="68236-134">本節列出 Windows Media Player 和 Windows Media Player control 物件模型所支援的通訊協定和檔案類型。</span><span class="sxs-lookup"><span data-stu-id="68236-134">This section lists the protocols and file types supported by Windows Media Player and the Windows Media Player control object model.</span></span>                          |
| [<span data-ttu-id="68236-135">關於程式庫</span><span class="sxs-lookup"><span data-stu-id="68236-135">About the Library</span></span>](about-the-library.md)                                                     | <span data-ttu-id="68236-136">本節說明 Windows Media Player 程式庫。</span><span class="sxs-lookup"><span data-stu-id="68236-136">This section describes the Windows Media Player library.</span></span>                                                                                                      |
| [<span data-ttu-id="68236-137">使用 HTML 搭配 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="68236-137">Using HTML with Windows Media Player</span></span>](using-html-with-windows-media-player.md)               | <span data-ttu-id="68236-138">本節說明讓 Windows Media Player 和 HTML 一起運作的各種方式。</span><span class="sxs-lookup"><span data-stu-id="68236-138">This section describes the various ways to make Windows Media Player and HTML work together.</span></span>                                                                  |
| [<span data-ttu-id="68236-139">內嵌 Windows Media Player 控制項</span><span class="sxs-lookup"><span data-stu-id="68236-139">Embedding the Windows Media Player Control</span></span>](embedding-the-windows-media-player-control.md)   | <span data-ttu-id="68236-140">本節說明在 Microsoft Office 檔和自訂程式中內嵌 Windows Media Player 控制項的各種方式。</span><span class="sxs-lookup"><span data-stu-id="68236-140">This section describes the various ways to embed the Windows Media Player control in Microsoft Office documents and in custom programs.</span></span>                       |
| [<span data-ttu-id="68236-141">關於裝置同步處理</span><span class="sxs-lookup"><span data-stu-id="68236-141">About Device Synchronization</span></span>](about-device-synchronization.md)                               | <span data-ttu-id="68236-142">本節說明將數位媒體內容傳輸至可攜式裝置的 Windows Media Player 10 或更新版本控制項所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="68236-142">This section describes the functionality provided by the Windows Media Player 10 or later control for transferring digital media content to portable devices.</span></span> |
| [<span data-ttu-id="68236-143">關於 CD 燒錄</span><span class="sxs-lookup"><span data-stu-id="68236-143">About CD Burning</span></span>](about-cd-burning.md)                                                       | <span data-ttu-id="68236-144">本節說明用來建立 Cd 的 Windows Media Player 控制項所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="68236-144">This section describes the functionality provided by the Windows Media Player control for creating CDs.</span></span>                                                       |
| [<span data-ttu-id="68236-145">關於 CD 翻錄</span><span class="sxs-lookup"><span data-stu-id="68236-145">About CD Ripping</span></span>](about-cd-ripping.md)                                                       | <span data-ttu-id="68236-146">本節說明 Windows Media Player 控制項所提供的功能，可將曲目從音訊 Cd 複製到使用者的電腦。</span><span class="sxs-lookup"><span data-stu-id="68236-146">This section describes the functionality provided by the Windows Media Player control for copying tracks from audio CDs to the user's computer.</span></span>               |
| [<span data-ttu-id="68236-147">關於資料夾監控</span><span class="sxs-lookup"><span data-stu-id="68236-147">About Folder Monitoring</span></span>](about-folder-monitoring.md)                                         | <span data-ttu-id="68236-148">本節說明用來控制播放程式資料夾監控進程的 Windows Media Player 控制項所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="68236-148">This section describes the functionality provided by the Windows Media Player control for controlling the Player's folder monitoring processes.</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="68236-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="68236-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68236-150">**Windows Media Player 物件模型**</span><span class="sxs-lookup"><span data-stu-id="68236-150">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 




