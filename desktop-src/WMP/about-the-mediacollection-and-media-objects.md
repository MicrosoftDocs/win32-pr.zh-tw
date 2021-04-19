---
title: 關於 MediaCollection 和 Media 物件
description: 關於 MediaCollection 和 Media 物件
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Windows Media Player，MediaCollection 物件
- Windows Media Player 物件模型，MediaCollection 物件
- 物件模型，MediaCollection 物件
- Windows Media Player ActiveX 控制項，MediaCollection 物件
- ActiveX 控制項，MediaCollection 物件
- Windows Media Player 行動 ActiveX 控制項，MediaCollection 物件
- Windows Media Player Mobile，MediaCollection 物件
- MediaCollection 物件
- Windows Media Player，媒體物件
- Windows Media Player 物件模型，媒體物件
- 物件模型，媒體物件
- Windows Media Player ActiveX 控制項、媒體物件
- ActiveX 控制項、媒體物件
- Windows Media Player 的行動 ActiveX 控制項、媒體物件
- Windows Media Player Mobile，Media 物件
- 媒體物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe902fd9ed046e0197fb5c8c2d995d26befafe29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106976323"
---
# <a name="about-the-mediacollection-and-media-objects"></a><span data-ttu-id="c4e7c-119">關於 MediaCollection 和 Media 物件</span><span class="sxs-lookup"><span data-stu-id="c4e7c-119">About the MediaCollection and Media Objects</span></span>

<span data-ttu-id="c4e7c-120">**MediaCollection** 和 **media** 物件會管理媒體集合，以定義 Windows Media Player 可以存取的數位媒體檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="c4e7c-120">The **MediaCollection** and **Media** objects govern the media collection, which defines the locations of digital media files that Windows Media Player can access.</span></span> <span data-ttu-id="c4e7c-121">您可以從 **Player** 物件的 **MediaCollection** 屬性取得 **MediaCollection** 物件。</span><span class="sxs-lookup"><span data-stu-id="c4e7c-121">You get the **MediaCollection** object from the **mediaCollection** property of the **Player** object.</span></span> <span data-ttu-id="c4e7c-122">**MediaCollection** 屬性會傳回 **mediaCollection** 物件。</span><span class="sxs-lookup"><span data-stu-id="c4e7c-122">The **mediaCollection** property returns the **MediaCollection** object.</span></span> <span data-ttu-id="c4e7c-123">您只能在建立 **MediaCollection** 物件之後，存取其屬性。</span><span class="sxs-lookup"><span data-stu-id="c4e7c-123">You can only access the properties of the **MediaCollection** object after you have created it.</span></span> <span data-ttu-id="c4e7c-124">例如，若要將 **Media** 物件新增 () 的歌曲，請使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="c4e7c-124">For example, to add a **Media** object (a song), use the following code:</span></span>


```C++
player.mediacollection.add('laure.wma');

```



<span data-ttu-id="c4e7c-125">您已將 laure 檔案新增至媒體集合。</span><span class="sxs-lookup"><span data-stu-id="c4e7c-125">You have added the file laure.wma to the media collection.</span></span>

<span data-ttu-id="c4e7c-126">您可以使用 **播放** 程式的 **currentMedia** 屬性來取得目前的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="c4e7c-126">You can get the current **Media** object by using the **currentMedia** property of the **Player**.</span></span> <span data-ttu-id="c4e7c-127">例如，此程式碼會取得目前 **媒體** 物件的 **duration** 屬性：</span><span class="sxs-lookup"><span data-stu-id="c4e7c-127">For example, this code gets the **duration** property of the current **Media** object:</span></span>


```C++
myduration = player.currentmedia.duration;

```



<span data-ttu-id="c4e7c-128">有許多方法可取得 **媒體** 物件，讓您可以存取其屬性。</span><span class="sxs-lookup"><span data-stu-id="c4e7c-128">There are many ways to get a **Media** object so that you can access its properties.</span></span> <span data-ttu-id="c4e7c-129">例如，如果您想要存取目前媒體的 **duration** 屬性，則可以使用下列每一行程式碼。</span><span class="sxs-lookup"><span data-stu-id="c4e7c-129">For example, if you want to access the **duration** property of the current media, each of the following lines of code could be used.</span></span>

<span data-ttu-id="c4e7c-130">若要取得目前播放媒體的持續時間：</span><span class="sxs-lookup"><span data-stu-id="c4e7c-130">To get the duration of the currently playing media:</span></span>


```C++
player.currentMedia.duration;

```



<span data-ttu-id="c4e7c-131">若要取得播放清單中目前媒體的持續時間：</span><span class="sxs-lookup"><span data-stu-id="c4e7c-131">To get the duration of the current media in a playlist:</span></span>


```C++
player.controls.currentItem.duration;

```



<span data-ttu-id="c4e7c-132">若要取得播放清單中第三個媒體專案的持續時間：</span><span class="sxs-lookup"><span data-stu-id="c4e7c-132">To get the duration of the third media item in a playlist:</span></span>


```C++
player.currentPlaylist.item(2).duration;

```



<span data-ttu-id="c4e7c-133">若要取得「爵士樂」類型中第三個媒體專案的持續時間：</span><span class="sxs-lookup"><span data-stu-id="c4e7c-133">To get the duration of the third media item in a "Jazz" genre:</span></span>


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



<span data-ttu-id="c4e7c-134">若要取得第二個播放清單中第三個媒體專案的持續時間：</span><span class="sxs-lookup"><span data-stu-id="c4e7c-134">To get the duration of the third media item in the second playlist:</span></span>


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a><span data-ttu-id="c4e7c-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4e7c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4e7c-136">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="c4e7c-136">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="c4e7c-137">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="c4e7c-137">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="c4e7c-138">**指令碼語言的播放程式物件模型**</span><span class="sxs-lookup"><span data-stu-id="c4e7c-138">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




