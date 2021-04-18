---
title: 腳本的物件模型參考
description: 腳本的物件模型參考
ms.assetid: a900fd55-2213-46db-84ad-93f199c60182
keywords:
- Windows Media Player，物件模型
- Windows Media Player 行動裝置，物件模型
- Windows Media Player 物件模型，參考
- 物件模型，參考
- ActiveX 控制項，參考
- Windows Media Player ActiveX 控制項，參考
- Windows Media Player Mobile ActiveX 控制項，參考
- 物件模型的參考，腳本
- Windows Media Player，腳本參考
- Windows Media Player 行動版、腳本參考
- Windows Media Player 物件模型，腳本參考
- 物件模型，腳本參考
- Windows Media Player ActiveX 控制項，腳本參考
- Windows Media Player 的行動 ActiveX 控制項，腳本參考
- ActiveX 控制項，腳本參考
- 腳本物件模型參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f20e5bacf6a1fd93579ce40e8957b7ce7aefae0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969062"
---
# <a name="object-model-reference-for-scripting"></a><span data-ttu-id="2b05b-119">腳本的物件模型參考</span><span class="sxs-lookup"><span data-stu-id="2b05b-119">Object Model Reference for Scripting</span></span>

<span data-ttu-id="2b05b-120">腳本的物件模型參考包含 Windows Media Player ActiveX 控制項物件模型的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2b05b-120">The object model reference for scripting contains detailed information about the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="2b05b-121">本節中的資訊是以設計來搭配 Microsoft JScript 之類的指令碼語言使用的樣式來呈現。</span><span class="sxs-lookup"><span data-stu-id="2b05b-121">The information in this section is presented in a style designed for use with script languages like Microsoft JScript.</span></span>

> [!Note]  
> <span data-ttu-id="2b05b-122">除非另行明確陳述，否則 Windows Media Player 10 行動版或更新版本中完全支援所有方法、屬性和事件。</span><span class="sxs-lookup"><span data-stu-id="2b05b-122">All methods, properties, and events are fully supported in Windows Media Player 10 Mobile or later unless explicitly stated otherwise.</span></span>

 

<span data-ttu-id="2b05b-123">腳本的物件模型參考包含下列物件及其相關聯方法、屬性和事件的檔。</span><span class="sxs-lookup"><span data-stu-id="2b05b-123">The object model reference for scripting contains documentation for the following objects and their associated methods, properties, and events.</span></span>



| <span data-ttu-id="2b05b-124">Object</span><span class="sxs-lookup"><span data-stu-id="2b05b-124">Object</span></span>                                              | <span data-ttu-id="2b05b-125">描述</span><span class="sxs-lookup"><span data-stu-id="2b05b-125">Description</span></span>                                                                                                                                                                                    |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b05b-126">光碟</span><span class="sxs-lookup"><span data-stu-id="2b05b-126">Cdrom</span></span>](cdrom-object.md)                           | <span data-ttu-id="2b05b-127">用來存取磁片磁碟機中 CD 或 DVD 的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="2b05b-127">Methods and properties for accessing a CD or DVD in its drive.</span></span>                                                                                                                                 |
| [<span data-ttu-id="2b05b-128">CdromCollection</span><span class="sxs-lookup"><span data-stu-id="2b05b-128">CdromCollection</span></span>](cdromcollection-object.md)       | <span data-ttu-id="2b05b-129">用來存取 CD 或 DVD 光碟機集合的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="2b05b-129">Methods and properties for accessing a collection of CD or DVD drives.</span></span>                                                                                                                         |
| [<span data-ttu-id="2b05b-130">ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="2b05b-130">ClosedCaption</span></span>](closedcaption-object.md)           | <span data-ttu-id="2b05b-131">包含具有媒體專案之標題的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b05b-131">Properties for including captions with a media item.</span></span>                                                                                                                                           |
| [<span data-ttu-id="2b05b-132">控制項</span><span class="sxs-lookup"><span data-stu-id="2b05b-132">Controls</span></span>](controls-object.md)                     | <span data-ttu-id="2b05b-133">代表 Windows Media Player 之傳輸控制項的方法和屬性，例如播放、停止和暫停。</span><span class="sxs-lookup"><span data-stu-id="2b05b-133">Methods and properties representing the transport controls of Windows Media Player, such as Play, Stop, and Pause.</span></span>                                                                             |
| [<span data-ttu-id="2b05b-134">Dvd</span><span class="sxs-lookup"><span data-stu-id="2b05b-134">DVD</span></span>](dvd-object.md)                               | <span data-ttu-id="2b05b-135">使用 Dvd 的屬性、方法和事件。</span><span class="sxs-lookup"><span data-stu-id="2b05b-135">A property, methods, and events for working with DVDs.</span></span>                                                                                                                                         |
| [<span data-ttu-id="2b05b-136">錯誤</span><span class="sxs-lookup"><span data-stu-id="2b05b-136">Error</span></span>](error-object.md)                           | <span data-ttu-id="2b05b-137">提供 **ErrorItem** 物件集合存取權的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="2b05b-137">Methods and properties providing access to a collection of **ErrorItem** objects.</span></span>                                                                                                              |
| [<span data-ttu-id="2b05b-138">ErrorItem</span><span class="sxs-lookup"><span data-stu-id="2b05b-138">ErrorItem</span></span>](erroritem-object.md)                   | <span data-ttu-id="2b05b-139">提供錯誤相關資訊的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b05b-139">Properties that provide information about errors.</span></span>                                                                                                                                              |
| [<span data-ttu-id="2b05b-140">媒體</span><span class="sxs-lookup"><span data-stu-id="2b05b-140">Media</span></span>](media-object.md)                           | <span data-ttu-id="2b05b-141">與媒體專案相關的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="2b05b-141">Methods and properties relating to media items.</span></span>                                                                                                                                                |
| [<span data-ttu-id="2b05b-142">MediaCollection</span><span class="sxs-lookup"><span data-stu-id="2b05b-142">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="2b05b-143">提供 **媒體** 物件集合存取權的方法。</span><span class="sxs-lookup"><span data-stu-id="2b05b-143">Methods that provide access to a collection of **Media** objects.</span></span>                                                                                                                              |
| [<span data-ttu-id="2b05b-144">MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="2b05b-144">MetadataPicture</span></span>](metadatapicture-object.md)       | <span data-ttu-id="2b05b-145">用來取得 **WM/圖片** 中繼資料屬性之影像值資訊的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b05b-145">Properties for retrieving information on the image values of the **WM/Picture** metadata attribute.</span></span>                                                                                            |
| [<span data-ttu-id="2b05b-146">MetadataText</span><span class="sxs-lookup"><span data-stu-id="2b05b-146">MetadataText</span></span>](metadatatext-object.md)             | <span data-ttu-id="2b05b-147">用於抓取複雜文字中繼資料屬性之中繼資料的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b05b-147">Properties for retrieving metadata for complex textual metadata attributes.</span></span>                                                                                                                    |
| [<span data-ttu-id="2b05b-148">Network</span><span class="sxs-lookup"><span data-stu-id="2b05b-148">Network</span></span>](network-object.md)                       | <span data-ttu-id="2b05b-149">與 Windows Media Player 的網路連接相關的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b05b-149">Properties relating to the network connection of Windows Media Player.</span></span>                                                                                                                         |
| [<span data-ttu-id="2b05b-150">球員</span><span class="sxs-lookup"><span data-stu-id="2b05b-150">Player</span></span>](player-object.md)                         | <span data-ttu-id="2b05b-151">Windows Media Player 的方法、屬性和事件可進行程式設計以回應。</span><span class="sxs-lookup"><span data-stu-id="2b05b-151">Methods, properties, and events that Windows Media Player can be programmed to respond to.</span></span>                                                                                                     |
| [<span data-ttu-id="2b05b-152">PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="2b05b-152">PlayerApplication</span></span>](playerapplication-object.md)   | <span data-ttu-id="2b05b-153">方法和屬性，可在遠端 Windows Media Player 控制項和播放程式的完整模式之間切換。</span><span class="sxs-lookup"><span data-stu-id="2b05b-153">Methods and properties for switching between a remoted Windows Media Player control and the full mode of the Player.</span></span> <span data-ttu-id="2b05b-154">只能搭配以遠端模式內嵌控制項的 c + + 程式使用。</span><span class="sxs-lookup"><span data-stu-id="2b05b-154">Can only be used with C++ programs that embed the control in remote mode.</span></span> |
| [<span data-ttu-id="2b05b-155">播放 清單</span><span class="sxs-lookup"><span data-stu-id="2b05b-155">Playlist</span></span>](playlist-object.md)                     | <span data-ttu-id="2b05b-156">操作媒體專案清單的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="2b05b-156">Methods and properties for manipulating lists of media items.</span></span>                                                                                                                                  |
| [<span data-ttu-id="2b05b-157">PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="2b05b-157">PlaylistArray</span></span>](playlistarray-object.md)           | <span data-ttu-id="2b05b-158">方法和屬性，用來依索引編號存取 **播放清單** 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="2b05b-158">A method and a property for accessing a collection of **Playlist** objects by index number.</span></span>                                                                                                    |
| [<span data-ttu-id="2b05b-159">PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="2b05b-159">PlaylistCollection</span></span>](playlistcollection-object.md) | <span data-ttu-id="2b05b-160">用來組織 **播放清單** 物件集合的方法。</span><span class="sxs-lookup"><span data-stu-id="2b05b-160">Methods for organizing a collection of **Playlist** objects.</span></span>                                                                                                                                   |
| [<span data-ttu-id="2b05b-161">查詢</span><span class="sxs-lookup"><span data-stu-id="2b05b-161">Query</span></span>](query-object.md)                           | <span data-ttu-id="2b05b-162">修改複合查詢的方法。</span><span class="sxs-lookup"><span data-stu-id="2b05b-162">Methods for modifying a compound query.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="2b05b-163">設定</span><span class="sxs-lookup"><span data-stu-id="2b05b-163">Settings</span></span>](settings-object.md)                     | <span data-ttu-id="2b05b-164">允許規格或抓取 Windows Media Player 設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b05b-164">Properties that allow the specification or retrieval of Windows Media Player settings.</span></span>                                                                                                         |
| [<span data-ttu-id="2b05b-165">StringCollection</span><span class="sxs-lookup"><span data-stu-id="2b05b-165">StringCollection</span></span>](stringcollection-object.md)     | <span data-ttu-id="2b05b-166">用來操作字串集合的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="2b05b-166">A method and a property for manipulating collections of strings.</span></span>                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="2b05b-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b05b-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b05b-168">**Windows Media Player 物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="2b05b-168">**Windows Media Player Object Model Reference**</span></span>](windows-media-player-object-model-reference.md)
</dt> </dl>

 

 




