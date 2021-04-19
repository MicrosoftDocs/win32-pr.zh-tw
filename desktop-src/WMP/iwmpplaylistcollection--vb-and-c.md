---
title: 'IWMPPlaylistCollection (VB 和 C ) 介面 (h.264. h) '
description: 提供在集合中操作 IWMPPlaylist 和 IWMPPlaylistArray 介面的方法。
ms.assetid: 19a4e0d7-cb3f-42ec-9acb-7ac0c5837662
keywords:
- IWMPPlaylistCollection (VB 和 C ) 介面 Windows Media Player
- IWMPPlaylistCollection (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection (VB and C )
- IWMPPlaylistCollection (VB and C ).setDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccc97f9e98838fedc3bd5441d6bfda2da5319dd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995916"
---
# <a name="iwmpplaylistcollection-vb-and-c-interface"></a><span data-ttu-id="d8313-105">IWMPPlaylistCollection (VB 和 c # ) 介面</span><span class="sxs-lookup"><span data-stu-id="d8313-105">IWMPPlaylistCollection (VB and C#) interface</span></span>

<span data-ttu-id="d8313-106">提供在集合中操作 **IWMPPlaylist** 和 **IWMPPlaylistArray** 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="d8313-106">Provides methods for manipulating **IWMPPlaylist** and **IWMPPlaylistArray** interfaces in a collection.</span></span>

## <a name="members"></a><span data-ttu-id="d8313-107">成員</span><span class="sxs-lookup"><span data-stu-id="d8313-107">Members</span></span>

<span data-ttu-id="d8313-108">**IWMPPlaylistCollection (VB 和 c # )** 介面都有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d8313-108">The **IWMPPlaylistCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="d8313-109">方法</span><span class="sxs-lookup"><span data-stu-id="d8313-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d8313-110">方法</span><span class="sxs-lookup"><span data-stu-id="d8313-110">Methods</span></span>

<span data-ttu-id="d8313-111">**IWMPPlaylistCollection (VB 和 c # )** 介面都有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d8313-111">The **IWMPPlaylistCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="d8313-112">方法</span><span class="sxs-lookup"><span data-stu-id="d8313-112">Method</span></span>                                                                                                 | <span data-ttu-id="d8313-113">描述</span><span class="sxs-lookup"><span data-stu-id="d8313-113">Description</span></span>                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8313-114">**getAll**</span><span class="sxs-lookup"><span data-stu-id="d8313-114">**getAll**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)                 | <span data-ttu-id="d8313-115">傳回 **IWMPPlaylistArray** 介面，此介面可讓您存取媒體櫃中的所有播放清單。</span><span class="sxs-lookup"><span data-stu-id="d8313-115">Returns an **IWMPPlaylistArray** interface that provides access to all of the playlists in the library.</span></span><br/>             |
| [<span data-ttu-id="d8313-116">**getByName**</span><span class="sxs-lookup"><span data-stu-id="d8313-116">**getByName**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)           | <span data-ttu-id="d8313-117">傳回 **IWMPPlaylistArray** 介面，這個介面會提供具有指定名稱的播放清單存取權（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="d8313-117">Returns an **IWMPPlaylistArray** interface that provides access to playlists with the specified name, if any exist.</span></span><br/> |
| [<span data-ttu-id="d8313-118">**importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="d8313-118">**importPlaylist**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md) | <span data-ttu-id="d8313-119">將靜態播放清單新增至程式庫。</span><span class="sxs-lookup"><span data-stu-id="d8313-119">Adds a static playlist to the library.</span></span><br/>                                                                              |
| [<span data-ttu-id="d8313-120">**isDeleted**</span><span class="sxs-lookup"><span data-stu-id="d8313-120">**isDeleted**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-isdeleted--vb-and-c.md)           | <span data-ttu-id="d8313-121">傳回值，指出指定的播放清單是否在 [刪除的專案] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="d8313-121">Returns a value indicating whether the specified playlist is in the deleted items folder.</span></span><br/>                           |
| <span data-ttu-id="d8313-122">[**[]**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)</span><span class="sxs-lookup"><span data-stu-id="d8313-122">[**newPlaylist**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)</span></span>       | <span data-ttu-id="d8313-123">傳回程式庫中新的空白播放清單的 **IWMPPlaylist** 介面。</span><span class="sxs-lookup"><span data-stu-id="d8313-123">Returns an **IWMPPlaylist** interface for a new, empty playlist in the library.</span></span><br/>                                     |
| [<span data-ttu-id="d8313-124">**刪除**</span><span class="sxs-lookup"><span data-stu-id="d8313-124">**remove**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-remove--vb-and-c.md)                 | <span data-ttu-id="d8313-125">從媒體櫃移除播放清單。</span><span class="sxs-lookup"><span data-stu-id="d8313-125">Removes a playlist from the library.</span></span><br/>                                                                                |
| <span data-ttu-id="d8313-126">**setDeleted**</span><span class="sxs-lookup"><span data-stu-id="d8313-126">**setDeleted**</span></span>                                                                                         | <span data-ttu-id="d8313-127">不再支援。</span><span class="sxs-lookup"><span data-stu-id="d8313-127">No longer supported.</span></span><br/>                                                                                                |



 

<span data-ttu-id="d8313-128">使用下列屬性來取得 **IWMPPlaylistCollection** 介面。</span><span class="sxs-lookup"><span data-stu-id="d8313-128">Get an **IWMPPlaylistCollection** interface by using the following property.</span></span>



| <span data-ttu-id="d8313-129">Object</span><span class="sxs-lookup"><span data-stu-id="d8313-129">Object</span></span>                                                                   | <span data-ttu-id="d8313-130">屬性</span><span class="sxs-lookup"><span data-stu-id="d8313-130">Property</span></span>                                                                                 |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8313-131">AxWindowsMediaPlayer 物件</span><span class="sxs-lookup"><span data-stu-id="d8313-131">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="d8313-132">**playlistCollection**</span><span class="sxs-lookup"><span data-stu-id="d8313-132">**playlistCollection**</span></span>](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="d8313-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8313-133">Requirements</span></span>



| <span data-ttu-id="d8313-134">需求</span><span class="sxs-lookup"><span data-stu-id="d8313-134">Requirement</span></span> | <span data-ttu-id="d8313-135">值</span><span class="sxs-lookup"><span data-stu-id="d8313-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d8313-136">標頭</span><span class="sxs-lookup"><span data-stu-id="d8313-136">Header</span></span><br/> | <dl> <span data-ttu-id="d8313-137"><dt>Wmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d8313-137"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8313-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8313-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8313-139">**適用于 Visual Basic .NET 和 C 的介面#**</span><span class="sxs-lookup"><span data-stu-id="d8313-139">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="d8313-140">**IWMPPlaylist 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d8313-140">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d8313-141">**IWMPPlaylistArray 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d8313-141">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





