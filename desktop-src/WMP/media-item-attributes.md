---
title: 媒體專案屬性
description: 媒體專案屬性
ms.assetid: d43addec-e06c-4ef3-9012-3ecf589b105c
keywords:
- Windows Media Player，程式庫
- Windows Media Player 物件模型，程式庫
- 物件模型，程式庫
- Windows Media Player 行動裝置、物件模型的程式庫
- Windows Media Player ActiveX 控制項，物件模型的程式庫
- Windows Media Player 的行動 ActiveX 控制項、物件模型的程式庫
- ActiveX 控制項，物件模型的程式庫
- Windows Media Player，媒體專案的屬性
- Windows Media Player 物件模型，媒體專案的屬性
- 物件模型、媒體專案的屬性
- Windows Media Player 行動裝置，媒體專案的屬性
- Windows Media Player ActiveX 控制項、媒體專案的屬性
- Windows Media Player 的行動 ActiveX 控制項、媒體專案的屬性
- ActiveX 控制項、媒體專案的屬性
- Windows Media Player 文件庫、媒體專案的屬性
- 文件庫、媒體專案的屬性
- 屬性，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ac8595cc07504c9cd3e195431513a1f8565e87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021414"
---
# <a name="media-item-attributes"></a><span data-ttu-id="69bff-120">媒體專案屬性</span><span class="sxs-lookup"><span data-stu-id="69bff-120">Media Item Attributes</span></span>

<span data-ttu-id="69bff-121">當您查看 Windows Media Player 中的程式庫時，您通常會看到有關媒體專案的大量資訊。</span><span class="sxs-lookup"><span data-stu-id="69bff-121">When you look at the library in Windows Media Player, you typically see a great deal of information about a media item.</span></span> <span data-ttu-id="69bff-122">例如，除了音訊播放軌的名稱之外，您也可能會看到播放軌的專輯名稱、演出者和編輯器的名稱、音樂的類型等等。</span><span class="sxs-lookup"><span data-stu-id="69bff-122">In addition to the name of an audio track, for example, you will likely see the name of the album the track is on, the names of the artist and composer, the genre of the music, and so on.</span></span>

<span data-ttu-id="69bff-123">在 Windows Media Player 物件模型中，這些中繼資料專案稱為屬性。</span><span class="sxs-lookup"><span data-stu-id="69bff-123">In the Windows Media Player object model, these metadata items are called attributes.</span></span> <span data-ttu-id="69bff-124">物件模型包含屬性和方法，您可以使用這些屬性和方法來查詢媒體專案和屬性的播放清單。</span><span class="sxs-lookup"><span data-stu-id="69bff-124">The object model includes properties and methods you can use to query media items and playlists for attributes.</span></span> <span data-ttu-id="69bff-125">然後，您可以在使用者介面中顯示內容值，或是您的程式碼可以根據屬性的值採取動作。</span><span class="sxs-lookup"><span data-stu-id="69bff-125">You can then display attribute values in your user interface, or your code can take actions based on the value of an attribute.</span></span>

<span data-ttu-id="69bff-126">下列主題將說明如何使用媒體專案屬性。</span><span class="sxs-lookup"><span data-stu-id="69bff-126">The following topics describe working with media item attributes.</span></span>



| <span data-ttu-id="69bff-127">主題</span><span class="sxs-lookup"><span data-stu-id="69bff-127">Topic</span></span>                                                                                      | <span data-ttu-id="69bff-128">描述</span><span class="sxs-lookup"><span data-stu-id="69bff-128">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69bff-129">瞭解屬性來源</span><span class="sxs-lookup"><span data-stu-id="69bff-129">Understanding Attribute Sources</span></span>](understanding-attribute-sources.md)                     | <span data-ttu-id="69bff-130">描述媒體專案的來源如何影響可能與其相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="69bff-130">Describes how the source of a media item affects the attributes that may be associated with it.</span></span> |
| [<span data-ttu-id="69bff-131">讀取屬性值</span><span class="sxs-lookup"><span data-stu-id="69bff-131">Reading Attribute Values</span></span>](reading-attribute-values.md)                                   | <span data-ttu-id="69bff-132">顯示用於取出屬性值的方法。</span><span class="sxs-lookup"><span data-stu-id="69bff-132">Shows the methods for retrieving the value of an attribute.</span></span>                                     |
| [<span data-ttu-id="69bff-133">具有多個值的屬性</span><span class="sxs-lookup"><span data-stu-id="69bff-133">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md)                     | <span data-ttu-id="69bff-134">顯示用來取得多重值屬性值的方法。</span><span class="sxs-lookup"><span data-stu-id="69bff-134">Shows the methods for retrieving the value of a multi-valued attribute.</span></span>                         |
| [<span data-ttu-id="69bff-135">從 CD 或 DVD 讀取屬性值</span><span class="sxs-lookup"><span data-stu-id="69bff-135">Reading Attribute Values from a CD or DVD</span></span>](reading-attribute-values-from-a-cd-or-dvd.md) | <span data-ttu-id="69bff-136">提供範例應用程式，以讀取媒體專案的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="69bff-136">Provides a sample application that reads all of the attributes of a media item.</span></span>                 |
| [<span data-ttu-id="69bff-137">變更屬性值</span><span class="sxs-lookup"><span data-stu-id="69bff-137">Changing Attribute Values</span></span>](changing-attribute-values.md)                                 | <span data-ttu-id="69bff-138">顯示變更屬性值的方法。</span><span class="sxs-lookup"><span data-stu-id="69bff-138">Shows the method for changing the value of an attribute.</span></span>                                        |
| [<span data-ttu-id="69bff-139">電視內容的屬性值</span><span class="sxs-lookup"><span data-stu-id="69bff-139">Attribute Values for TV Content</span></span>](attribute-values-for-tv-content.md)                     | <span data-ttu-id="69bff-140">顯示如何指定包含電視節目之數位視訊內容的屬性。</span><span class="sxs-lookup"><span data-stu-id="69bff-140">Shows how to specify attributes for digital video content that contains TV shows.</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="69bff-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="69bff-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69bff-142">**播放清單屬性**</span><span class="sxs-lookup"><span data-stu-id="69bff-142">**Playlist Attributes**</span></span>](playlist-attributes.md)
</dt> <dt>

[<span data-ttu-id="69bff-143">**使用程式庫**</span><span class="sxs-lookup"><span data-stu-id="69bff-143">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




