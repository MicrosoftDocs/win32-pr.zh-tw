---
title: 指令碼語言的播放程式物件模型
description: 指令碼語言的播放程式物件模型
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
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
- Windows Media Player，指令碼語言
- Windows Media Player 物件模型，指令碼語言
- 物件模型，指令碼語言
- Windows Media Player ActiveX 控制項，指令碼語言
- ActiveX 控制項，指令碼語言
- Windows Media Player 的行動 ActiveX 控制項、指令碼語言
- Windows Media Player 行動裝置、指令碼語言
- 指令碼語言
- Windows Media Player，Player 物件
- Windows Media Player 物件模型、Player 物件
- 物件模型、Player 物件
- Windows Media Player ActiveX 控制項、Player 物件
- ActiveX 控制項、Player 物件
- Windows Media Player Mobile ActiveX 控制項、Player 物件
- Windows Media Player Mobile，Player 物件
- Player 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670bff03075fd98812dbee269115e297a137e92d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104553054"
---
# <a name="player-object-model-for-scripting-languages"></a><span data-ttu-id="e1a24-129">指令碼語言的播放程式物件模型</span><span class="sxs-lookup"><span data-stu-id="e1a24-129">Player Object Model for Scripting Languages</span></span>

<span data-ttu-id="e1a24-130">ActiveX 使用物件的概念來包含程式設計功能。</span><span class="sxs-lookup"><span data-stu-id="e1a24-130">ActiveX uses the concept of objects to contain programming functionality.</span></span> <span data-ttu-id="e1a24-131">Windows Media Player 會使用數個物件來分割控制項所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="e1a24-131">Windows Media Player uses several objects to divide up the functionality the control provides.</span></span> <span data-ttu-id="e1a24-132">根物件是 **player** 物件，而其他物件則是透過特定屬性附加至 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="e1a24-132">The root object is the **Player** object, and the other objects are attached to the **Player** object through specific properties.</span></span>

<span data-ttu-id="e1a24-133">下圖顯示 Windows Media Player 11 ActiveX 控制項物件模型在指令碼語言中的運作方式。</span><span class="sxs-lookup"><span data-stu-id="e1a24-133">The following diagram shows how the Windows Media Player 11 ActiveX control object model works for scripting languages.</span></span>

![windows media player 11 物件模型的圖表](images/playeromdiag.png)

<span data-ttu-id="e1a24-135">在 c + + 中，有時也是在 .NET 語言中，物件是由 COM 介面表示。</span><span class="sxs-lookup"><span data-stu-id="e1a24-135">In C++, and sometimes in .NET languages, objects are represented by COM interfaces.</span></span> <span data-ttu-id="e1a24-136">在 Windows Media Player 物件模型中，COM 介面名稱與物件名稱相同，但前面會加上 "IWMP"。</span><span class="sxs-lookup"><span data-stu-id="e1a24-136">In the Windows Media Player object model, COM interface names are the same as the object name, but are prefixed with "IWMP".</span></span> <span data-ttu-id="e1a24-137">例如，透過 **IWMPNetwork** 介面公開 **網路** 物件。</span><span class="sxs-lookup"><span data-stu-id="e1a24-137">For example, the **Network** object is exposed through the **IWMPNetwork** interface.</span></span>

<span data-ttu-id="e1a24-138">下列各節提供每個物件的概念總覽：</span><span class="sxs-lookup"><span data-stu-id="e1a24-138">The following sections provide conceptual overviews for each object:</span></span>

-   [<span data-ttu-id="e1a24-139">關於 Cdrom 和 CdromCollection 物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-139">About the Cdrom and CdromCollection Objects</span></span>](about-the-cdrom-and-cdromcollection-objects.md)
-   [<span data-ttu-id="e1a24-140">關於 ClosedCaption 物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-140">About the ClosedCaption Object</span></span>](about-the-closedcaption-object.md)
-   [<span data-ttu-id="e1a24-141">關於控制項物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-141">About the Controls Object</span></span>](about-the-controls-object.md)
-   [<span data-ttu-id="e1a24-142">關於 DVD 物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-142">About the DVD Object</span></span>](about-the-dvd-object.md)
-   [<span data-ttu-id="e1a24-143">關於 Error 和 ErrorItem 物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-143">About the Error and ErrorItem Objects</span></span>](about-the-error-and-erroritem-objects.md)
-   [<span data-ttu-id="e1a24-144">關於 MediaCollection 和 Media 物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-144">About the MediaCollection and Media Objects</span></span>](about-the-mediacollection-and-media-objects.md)
-   [<span data-ttu-id="e1a24-145">關於 MetadataPicture 物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-145">About the MetadataPicture Object</span></span>](about-the-metadatapicture-object.md)
-   [<span data-ttu-id="e1a24-146">關於 MetadataText 物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-146">About the MetadataText Object</span></span>](about-the-metadatatext-object.md)
-   [<span data-ttu-id="e1a24-147">關於 Network 物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-147">About the Network Object</span></span>](about-the-network-object.md)
-   [<span data-ttu-id="e1a24-148">關於 Player 物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-148">About the Player Object</span></span>](about-the-player-object.md)
-   [<span data-ttu-id="e1a24-149">關於 PlayerApplication 物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-149">About the PlayerApplication Object</span></span>](about-the-playerapplication-object.md)
-   [<span data-ttu-id="e1a24-150">關於播放清單、PlaylistCollection 和 PlaylistArray 物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-150">About the Playlist, PlaylistCollection, and PlaylistArray Objects</span></span>](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [<span data-ttu-id="e1a24-151">關於 Query 物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-151">About the Query Object</span></span>](about-the-query-object.md)
-   [<span data-ttu-id="e1a24-152">關於 Settings 物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-152">About the Settings Object</span></span>](about-the-settings-object.md)
-   [<span data-ttu-id="e1a24-153">關於 StringCollection 物件</span><span class="sxs-lookup"><span data-stu-id="e1a24-153">About the StringCollection Object</span></span>](about-the-stringcollection-object.md)

<span data-ttu-id="e1a24-154">您可以透過特定的 COM 介面取得額外的功能。</span><span class="sxs-lookup"><span data-stu-id="e1a24-154">Additional functionality is available through certain COM interfaces.</span></span> <span data-ttu-id="e1a24-155">您是否可以存取這些介面，可能取決於您用於程式設計的語言和其他因素，例如用來建立 Windows Media Player 控制項實例的模式。</span><span class="sxs-lookup"><span data-stu-id="e1a24-155">Whether you can access these interfaces may depend on the language you use for programming and other factors, such as the mode used to create the instance of the Windows Media Player control.</span></span> <span data-ttu-id="e1a24-156">如需 Windows Media Player 控制項公開的 COM 介面完整清單，請參閱 [c + + 的物件模型參考](object-model-reference-for-c.md)。</span><span class="sxs-lookup"><span data-stu-id="e1a24-156">For a complete list of COM interfaces exposed by the Windows Media Player control, see the [Object Model Reference for C++](object-model-reference-for-c.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1a24-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1a24-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1a24-158">**關於 Player 物件模型**</span><span class="sxs-lookup"><span data-stu-id="e1a24-158">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="e1a24-159">**在 .NET Framework 方案中使用 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="e1a24-159">**Using the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




