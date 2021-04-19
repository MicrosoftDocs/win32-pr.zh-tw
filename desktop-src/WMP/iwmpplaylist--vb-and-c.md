---
title: IWMPPlaylist (VB 和 C) 介面 (Wmp.h)
description: 提供屬性和方法來組織、管理和操作播放清單中的媒體專案。IWMPPlaylist 介面會公開下列屬性。
ms.assetid: c3f4f9dd-eb5f-493a-b8d0-22e70c63a2d1
keywords:
- IWMPPlaylist (VB 和 C ) 介面 Windows Media Player
- IWMPPlaylist (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPPlaylist (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52090588905e2fd79b218abe939f78c1e38fc79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989684"
---
# <a name="iwmpplaylist-vb-and-c-interface"></a><span data-ttu-id="c39be-105">IWMPPlaylist (VB 和 c # ) 介面</span><span class="sxs-lookup"><span data-stu-id="c39be-105">IWMPPlaylist (VB and C#) interface</span></span>

<span data-ttu-id="c39be-106">提供屬性和方法來組織、管理和操作播放清單中的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="c39be-106">Provides properties and methods to organize, manage, and manipulate media items in a playlist.</span></span>

<span data-ttu-id="c39be-107">**IWMPPlaylist** 介面會公開下列屬性。</span><span class="sxs-lookup"><span data-stu-id="c39be-107">The **IWMPPlaylist** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="c39be-108">成員</span><span class="sxs-lookup"><span data-stu-id="c39be-108">Members</span></span>

<span data-ttu-id="c39be-109">**IWMPPlaylist (VB 和 c # )** 介面都有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c39be-109">The **IWMPPlaylist (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="c39be-110">方法</span><span class="sxs-lookup"><span data-stu-id="c39be-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c39be-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c39be-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c39be-112">方法</span><span class="sxs-lookup"><span data-stu-id="c39be-112">Methods</span></span>

<span data-ttu-id="c39be-113">**IWMPPlaylist (VB 和 c # )** 介面都有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c39be-113">The **IWMPPlaylist (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="c39be-114">方法</span><span class="sxs-lookup"><span data-stu-id="c39be-114">Method</span></span>                                                                       | <span data-ttu-id="c39be-115">描述</span><span class="sxs-lookup"><span data-stu-id="c39be-115">Description</span></span>                                                             |
|:-----------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="c39be-116">**appendItem**</span><span class="sxs-lookup"><span data-stu-id="c39be-116">**appendItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)   | <span data-ttu-id="c39be-117">將媒體專案加入至播放清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="c39be-117">Adds a media item to the end of the playlist.</span></span><br/>                |
| [<span data-ttu-id="c39be-118">**清楚**</span><span class="sxs-lookup"><span data-stu-id="c39be-118">**clear**</span></span>](iwmpplaylist-iwmpplaylist-clear--vb-and-c.md)                   | <span data-ttu-id="c39be-119">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="c39be-119">Reserved for future use.</span></span><br/>                                     |
| [<span data-ttu-id="c39be-120">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="c39be-120">**getItemInfo**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) | <span data-ttu-id="c39be-121">傳回依名稱指定的播放清單屬性值。</span><span class="sxs-lookup"><span data-stu-id="c39be-121">Returns the value of a playlist attribute specified by name.</span></span><br/> |
| [<span data-ttu-id="c39be-122">**insertItem**</span><span class="sxs-lookup"><span data-stu-id="c39be-122">**insertItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)   | <span data-ttu-id="c39be-123">將媒體專案插入播放清單中的指定位置。</span><span class="sxs-lookup"><span data-stu-id="c39be-123">Inserts a media item at a specified location in a playlist.</span></span><br/>  |
| [<span data-ttu-id="c39be-124">**moveItem**</span><span class="sxs-lookup"><span data-stu-id="c39be-124">**moveItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-moveitem--vb-and-c.md)       | <span data-ttu-id="c39be-125">變更播放清單中媒體專案的位置。</span><span class="sxs-lookup"><span data-stu-id="c39be-125">Changes the location of a media item in the playlist.</span></span><br/>        |
| [<span data-ttu-id="c39be-126">**removeItem**</span><span class="sxs-lookup"><span data-stu-id="c39be-126">**removeItem**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)   | <span data-ttu-id="c39be-127">從播放清單中移除指定的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="c39be-127">Removes the specified media item from the playlist.</span></span><br/>          |
| [<span data-ttu-id="c39be-128">**setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="c39be-128">**setItemInfo**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md) | <span data-ttu-id="c39be-129">設定播放清單屬性的值。</span><span class="sxs-lookup"><span data-stu-id="c39be-129">Sets the value of a playlist attribute.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="c39be-130">屬性</span><span class="sxs-lookup"><span data-stu-id="c39be-130">Properties</span></span>

<span data-ttu-id="c39be-131">**IWMPPlaylist (VB 和 c # )** 介面都有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c39be-131">The **IWMPPlaylist (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="c39be-132">屬性</span><span class="sxs-lookup"><span data-stu-id="c39be-132">Property</span></span>                                                                                      | <span data-ttu-id="c39be-133">存取類型</span><span class="sxs-lookup"><span data-stu-id="c39be-133">Access type</span></span>           | <span data-ttu-id="c39be-134">Description</span><span class="sxs-lookup"><span data-stu-id="c39be-134">Description</span></span>                                                                                                                                         |
|:----------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c39be-135">**attributeCount**</span><span class="sxs-lookup"><span data-stu-id="c39be-135">**attributeCount**</span></span>](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)<br/> | <span data-ttu-id="c39be-136">唯讀</span><span class="sxs-lookup"><span data-stu-id="c39be-136">Read-only</span></span><br/>  | <span data-ttu-id="c39be-137">取得與播放清單相關聯的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="c39be-137">Gets the number of attributes associated with a playlist.</span></span><br/>                                                                                |
| [<span data-ttu-id="c39be-138">**attributeName**</span><span class="sxs-lookup"><span data-stu-id="c39be-138">**attributeName**</span></span>](iwmpplaylist-attributename--vb-and-c.md)<br/>                      | <span data-ttu-id="c39be-139">唯讀</span><span class="sxs-lookup"><span data-stu-id="c39be-139">Read-only</span></span><br/>  | <span data-ttu-id="c39be-140">取得索引所指定之播放清單屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="c39be-140">Gets the name of a playlist attribute specified by an index.</span></span> <span data-ttu-id="c39be-141">在 c # 中，這是 get \_ attributeName 方法。</span><span class="sxs-lookup"><span data-stu-id="c39be-141">In C# this is the get\_attributeName method.</span></span><br/>                               |
| [<span data-ttu-id="c39be-142">**count**</span><span class="sxs-lookup"><span data-stu-id="c39be-142">**count**</span></span>](wmplibiwmpplaylist-iwmpplaylist-count--vb-and-c.md)<br/>                   | <span data-ttu-id="c39be-143">唯讀</span><span class="sxs-lookup"><span data-stu-id="c39be-143">Read-only</span></span><br/>  | <span data-ttu-id="c39be-144">取得播放清單中的媒體專案數目。</span><span class="sxs-lookup"><span data-stu-id="c39be-144">Gets the number of media items in a playlist.</span></span><br/>                                                                                            |
| [<span data-ttu-id="c39be-145">**isIdentical**</span><span class="sxs-lookup"><span data-stu-id="c39be-145">**isIdentical**</span></span>](iwmpplaylist-isidentical--vb-and-c.md)<br/>                          | <span data-ttu-id="c39be-146">唯讀</span><span class="sxs-lookup"><span data-stu-id="c39be-146">Read-only</span></span><br/>  | <span data-ttu-id="c39be-147">取得值，指出指定的播放清單是否與目前的播放清單相同。</span><span class="sxs-lookup"><span data-stu-id="c39be-147">Gets a value indicating whether the specified playlist is identical to the current playlist.</span></span> <span data-ttu-id="c39be-148">在 c # 中，這是 get \_ isIdentical 方法。</span><span class="sxs-lookup"><span data-stu-id="c39be-148">In C# this is the get\_isIdentical method.</span></span><br/> |
| [<span data-ttu-id="c39be-149">**項目**</span><span class="sxs-lookup"><span data-stu-id="c39be-149">**Item**</span></span>](iwmpplaylist-item--vb-and-c.md)<br/>                                        | <span data-ttu-id="c39be-150">唯讀</span><span class="sxs-lookup"><span data-stu-id="c39be-150">Read-only</span></span><br/>  | <span data-ttu-id="c39be-151">取得位於指定索引處之媒體專案的介面。</span><span class="sxs-lookup"><span data-stu-id="c39be-151">Gets an interface to the media item at the specified index.</span></span> <span data-ttu-id="c39be-152">在 c # 中，這是取得 \_ 專案方法。</span><span class="sxs-lookup"><span data-stu-id="c39be-152">In C# this is the get\_Item method.</span></span><br/>                                         |
| [<span data-ttu-id="c39be-153">**名字**</span><span class="sxs-lookup"><span data-stu-id="c39be-153">**name**</span></span>](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)<br/>                     | <span data-ttu-id="c39be-154">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c39be-154">Read/write</span></span><br/> | <span data-ttu-id="c39be-155">取得或設定播放清單的名稱。</span><span class="sxs-lookup"><span data-stu-id="c39be-155">Gets or sets the name of the playlist.</span></span><br/>                                                                                                   |



 

<span data-ttu-id="c39be-156">使用透過下列物件或介面存取的下列屬性或方法，取得 **IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="c39be-156">Get an **IWMPPlaylist** interface by using the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="c39be-157">物件或介面</span><span class="sxs-lookup"><span data-stu-id="c39be-157">Object or interface</span></span>                                                | <span data-ttu-id="c39be-158">屬性或方法</span><span class="sxs-lookup"><span data-stu-id="c39be-158">Property or method</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c39be-159">**IWMPCdrom**</span><span class="sxs-lookup"><span data-stu-id="c39be-159">**IWMPCdrom**</span></span>](iwmpcdrom--vb-and-c.md)                           | [<span data-ttu-id="c39be-160">**播放 清單**</span><span class="sxs-lookup"><span data-stu-id="c39be-160">**Playlist**</span></span>](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="c39be-161">**IWMPMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="c39be-161">**IWMPMediaCollection**</span></span>](iwmpmediacollection--vb-and-c.md)       | <span data-ttu-id="c39be-162">[**getAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)、 [**getByAlbum**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum)、 [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)、 [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)、 [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)、 [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)</span><span class="sxs-lookup"><span data-stu-id="c39be-162">[**getAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md), [**getByAlbum**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum), [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md), [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md), [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md), [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)</span></span> |
| [<span data-ttu-id="c39be-163">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="c39be-163">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md)  | <span data-ttu-id="c39be-164">[**currentPlaylist**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)、 [ **[]**](axwmplib-axwindowsmediaplayer-newplaylist.md)</span><span class="sxs-lookup"><span data-stu-id="c39be-164">[**currentPlaylist**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [**newPlaylist**](axwmplib-axwindowsmediaplayer-newplaylist.md)</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="c39be-165">**IWMPPlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="c39be-165">**IWMPPlaylistArray**</span></span>](iwmpplaylistarray--vb-and-c.md)           | [<span data-ttu-id="c39be-166">**項目**</span><span class="sxs-lookup"><span data-stu-id="c39be-166">**Item**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="c39be-167">**IWMPPlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="c39be-167">**IWMPPlaylistCollection**</span></span>](iwmpplaylistcollection--vb-and-c.md) | <span data-ttu-id="c39be-168">[**[]**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)</span><span class="sxs-lookup"><span data-stu-id="c39be-168">[**newPlaylist**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="c39be-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="c39be-169">Requirements</span></span>



| <span data-ttu-id="c39be-170">需求</span><span class="sxs-lookup"><span data-stu-id="c39be-170">Requirement</span></span> | <span data-ttu-id="c39be-171">值</span><span class="sxs-lookup"><span data-stu-id="c39be-171">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c39be-172">標頭</span><span class="sxs-lookup"><span data-stu-id="c39be-172">Header</span></span><br/> | <dl> <span data-ttu-id="c39be-173"><dt>Wmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c39be-173"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c39be-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c39be-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c39be-175">**適用于 Visual Basic .NET 和 C 的介面#**</span><span class="sxs-lookup"><span data-stu-id="c39be-175">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





