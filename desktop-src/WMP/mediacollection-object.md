---
title: MediaCollection 物件
description: MediaCollection 物件提供一種方式來組織大型的媒體專案集合。 您可以查詢它，以自動產生播放清單。
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- MediaCollection 物件 Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2232e3590acd371039494b31c5d592c2e00f0199
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106969086"
---
# <a name="mediacollection-object"></a><span data-ttu-id="48371-105">MediaCollection 物件</span><span class="sxs-lookup"><span data-stu-id="48371-105">MediaCollection Object</span></span>

<span data-ttu-id="48371-106">**MediaCollection** 物件提供一種方式來組織大型的媒體專案集合。</span><span class="sxs-lookup"><span data-stu-id="48371-106">The **MediaCollection** object provides a way to organize a large collection of media items.</span></span> <span data-ttu-id="48371-107">您可以查詢它，以自動產生播放清單。</span><span class="sxs-lookup"><span data-stu-id="48371-107">It can be queried to generate playlists automatically.</span></span>

<span data-ttu-id="48371-108">**MediaCollection** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="48371-108">The **MediaCollection** object supports the following methods.</span></span>



| <span data-ttu-id="48371-109">方法</span><span class="sxs-lookup"><span data-stu-id="48371-109">Method</span></span>                                                                           | <span data-ttu-id="48371-110">描述</span><span class="sxs-lookup"><span data-stu-id="48371-110">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48371-111">add</span><span class="sxs-lookup"><span data-stu-id="48371-111">add</span></span>](mediacollection-add.md)                                                   | <span data-ttu-id="48371-112">將新的媒體專案或播放清單新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="48371-112">Adds a new media item or playlist to the library.</span></span>                                                                                                              |
| [<span data-ttu-id="48371-113">createQuery</span><span class="sxs-lookup"><span data-stu-id="48371-113">createQuery</span></span>](mediacollection-createquery.md)                                   | <span data-ttu-id="48371-114">建立新的 [查詢](query-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="48371-114">Creates a new [Query](query-object.md) object.</span></span>                                                                                                                |
| [<span data-ttu-id="48371-115">getAll</span><span class="sxs-lookup"><span data-stu-id="48371-115">getAll</span></span>](mediacollection-getall.md)                                             | <span data-ttu-id="48371-116">抓取包含媒體櫃中所有媒體專案的 [播放清單](playlist-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="48371-116">Retrieves a [Playlist](playlist-object.md) object containing all media items in the library.</span></span>                                                                  |
| [<span data-ttu-id="48371-117">getAttributeStringCollection</span><span class="sxs-lookup"><span data-stu-id="48371-117">getAttributeStringCollection</span></span>](mediacollection-getattributestringcollection.md) | <span data-ttu-id="48371-118">抓取 [StringCollection](stringcollection-object.md) 物件，代表指定之媒體類型內指定之屬性的所有值集。</span><span class="sxs-lookup"><span data-stu-id="48371-118">Retrieves a [StringCollection](stringcollection-object.md) object representing the set of all values for a specified attribute within a specified media type.</span></span> |
| [<span data-ttu-id="48371-119">getByAlbum</span><span class="sxs-lookup"><span data-stu-id="48371-119">getByAlbum</span></span>](mediacollection-getbyalbum.md)                                     | <span data-ttu-id="48371-120">從指定的專輯抓取包含媒體專案的 [播放清單](playlist-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="48371-120">Retrieves a [Playlist](playlist-object.md) object containing media items from the specified album.</span></span>                                                            |
| [<span data-ttu-id="48371-121">getByAttribute</span><span class="sxs-lookup"><span data-stu-id="48371-121">getByAttribute</span></span>](mediacollection-getbyattribute.md)                             | <span data-ttu-id="48371-122">抓取 [播放清單](playlist-object.md) 物件，其中包含具有指定之屬性的媒體專案具有指定的值。</span><span class="sxs-lookup"><span data-stu-id="48371-122">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified attribute having the specified value.</span></span>                             |
| [<span data-ttu-id="48371-123">getByAttributeAndMediaType</span><span class="sxs-lookup"><span data-stu-id="48371-123">getByAttributeAndMediaType</span></span>](mediacollection-getbyattributeandmediatype.md)     | <span data-ttu-id="48371-124">抓取包含具有指定屬性和媒體類型之[媒體](media-object.md)物件的[播放清單](playlist-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="48371-124">Retrieves a [Playlist](playlist-object.md) object containing [Media](media-object.md) objects having the specified attribute and media type.</span></span>                 |
| [<span data-ttu-id="48371-125">getByAuthor</span><span class="sxs-lookup"><span data-stu-id="48371-125">getByAuthor</span></span>](mediacollection-getbyauthor.md)                                   | <span data-ttu-id="48371-126">依指定的作者，抓取包含媒體專案的 [播放清單](playlist-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="48371-126">Retrieves a [Playlist](playlist-object.md) object containing media items by the specified author.</span></span>                                                             |
| [<span data-ttu-id="48371-127">getByGenre</span><span class="sxs-lookup"><span data-stu-id="48371-127">getByGenre</span></span>](mediacollection-getbygenre.md)                                     | <span data-ttu-id="48371-128">抓取包含具有指定類型之媒體專案的 [播放清單](playlist-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="48371-128">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified genre.</span></span>                                                            |
| [<span data-ttu-id="48371-129">getByName</span><span class="sxs-lookup"><span data-stu-id="48371-129">getByName</span></span>](mediacollection-getbyname.md)                                       | <span data-ttu-id="48371-130">抓取包含具有指定名稱之媒體專案的 [播放清單](playlist-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="48371-130">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified name.</span></span>                                                             |
| [<span data-ttu-id="48371-131">getMediaAtom</span><span class="sxs-lookup"><span data-stu-id="48371-131">getMediaAtom</span></span>](mediacollection-getmediaatom.md)                                 | <span data-ttu-id="48371-132">抓取可用屬性集合中指定的屬性所在的索引。</span><span class="sxs-lookup"><span data-stu-id="48371-132">Retrieves the index at which a specified property resides within the set of available properties.</span></span>                                                              |
| [<span data-ttu-id="48371-133">getPlaylistByQuery</span><span class="sxs-lookup"><span data-stu-id="48371-133">getPlaylistByQuery</span></span>](mediacollection-getplaylistbyquery.md)                     | <span data-ttu-id="48371-134">抓取包含符合查詢準則之[媒體](media-object.md)物件的[播放清單](playlist-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="48371-134">Retrieves a [Playlist](playlist-object.md) object containing [Media](media-object.md) objects that match the query conditions.</span></span>                               |
| [<span data-ttu-id="48371-135">getStringCollectionByQuery</span><span class="sxs-lookup"><span data-stu-id="48371-135">getStringCollectionByQuery</span></span>](mediacollection-getstringcollectionbyquery.md)     | <span data-ttu-id="48371-136">抓取 [StringCollection](stringcollection-object.md) 物件，其中包含符合查詢準則的字串。</span><span class="sxs-lookup"><span data-stu-id="48371-136">Retrieves a [StringCollection](stringcollection-object.md) object containing strings that match the query conditions.</span></span>                                         |
| [<span data-ttu-id="48371-137">isDeleted</span><span class="sxs-lookup"><span data-stu-id="48371-137">isDeleted</span></span>](mediacollection-isdeleted.md)                                       | <span data-ttu-id="48371-138">抓取值，指出指定的媒體專案是否在 [刪除的專案] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="48371-138">Retrieves a value indicating whether the specified media item is in the deleted items folder.</span></span>                                                                  |
| [<span data-ttu-id="48371-139">remove</span><span class="sxs-lookup"><span data-stu-id="48371-139">remove</span></span>](mediacollection-remove.md)                                             | <span data-ttu-id="48371-140">從媒體集合中移除專案。</span><span class="sxs-lookup"><span data-stu-id="48371-140">Removes an item from the media collection.</span></span>                                                                                                                     |
| [<span data-ttu-id="48371-141">setDeleted</span><span class="sxs-lookup"><span data-stu-id="48371-141">setDeleted</span></span>](mediacollection-setdeleted.md)                                     | <span data-ttu-id="48371-142">將指定的媒體專案移到 [刪除的專案] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="48371-142">Moves the specified media item to the deleted items folder.</span></span>                                                                                                    |



 

<span data-ttu-id="48371-143">**MediaCollection** 物件是透過下列屬性來存取。</span><span class="sxs-lookup"><span data-stu-id="48371-143">The **MediaCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="48371-144">Object</span><span class="sxs-lookup"><span data-stu-id="48371-144">Object</span></span>                      | <span data-ttu-id="48371-145">屬性</span><span class="sxs-lookup"><span data-stu-id="48371-145">Property</span></span>                                      |
|-----------------------------|-----------------------------------------------|
| [<span data-ttu-id="48371-146">球員</span><span class="sxs-lookup"><span data-stu-id="48371-146">Player</span></span>](player-object.md) | [<span data-ttu-id="48371-147">mediaCollection</span><span class="sxs-lookup"><span data-stu-id="48371-147">mediaCollection</span></span>](player-mediacollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="48371-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48371-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48371-149">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="48371-149">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




