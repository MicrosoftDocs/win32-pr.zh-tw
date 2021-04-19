---
title: 在 Firefox 所顯示的網頁中使用腳本
description: 在 Firefox 所顯示的網頁中使用腳本
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
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
- Windows Media Player ActiveX 控制項，腳本範例
- Windows Media Player Mobile ActiveX 控制項，腳本範例
- ActiveX 控制項，腳本範例
- 內嵌、網頁
- 網頁內嵌、腳本範例
- Windows Media Player，Firefox
- Windows Media Player 物件模型，Firefox
- 物件模型，Firefox
- Windows Media Player Mobile、Firefox
- Windows Media Player ActiveX 控制項，Firefox
- Windows Media Player Mobile ActiveX 控制項，Firefox
- ActiveX 控制項、Firefox
- Firefox，腳本範例
- 網頁內嵌、Firefox
- 網頁內嵌的腳本範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8629f87f954d12602999f76483fdd36ab279290
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "106967856"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="0ad82-128">在 Firefox 所顯示的網頁中使用腳本</span><span class="sxs-lookup"><span data-stu-id="0ad82-128">Using Script in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="0ad82-129">當使用者與頁面互動時，網頁上的腳本可以使用 Player 物件模型來控制播放機。</span><span class="sxs-lookup"><span data-stu-id="0ad82-129">Script on a webpage can use the Player object model to control the Player as the user interacts with the page.</span></span> <span data-ttu-id="0ad82-130">例如，下列輸入專案具有可設定播放程式音量的腳本。</span><span class="sxs-lookup"><span data-stu-id="0ad82-130">For example, the following INPUT element has script that sets the Player volume.</span></span>


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



<span data-ttu-id="0ad82-131">Windows Media Player 物件模型中的許多物件都受到 Internet Explorer 和 Firefox 外掛程式的支援。</span><span class="sxs-lookup"><span data-stu-id="0ad82-131">Many of the objects in the Windows Media Player object model are supported by Internet Explorer and by the Firefox plug-in.</span></span> <span data-ttu-id="0ad82-132">不過，Firefox 外掛程式不支援某些物件。</span><span class="sxs-lookup"><span data-stu-id="0ad82-132">However, there are some objects that are not supported by the Firefox plug-in.</span></span> <span data-ttu-id="0ad82-133">下表列出 Player 物件模型中的所有物件，並顯示 Firefox 外掛程式支援的物件。</span><span class="sxs-lookup"><span data-stu-id="0ad82-133">The following table lists all of the objects in the Player object model and shows which objects are supported by the Firefox plug-in.</span></span>



| <span data-ttu-id="0ad82-134">Object</span><span class="sxs-lookup"><span data-stu-id="0ad82-134">Object</span></span>                                              | <span data-ttu-id="0ad82-135">Firefox 支援</span><span class="sxs-lookup"><span data-stu-id="0ad82-135">Firefox support</span></span> |
|-----------------------------------------------------|-----------------|
| [<span data-ttu-id="0ad82-136">光碟</span><span class="sxs-lookup"><span data-stu-id="0ad82-136">Cdrom</span></span>](cdrom-object.md)                           | <span data-ttu-id="0ad82-137">不可以</span><span class="sxs-lookup"><span data-stu-id="0ad82-137">no</span></span>              |
| [<span data-ttu-id="0ad82-138">CdromCollection</span><span class="sxs-lookup"><span data-stu-id="0ad82-138">CdromCollection</span></span>](cdromcollection-object.md)       | <span data-ttu-id="0ad82-139">不可以</span><span class="sxs-lookup"><span data-stu-id="0ad82-139">no</span></span>              |
| [<span data-ttu-id="0ad82-140">ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="0ad82-140">ClosedCaption</span></span>](closedcaption-object.md)           | <span data-ttu-id="0ad82-141">是</span><span class="sxs-lookup"><span data-stu-id="0ad82-141">yes</span></span>             |
| [<span data-ttu-id="0ad82-142">控制項</span><span class="sxs-lookup"><span data-stu-id="0ad82-142">Controls</span></span>](controls-object.md)                     | <span data-ttu-id="0ad82-143">不可以</span><span class="sxs-lookup"><span data-stu-id="0ad82-143">no</span></span>              |
| [<span data-ttu-id="0ad82-144">Dvd</span><span class="sxs-lookup"><span data-stu-id="0ad82-144">DVD</span></span>](dvd-object.md)                               | <span data-ttu-id="0ad82-145">不可以</span><span class="sxs-lookup"><span data-stu-id="0ad82-145">no</span></span>              |
| [<span data-ttu-id="0ad82-146">錯誤</span><span class="sxs-lookup"><span data-stu-id="0ad82-146">Error</span></span>](error-object.md)                           | <span data-ttu-id="0ad82-147">是</span><span class="sxs-lookup"><span data-stu-id="0ad82-147">yes</span></span>             |
| [<span data-ttu-id="0ad82-148">ErrorItem</span><span class="sxs-lookup"><span data-stu-id="0ad82-148">ErrorItem</span></span>](erroritem-object.md)                   | <span data-ttu-id="0ad82-149">是</span><span class="sxs-lookup"><span data-stu-id="0ad82-149">yes</span></span>             |
| [<span data-ttu-id="0ad82-150">媒體</span><span class="sxs-lookup"><span data-stu-id="0ad82-150">Media</span></span>](media-object.md)                           | <span data-ttu-id="0ad82-151">是</span><span class="sxs-lookup"><span data-stu-id="0ad82-151">yes</span></span>             |
| [<span data-ttu-id="0ad82-152">MediaCollection</span><span class="sxs-lookup"><span data-stu-id="0ad82-152">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="0ad82-153">不可以</span><span class="sxs-lookup"><span data-stu-id="0ad82-153">no</span></span>              |
| [<span data-ttu-id="0ad82-154">MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="0ad82-154">MetadataPicture</span></span>](metadatapicture-object.md)       | <span data-ttu-id="0ad82-155">不可以</span><span class="sxs-lookup"><span data-stu-id="0ad82-155">no</span></span>              |
| [<span data-ttu-id="0ad82-156">MetadataText</span><span class="sxs-lookup"><span data-stu-id="0ad82-156">MetadataText</span></span>](metadatatext-object.md)             | <span data-ttu-id="0ad82-157">不可以</span><span class="sxs-lookup"><span data-stu-id="0ad82-157">no</span></span>              |
| [<span data-ttu-id="0ad82-158">Network</span><span class="sxs-lookup"><span data-stu-id="0ad82-158">Network</span></span>](network-object.md)                       | <span data-ttu-id="0ad82-159">是</span><span class="sxs-lookup"><span data-stu-id="0ad82-159">yes</span></span>             |
| [<span data-ttu-id="0ad82-160">球員</span><span class="sxs-lookup"><span data-stu-id="0ad82-160">Player</span></span>](player-object.md)                         | <span data-ttu-id="0ad82-161">是</span><span class="sxs-lookup"><span data-stu-id="0ad82-161">yes</span></span>             |
| [<span data-ttu-id="0ad82-162">PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="0ad82-162">PlayerApplication</span></span>](playerapplication-object.md)   | <span data-ttu-id="0ad82-163">不可以</span><span class="sxs-lookup"><span data-stu-id="0ad82-163">no</span></span>              |
| [<span data-ttu-id="0ad82-164">播放 清單</span><span class="sxs-lookup"><span data-stu-id="0ad82-164">Playlist</span></span>](playlist-object.md)                     | <span data-ttu-id="0ad82-165">是</span><span class="sxs-lookup"><span data-stu-id="0ad82-165">yes</span></span>             |
| [<span data-ttu-id="0ad82-166">PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="0ad82-166">PlaylistArray</span></span>](playlistarray-object.md)           | <span data-ttu-id="0ad82-167">不可以</span><span class="sxs-lookup"><span data-stu-id="0ad82-167">no</span></span>              |
| [<span data-ttu-id="0ad82-168">PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="0ad82-168">PlaylistCollection</span></span>](playlistcollection-object.md) | <span data-ttu-id="0ad82-169">不可以</span><span class="sxs-lookup"><span data-stu-id="0ad82-169">no</span></span>              |
| [<span data-ttu-id="0ad82-170">查詢</span><span class="sxs-lookup"><span data-stu-id="0ad82-170">Query</span></span>](query-object.md)                           | <span data-ttu-id="0ad82-171">不可以</span><span class="sxs-lookup"><span data-stu-id="0ad82-171">no</span></span>              |
| [<span data-ttu-id="0ad82-172">設定</span><span class="sxs-lookup"><span data-stu-id="0ad82-172">Settings</span></span>](settings-object.md)                     | <span data-ttu-id="0ad82-173">是</span><span class="sxs-lookup"><span data-stu-id="0ad82-173">yes</span></span>             |
| [<span data-ttu-id="0ad82-174">StringCollection</span><span class="sxs-lookup"><span data-stu-id="0ad82-174">StringCollection</span></span>](stringcollection-object.md)     | <span data-ttu-id="0ad82-175">不可以</span><span class="sxs-lookup"><span data-stu-id="0ad82-175">no</span></span>              |



 

<span data-ttu-id="0ad82-176">Firefox 外掛程式支援 **player** 物件，但是 **player** 物件的某些屬性會在 Firefox 瀏覽器中傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0ad82-176">The Firefox plug-in supports the **Player** object, but certain properties of the **Player** object return **NULL** in a Firefox browser.</span></span> <span data-ttu-id="0ad82-177">例如， **Player** 物件的 [cdromCollection](player-cdromcollection.md)屬性會傳回 **Null** ，因為 Firefox 外掛程式不支援 **Cdrom** 物件。</span><span class="sxs-lookup"><span data-stu-id="0ad82-177">For example, the [cdromCollection](player-cdromcollection.md) property of the **Player** object returns **NULL** because the Firefox plug-in does not support the **Cdrom** object.</span></span> <span data-ttu-id="0ad82-178">同樣地，在 Firefox 瀏覽器中， **Player** 物件的 [dvd](player-dvd.md)、 [mediaCollection](player-mediacollection.md)、 [playerApplication](player-playerapplication.md)和 [playlistCollection](player-playlistcollection.md)屬性會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0ad82-178">Similarly, the [dvd](player-dvd.md), [mediaCollection](player-mediacollection.md), [playerApplication](player-playerapplication.md), and [playlistCollection](player-playlistcollection.md) properties of the **Player** object return **NULL** in a Firefox browser.</span></span>

<span data-ttu-id="0ad82-179">**PluginVersionInfo** 屬性受到 Firefox 外掛程式的支援，但不受 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="0ad82-179">The **Player.pluginVersionInfo** property is supported by the Firefox plug-in but not by Internet Explorer.</span></span> <span data-ttu-id="0ad82-180">這個屬性會傳回 Firefox 外掛程式的版本。</span><span class="sxs-lookup"><span data-stu-id="0ad82-180">This property returns the version of the Firefox plug-in.</span></span>

<span data-ttu-id="0ad82-181">Firefox 外掛程式支援 **媒體** 物件，包括 [getItemInfoByType](media-getiteminfobytype.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="0ad82-181">The Firefox plug-in supports the **Media** object, including the [getItemInfoByType](media-getiteminfobytype.md) property.</span></span> <span data-ttu-id="0ad82-182">不過，在 Firefox 瀏覽器中， **getItemInfoByType** 屬性不支援 **MetadataText** 和 **MetadataPicture** 傳回型別。</span><span class="sxs-lookup"><span data-stu-id="0ad82-182">However, in a Firefox browser, the **getItemInfoByType** property does not support the **MetadataText** and **MetadataPicture** return types.</span></span>

<span data-ttu-id="0ad82-183">Firefox 外掛程式除了[setMode](settings-setmode.md)方法和[requestMediaAccessRights](settings-requestmediaaccessrights.md)屬性之外，還支援[Settings](settings-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="0ad82-183">The Firefox plug-in supports the [Settings](settings-object.md) object except for the [setMode](settings-setmode.md) method and the [requestMediaAccessRights](settings-requestmediaaccessrights.md) property.</span></span> <span data-ttu-id="0ad82-184">在 Firefox 瀏覽器中， **requestMediaAccessRight** 屬性一律會傳回 false。</span><span class="sxs-lookup"><span data-stu-id="0ad82-184">In a Firefox browser, the **requestMediaAccessRight** property always returns false.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ad82-185">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ad82-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ad82-186">**搭配 Firefox 使用 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="0ad82-186">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




