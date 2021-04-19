---
title: 'IWMPMediaCollection (VB 和 C ) 介面 (h.264. h) '
description: 提供可用於組織大型媒體專案集合的方法。
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- IWMPMediaCollection (VB 和 C ) 介面 Windows Media Player
- IWMPMediaCollection (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPMediaCollection (VB and C )
- IWMPMediaCollection (VB and C ).isDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 424fd45b1fd3d02000a9774ffe75ec87e52dd9c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993248"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a><span data-ttu-id="6f5c1-105">IWMPMediaCollection (VB 和 c # ) 介面</span><span class="sxs-lookup"><span data-stu-id="6f5c1-105">IWMPMediaCollection (VB and C#) interface</span></span>

<span data-ttu-id="6f5c1-106">提供可用於組織大型媒體專案集合的方法。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-106">Provides methods that can be used to organize a large collection of media items.</span></span>

## <a name="members"></a><span data-ttu-id="6f5c1-107">成員</span><span class="sxs-lookup"><span data-stu-id="6f5c1-107">Members</span></span>

<span data-ttu-id="6f5c1-108">**IWMPMediaCollection (VB 和 c # )** 介面都有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6f5c1-108">The **IWMPMediaCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="6f5c1-109">方法</span><span class="sxs-lookup"><span data-stu-id="6f5c1-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6f5c1-110">方法</span><span class="sxs-lookup"><span data-stu-id="6f5c1-110">Methods</span></span>

<span data-ttu-id="6f5c1-111">**IWMPMediaCollection (VB 和 c # )** 介面都有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-111">The **IWMPMediaCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="6f5c1-112">方法</span><span class="sxs-lookup"><span data-stu-id="6f5c1-112">Method</span></span>                                                                                                                       | <span data-ttu-id="6f5c1-113">描述</span><span class="sxs-lookup"><span data-stu-id="6f5c1-113">Description</span></span>                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f5c1-114">**add**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-114">**add**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | <span data-ttu-id="6f5c1-115">將新的媒體專案或播放清單新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-115">Adds a new media item or playlist to the library.</span></span><br/>                                                                                  |
| [<span data-ttu-id="6f5c1-116">**getAll**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-116">**getAll**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | <span data-ttu-id="6f5c1-117">傳回 **IWMPPlaylist** 介面，這個介面對應于包含媒體櫃中所有媒體專案的播放清單。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-117">Returns an **IWMPPlaylist** interface that corresponds to the playlist that contains all media items in the library.</span></span><br/>               |
| [<span data-ttu-id="6f5c1-118">**getAttributeStringCollection**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-118">**getAttributeStringCollection**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | <span data-ttu-id="6f5c1-119">傳回 **IWMPStringCollection** 介面，這個介面表示媒體類型內指定之屬性的所有值集。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-119">Returns an **IWMPStringCollection** interface that represents the set of all values for a specified attribute within a media type.</span></span><br/> |
| [<span data-ttu-id="6f5c1-120">**getByAlbum**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-120">**getByAlbum**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | <span data-ttu-id="6f5c1-121">傳回 **IWMPPlaylist** 介面，這個介面可讓您從指定的專輯存取媒體專案。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-121">Returns an **IWMPPlaylist** interface that provides access to media items from the specified album.</span></span><br/>                                |
| [<span data-ttu-id="6f5c1-122">**getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-122">**getByAttribute**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | <span data-ttu-id="6f5c1-123">傳回 **IWMPPlaylist** 介面，這個介面會對應到具有指定值的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-123">Returns an **IWMPPlaylist** interface that corresponds to the specified attribute having the specified value.</span></span><br/>                      |
| [<span data-ttu-id="6f5c1-124">**getByAuthor**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-124">**getByAuthor**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | <span data-ttu-id="6f5c1-125">傳回 **IWMPPlaylist** 介面，這個介面會提供指定作者對媒體專案的存取權。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-125">Returns an **IWMPPlaylist** interface that provides access to the media items by the specified author.</span></span><br/>                             |
| [<span data-ttu-id="6f5c1-126">**getByGenre**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-126">**getByGenre**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | <span data-ttu-id="6f5c1-127">傳回 **IWMPPlaylist** 介面，這個介面可讓您存取指定之類型的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-127">Returns an **IWMPPlaylist** interface that provides access to media items of the specified genre.</span></span><br/>                                  |
| [<span data-ttu-id="6f5c1-128">**getByName**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-128">**getByName**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | <span data-ttu-id="6f5c1-129">傳回 **IWMPPlaylist** 介面，這個介面會提供具有指定名稱之媒體專案的存取權。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-129">Returns an **IWMPPlaylist** interface that provides access to media items with the specified name.</span></span><br/>                                 |
| [<span data-ttu-id="6f5c1-130">**getMediaAtom**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-130">**getMediaAtom**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | <span data-ttu-id="6f5c1-131">傳回指定之屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-131">Returns the index of a specified attribute.</span></span><br/>                                                                                        |
| <span data-ttu-id="6f5c1-132">**isDeleted**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-132">**isDeleted**</span></span>                                                                                                                | <span data-ttu-id="6f5c1-133">不再支援。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-133">No longer supported.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="6f5c1-134">**刪除**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-134">**remove**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | <span data-ttu-id="6f5c1-135">從媒體集合移除指定的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-135">Removes the specified media item from the media collection.</span></span><br/>                                                                        |
| [<span data-ttu-id="6f5c1-136">**setDeleted**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-136">**setDeleted**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | <span data-ttu-id="6f5c1-137">將指定的媒體專案移到 [刪除的專案] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-137">Moves the specified media item to the deleted items folder.</span></span><br/>                                                                        |



 

<span data-ttu-id="6f5c1-138">使用透過下列物件或介面存取的下列屬性來取得 **IWMPMediaCollection** 介面。</span><span class="sxs-lookup"><span data-stu-id="6f5c1-138">Get an **IWMPMediaCollection** interface by using the following properties accessed through the following object or interface.</span></span>



| <span data-ttu-id="6f5c1-139">物件或介面</span><span class="sxs-lookup"><span data-stu-id="6f5c1-139">Object or interface</span></span>                                               | <span data-ttu-id="6f5c1-140">屬性</span><span class="sxs-lookup"><span data-stu-id="6f5c1-140">Property</span></span>                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f5c1-141">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="6f5c1-141">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="6f5c1-142">**mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-142">**mediaCollection**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [<span data-ttu-id="6f5c1-143">**IWMPLibrary**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-143">**IWMPLibrary**</span></span>](iwmplibrary--vb-and-c.md)                      | [<span data-ttu-id="6f5c1-144">**mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-144">**mediaCollection**</span></span>](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="6f5c1-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f5c1-145">Requirements</span></span>



| <span data-ttu-id="6f5c1-146">需求</span><span class="sxs-lookup"><span data-stu-id="6f5c1-146">Requirement</span></span> | <span data-ttu-id="6f5c1-147">值</span><span class="sxs-lookup"><span data-stu-id="6f5c1-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6f5c1-148">標頭</span><span class="sxs-lookup"><span data-stu-id="6f5c1-148">Header</span></span><br/> | <dl> <span data-ttu-id="6f5c1-149"><dt>Wmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="6f5c1-149"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f5c1-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f5c1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f5c1-151">**適用于 Visual Basic .NET 和 C 的介面#**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-151">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="6f5c1-152">**IWMPMediaCollection2 介面**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-152">**IWMPMediaCollection2 Interface**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6f5c1-153">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-153">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6f5c1-154">**IWMPStringCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="6f5c1-154">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





