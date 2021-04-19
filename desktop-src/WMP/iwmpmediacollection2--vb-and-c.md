---
title: 'IWMPMediaCollection2 (VB 和 C ) 介面 (h.264. h) '
description: 提供補充 IWMPMediaCollection 介面的方法。
ms.assetid: 204f336c-ea78-43d4-9686-bcab72362bc9
keywords:
- IWMPMediaCollection2 (VB 和 C ) 介面 Windows Media Player
- IWMPMediaCollection2 (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPMediaCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58175e80fbf0f706a9ae6c6b3b69afbd26d52af3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976125"
---
# <a name="iwmpmediacollection2-vb-and-c-interface"></a><span data-ttu-id="3d202-105">IWMPMediaCollection2 (VB 和 c # ) 介面</span><span class="sxs-lookup"><span data-stu-id="3d202-105">IWMPMediaCollection2 (VB and C#) interface</span></span>

<span data-ttu-id="3d202-106">提供補充 **IWMPMediaCollection** 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="3d202-106">Provides methods that supplement the **IWMPMediaCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="3d202-107">成員</span><span class="sxs-lookup"><span data-stu-id="3d202-107">Members</span></span>

<span data-ttu-id="3d202-108">**IWMPMediaCollection2 (VB 和 c # )** 介面都有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3d202-108">The **IWMPMediaCollection2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="3d202-109">方法</span><span class="sxs-lookup"><span data-stu-id="3d202-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3d202-110">方法</span><span class="sxs-lookup"><span data-stu-id="3d202-110">Methods</span></span>

<span data-ttu-id="3d202-111">**IWMPMediaCollection2 (VB 和 c # )** 介面都有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3d202-111">The **IWMPMediaCollection2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="3d202-112">方法</span><span class="sxs-lookup"><span data-stu-id="3d202-112">Method</span></span>                                                                                                                     | <span data-ttu-id="3d202-113">描述</span><span class="sxs-lookup"><span data-stu-id="3d202-113">Description</span></span>                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d202-114">**createQuery**</span><span class="sxs-lookup"><span data-stu-id="3d202-114">**createQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)                               | <span data-ttu-id="3d202-115">傳回代表新查詢的 **IWMPQuery** 介面。</span><span class="sxs-lookup"><span data-stu-id="3d202-115">Returns an **IWMPQuery** interface that represents a new query.</span></span><br/>                                                                                               |
| [<span data-ttu-id="3d202-116">**getByAttributeAndMediaType**</span><span class="sxs-lookup"><span data-stu-id="3d202-116">**getByAttributeAndMediaType**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getbyattributeandmediatype--vb-and-c.md) | <span data-ttu-id="3d202-117">傳回 **IWMPPlaylist** 介面，這個介面會提供具有指定屬性和媒體類型之媒體專案的存取權。</span><span class="sxs-lookup"><span data-stu-id="3d202-117">Returns an **IWMPPlaylist** interface that provides access to media items that have a specified attribute and media type.</span></span><br/>                                     |
| [<span data-ttu-id="3d202-118">**getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="3d202-118">**getPlaylistByQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)                 | <span data-ttu-id="3d202-119">傳回 **IWMPPlaylist** 介面，這個介面會提供符合查詢準則之媒體專案的存取權。</span><span class="sxs-lookup"><span data-stu-id="3d202-119">Returns an **IWMPPlaylist** interface that provides access to media items that match the query conditions.</span></span><br/>                                                    |
| [<span data-ttu-id="3d202-120">**getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="3d202-120">**getStringCollectionByQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md) | <span data-ttu-id="3d202-121">傳回 **IWMPStringCollection** 介面，這個介面可讓您存取符合查詢準則之指定屬性的所有字串值集。</span><span class="sxs-lookup"><span data-stu-id="3d202-121">Returns an **IWMPStringCollection** interface that provides access to the set of all string values for a specified attribute that match the query conditions.</span></span><br/> |



 

<span data-ttu-id="3d202-122">藉由轉換 [**AxWindowsMediaPlayer mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)屬性所傳回的值，或由 [**IWMPLibrary. mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)屬性傳回的值來取得 **IWMPMediaCollection2** 介面。</span><span class="sxs-lookup"><span data-stu-id="3d202-122">Get an **IWMPMediaCollection2** interface by casting the value returned by the [**AxWindowsMediaPlayer.mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) property or the value returned by the [**IWMPLibrary.mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d202-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d202-123">Requirements</span></span>



| <span data-ttu-id="3d202-124">需求</span><span class="sxs-lookup"><span data-stu-id="3d202-124">Requirement</span></span> | <span data-ttu-id="3d202-125">值</span><span class="sxs-lookup"><span data-stu-id="3d202-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3d202-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3d202-126">Header</span></span><br/> | <dl> <span data-ttu-id="3d202-127"><dt>Wmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d202-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d202-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d202-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d202-129">**適用于 Visual Basic .NET 和 C 的介面#**</span><span class="sxs-lookup"><span data-stu-id="3d202-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="3d202-130">**IWMPMediaCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3d202-130">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





