---
title: 管理媒體專案
description: 管理媒體專案
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows Media Player，程式庫
- Windows Media Player 物件模型，程式庫
- 物件模型，程式庫
- Windows Media Player 行動裝置、物件模型的程式庫
- Windows Media Player ActiveX 控制項，物件模型的程式庫
- Windows Media Player 的行動 ActiveX 控制項、物件模型的程式庫
- ActiveX 控制項，物件模型的程式庫
- Windows Media Player 程式庫，管理媒體專案
- 媒體櫃，管理媒體專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b8003de49de9b7e4e51aabeffa222fb649ddef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092317"
---
# <a name="managing-media-items"></a><span data-ttu-id="3e84b-112">管理媒體專案</span><span class="sxs-lookup"><span data-stu-id="3e84b-112">Managing Media Items</span></span>

<span data-ttu-id="3e84b-113">**媒體** 物件代表一個媒體專案。</span><span class="sxs-lookup"><span data-stu-id="3e84b-113">A **Media** object represents one media item.</span></span> <span data-ttu-id="3e84b-114">它具有可用來抓取資訊並向使用者顯示資訊的屬性和方法，或根據您抓取的值採取不同的動作。</span><span class="sxs-lookup"><span data-stu-id="3e84b-114">It has properties and methods you can use to retrieve information and display it to the user, or to take different actions based on the value you retrieve.</span></span>

<span data-ttu-id="3e84b-115">**媒體** 物件的大部分工作都牽涉到與媒體專案內容相關的中繼資料（稱為屬性）。</span><span class="sxs-lookup"><span data-stu-id="3e84b-115">Much of your work with **Media** objects involves metadata about the content of the media item, called the attributes.</span></span> <span data-ttu-id="3e84b-116">主題 [媒體專案屬性](media-item-attributes.md) 說明如何讀取和變更屬性值。</span><span class="sxs-lookup"><span data-stu-id="3e84b-116">The topic [Media Item Attributes](media-item-attributes.md) describes how to read and change attribute values.</span></span> <span data-ttu-id="3e84b-117">除了本主題之外，請參閱 Microsoft 網站上的 [Windows Media 中繼資料使用指導方針](/previous-versions/ms867702(v=msdn.10)) ，以取得有關屬性及其用途的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3e84b-117">In addition to this topic, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)) on the Microsoft website for more information about the attributes and their use.</span></span>

<span data-ttu-id="3e84b-118">**媒體** 物件具有直接取出部分屬性的屬性和方法，例如專案的名稱或持續時間。</span><span class="sxs-lookup"><span data-stu-id="3e84b-118">The **Media** object has properties and methods that retrieve some attributes directly, such as the name or duration of the item.</span></span> <span data-ttu-id="3e84b-119">針對影片專案，您可以抓取影像的高度和寬度，也可以根據標記的名稱或索引來取得標記資訊。</span><span class="sxs-lookup"><span data-stu-id="3e84b-119">For video items, you can retrieve the height and width of the image, and you can retrieve marker information based on the name or index of a marker.</span></span> <span data-ttu-id="3e84b-120">您也可以判斷特定媒體專案是否包含在特定的播放清單中。</span><span class="sxs-lookup"><span data-stu-id="3e84b-120">You can also determine whether a particular media item is included in a particular playlist.</span></span>

## <a name="retrieving-a-media-object"></a><span data-ttu-id="3e84b-121">取出媒體物件</span><span class="sxs-lookup"><span data-stu-id="3e84b-121">Retrieving a Media Object</span></span>

<span data-ttu-id="3e84b-122">您可以使用 *播放* 程式來快速存取目前的媒體專案。**currentMedia** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3e84b-122">You can quickly access the current media item by using the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="3e84b-123">在本主題中， **Player** 物件是以下列方式定義：</span><span class="sxs-lookup"><span data-stu-id="3e84b-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="3e84b-124">下列 c # 範例會捕獲代表目前專案的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="3e84b-124">The following C# example retrieves a **Media** object representing the current item.</span></span>


```C++
IWMPMedia media;
media = Player.currentMedia;

```



<span data-ttu-id="3e84b-125">您可以使用 *播放* 程式，從數位媒體檔案建立新的媒體專案。**newMedia** 方法。</span><span class="sxs-lookup"><span data-stu-id="3e84b-125">You can create a new media item from a digital media file by using the *Player*.**newMedia** method.</span></span> <span data-ttu-id="3e84b-126">您將 URL 路徑傳遞至數位媒體檔案，它會傳回新 **媒體** 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="3e84b-126">You pass the method the URL path to a digital media file, and it returns a reference to the new **Media** object.</span></span> <span data-ttu-id="3e84b-127">方法不會直接將新的物件加入至程式庫。</span><span class="sxs-lookup"><span data-stu-id="3e84b-127">The method does not add the new object to the library directly.</span></span> <span data-ttu-id="3e84b-128">不過，您可以將物件傳遞至 *播放清單*。**appendItem** 方法或 *播放清單*。**insertItem** 方法。</span><span class="sxs-lookup"><span data-stu-id="3e84b-128">However, you can pass the object to the *Playlist*.**appendItem** method or the *Playlist*.**insertItem** method.</span></span>

<span data-ttu-id="3e84b-129">下列 c # 範例會根據隨 Windows Media Player SDK 一併安裝的其中一個數位媒體範例，建立 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="3e84b-129">The following C# example creates a **Media** object based on one of the digital media samples installed with the Windows Media Player SDK.</span></span>


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> <span data-ttu-id="3e84b-130">您必須在字串中包含兩個反斜線 (\) 字元 (或在 c # ) 中使用 @ 字元，以代表一個實際的反斜線字元。</span><span class="sxs-lookup"><span data-stu-id="3e84b-130">You must include two backslash (\) characters (or use the @ character in C#) in a string to represent one actual backslash character.</span></span> <span data-ttu-id="3e84b-131">這是因為 c # 會使用單一反斜線字元來定義 escape 序列。</span><span class="sxs-lookup"><span data-stu-id="3e84b-131">This is because C# uses a single backslash character to define an escape sequence.</span></span>

 

<span data-ttu-id="3e84b-132">您可以使用 *MediaCollection*，從數位媒體檔案建立新的媒體專案，並將其新增至程式庫。**add** 方法。</span><span class="sxs-lookup"><span data-stu-id="3e84b-132">You can create a new media item from a digital media file and add it to the library in one step by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="3e84b-133">就像 *玩家* 一樣。**newMedia** 方法， **add** 方法會採用數位媒體檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="3e84b-133">Like the *Player*.**newMedia** method, the **add** method takes a path to a digital media file.</span></span>

<span data-ttu-id="3e84b-134">下列 c # 範例會根據其中一個 SDK 範例檔案建立 **媒體** 物件，並將該物件新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="3e84b-134">The following C# example creates a **Media** object based on one of the SDK sample files and adds that object to the library.</span></span>


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



<span data-ttu-id="3e84b-135">您可以使用 *播放清單* 來取出代表播放清單中媒體專案的 **媒體** 物件。**item** 方法。</span><span class="sxs-lookup"><span data-stu-id="3e84b-135">You can retrieve a **Media** object representing a media item in a playlist by using the *Playlist*.**item** method.</span></span> <span data-ttu-id="3e84b-136">下列 c # 範例會從目前的播放清單抓取第六個媒體專案。</span><span class="sxs-lookup"><span data-stu-id="3e84b-136">The following C# example retrieves the sixth media item from the current playlist.</span></span>


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a><span data-ttu-id="3e84b-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e84b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e84b-138">**CurrentItem**</span><span class="sxs-lookup"><span data-stu-id="3e84b-138">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="3e84b-139">**管理播放清單**</span><span class="sxs-lookup"><span data-stu-id="3e84b-139">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="3e84b-140">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="3e84b-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="3e84b-141">**MediaCollection 新增**</span><span class="sxs-lookup"><span data-stu-id="3e84b-141">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="3e84b-142">**CurrentMedia**</span><span class="sxs-lookup"><span data-stu-id="3e84b-142">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="3e84b-143">**NewMedia**</span><span class="sxs-lookup"><span data-stu-id="3e84b-143">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="3e84b-144">**播放清單。專案**</span><span class="sxs-lookup"><span data-stu-id="3e84b-144">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="3e84b-145">**使用程式庫**</span><span class="sxs-lookup"><span data-stu-id="3e84b-145">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




