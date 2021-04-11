---
title: 播放清單物件
description: 播放清單物件提供一種方式，可讓您使用下列屬性和方法，在清單中組織媒體專案以方便操作。
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- 播放清單物件 Windows Media Player
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d517e13f8da103b1f9cee9498cce58a62eaf6462
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022248"
---
# <a name="playlist-object"></a><span data-ttu-id="1c565-104">播放清單物件</span><span class="sxs-lookup"><span data-stu-id="1c565-104">Playlist Object</span></span>

<span data-ttu-id="1c565-105">**播放** 清單物件提供一種方式，可讓您使用下列屬性和方法，在清單中組織媒體專案以方便操作。</span><span class="sxs-lookup"><span data-stu-id="1c565-105">The **Playlist** object provides a way to organize media items in a list for easy manipulation by using the following properties and methods.</span></span>

<span data-ttu-id="1c565-106">**播放清單** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="1c565-106">The **Playlist** object supports the following properties.</span></span>



| <span data-ttu-id="1c565-107">屬性</span><span class="sxs-lookup"><span data-stu-id="1c565-107">Property</span></span>                                      | <span data-ttu-id="1c565-108">描述</span><span class="sxs-lookup"><span data-stu-id="1c565-108">Description</span></span>                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="1c565-109">attributeCount</span><span class="sxs-lookup"><span data-stu-id="1c565-109">attributeCount</span></span>](playlist-attributecount.md) | <span data-ttu-id="1c565-110">捕獲與播放清單相關聯的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="1c565-110">Retrieves the number of attributes associated with the playlist.</span></span> |
| [<span data-ttu-id="1c565-111">attributeName</span><span class="sxs-lookup"><span data-stu-id="1c565-111">attributeName</span></span>](playlist-attributename.md)   | <span data-ttu-id="1c565-112">抓取索引所指定之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c565-112">Retrieves the name of an attribute specified by an index.</span></span>        |
| [<span data-ttu-id="1c565-113">計數</span><span class="sxs-lookup"><span data-stu-id="1c565-113">count</span></span>](playlist-count.md)                   | <span data-ttu-id="1c565-114">捕獲播放清單中的專案數。</span><span class="sxs-lookup"><span data-stu-id="1c565-114">Retrieves the number of items in the playlist.</span></span>                   |
| [<span data-ttu-id="1c565-115">name</span><span class="sxs-lookup"><span data-stu-id="1c565-115">name</span></span>](playlist-name.md)                     | <span data-ttu-id="1c565-116">指定或抓取播放清單的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c565-116">Specifies or retrieves the name of the playlist.</span></span>                 |



 

<span data-ttu-id="1c565-117">**播放清單** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="1c565-117">The **Playlist** object supports the following methods.</span></span>



| <span data-ttu-id="1c565-118">方法</span><span class="sxs-lookup"><span data-stu-id="1c565-118">Method</span></span>                                  | <span data-ttu-id="1c565-119">描述</span><span class="sxs-lookup"><span data-stu-id="1c565-119">Description</span></span>                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c565-120">appendItem</span><span class="sxs-lookup"><span data-stu-id="1c565-120">appendItem</span></span>](playlist-appenditem.md)   | <span data-ttu-id="1c565-121">將媒體專案加入至播放清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="1c565-121">Adds a media item to the end of the playlist.</span></span>                                                          |
| <span data-ttu-id="1c565-122">**清除**</span><span class="sxs-lookup"><span data-stu-id="1c565-122">**clear**</span></span>                               | <span data-ttu-id="1c565-123">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="1c565-123">Reserved for future use.</span></span>                                                                               |
| [<span data-ttu-id="1c565-124">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="1c565-124">getItemInfo</span></span>](playlist-getiteminfo.md) | <span data-ttu-id="1c565-125">捕獲播放清單屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1c565-125">Retrieves the value of a playlist attribute.</span></span>                                                           |
| [<span data-ttu-id="1c565-126">insertItem</span><span class="sxs-lookup"><span data-stu-id="1c565-126">insertItem</span></span>](playlist-insertitem.md)   | <span data-ttu-id="1c565-127">將媒體專案插入播放清單中指定的位置。</span><span class="sxs-lookup"><span data-stu-id="1c565-127">Inserts a media item into the playlist at the specified location.</span></span>                                      |
| [<span data-ttu-id="1c565-128">isIdentical</span><span class="sxs-lookup"><span data-stu-id="1c565-128">isIdentical</span></span>](playlist-isidentical.md) | <span data-ttu-id="1c565-129">抓取值，指出提供的播放清單物件是否與目前的 **播放清單** 物件相同。</span><span class="sxs-lookup"><span data-stu-id="1c565-129">Retrieves a value indicating whether the supplied **Playlist** object is identical to the current one.</span></span> |
| [<span data-ttu-id="1c565-130">item</span><span class="sxs-lookup"><span data-stu-id="1c565-130">item</span></span>](playlist-item.md)               | <span data-ttu-id="1c565-131">抓取位於指定之索引處的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="1c565-131">Retrieves the media item at the specified index.</span></span>                                                       |
| [<span data-ttu-id="1c565-132">moveItem</span><span class="sxs-lookup"><span data-stu-id="1c565-132">moveItem</span></span>](playlist-moveitem.md)       | <span data-ttu-id="1c565-133">變更播放清單中專案的位置。</span><span class="sxs-lookup"><span data-stu-id="1c565-133">Changes the location of an item in the playlist.</span></span>                                                       |
| [<span data-ttu-id="1c565-134">removeItem</span><span class="sxs-lookup"><span data-stu-id="1c565-134">removeItem</span></span>](playlist-removeitem.md)   | <span data-ttu-id="1c565-135">從播放清單中移除指定的專案。</span><span class="sxs-lookup"><span data-stu-id="1c565-135">Removes the specified item from the playlist.</span></span>                                                          |
| [<span data-ttu-id="1c565-136">setItemInfo</span><span class="sxs-lookup"><span data-stu-id="1c565-136">setItemInfo</span></span>](playlist-setiteminfo.md) | <span data-ttu-id="1c565-137">指定播放清單屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1c565-137">Specifies the value of a playlist attribute.</span></span>                                                           |



 

<span data-ttu-id="1c565-138">**播放清單** 物件是透過下列屬性和方法來存取。</span><span class="sxs-lookup"><span data-stu-id="1c565-138">The **Playlist** object is accessed through the following properties and methods.</span></span>



| <span data-ttu-id="1c565-139">Object</span><span class="sxs-lookup"><span data-stu-id="1c565-139">Object</span></span>                                              | <span data-ttu-id="1c565-140">屬性或方法</span><span class="sxs-lookup"><span data-stu-id="1c565-140">Property or method</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c565-141">光碟</span><span class="sxs-lookup"><span data-stu-id="1c565-141">Cdrom</span></span>](cdrom-object.md)                           | [<span data-ttu-id="1c565-142">播放清單</span><span class="sxs-lookup"><span data-stu-id="1c565-142">playlist</span></span>](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="1c565-143">MediaCollection</span><span class="sxs-lookup"><span data-stu-id="1c565-143">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="1c565-144">[getAll](mediacollection-getall.md)、 [getByAlbum](mediacollection-getbyalbum.md)、 [getByAttribute](mediacollection-getbyattribute.md)、 [getByAuthor](mediacollection-getbyauthor.md)、 [getByGenre](mediacollection-getbygenre.md)、 [getByName](mediacollection-getbyname.md)</span><span class="sxs-lookup"><span data-stu-id="1c565-144">[getAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md)</span></span> |
| [<span data-ttu-id="1c565-145">球員</span><span class="sxs-lookup"><span data-stu-id="1c565-145">Player</span></span>](player-object.md)                         | <span data-ttu-id="1c565-146">[currentPlaylist](player-currentplaylist.md)、 [[]](player-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="1c565-146">[currentPlaylist](player-currentplaylist.md), [newPlaylist](player-newplaylist.md)</span></span>                                                                                                                                                                                               |
| [<span data-ttu-id="1c565-147">PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="1c565-147">PlaylistArray</span></span>](playlistarray-object.md)           | [<span data-ttu-id="1c565-148">item</span><span class="sxs-lookup"><span data-stu-id="1c565-148">item</span></span>](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="1c565-149">PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="1c565-149">PlaylistCollection</span></span>](playlistcollection-object.md) | <span data-ttu-id="1c565-150">[[]](playlistcollection-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="1c565-150">[newPlaylist](playlistcollection-newplaylist.md)</span></span>                                                                                                                                                                                                                                  |



 

<span data-ttu-id="1c565-151">因為這是最常見的存取方式，也就是 *播放機*。**currentPlaylist** 是用於參考語法區段中的說明用途。</span><span class="sxs-lookup"><span data-stu-id="1c565-151">Because it is the most common means of access, *player*.**currentPlaylist** is used for purposes of illustration in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c565-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c565-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c565-153">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="1c565-153">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




