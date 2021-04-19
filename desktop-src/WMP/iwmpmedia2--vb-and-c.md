---
title: 'IWMPMedia2 (VB 和 C ) 介面 (h.264. h) '
description: 提供其他媒體專案屬性的存取權。
ms.assetid: 7d9f8304-ae26-4175-b9d4-9f272861ef87
keywords:
- IWMPMedia2 (VB 和 C ) 介面 Windows Media Player
- IWMPMedia2 (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPMedia2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1a77322e0e6649d9a286c920ccd9ddc77890f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997450"
---
# <a name="iwmpmedia2-vb-and-c-interface"></a><span data-ttu-id="0cb12-105">IWMPMedia2 (VB 和 c # ) 介面</span><span class="sxs-lookup"><span data-stu-id="0cb12-105">IWMPMedia2 (VB and C#) interface</span></span>

<span data-ttu-id="0cb12-106">提供其他媒體專案屬性的存取權。</span><span class="sxs-lookup"><span data-stu-id="0cb12-106">Provides access to an additional media item property.</span></span>

<span data-ttu-id="0cb12-107">除了繼承自 **IWMPMedia** 的屬性和方法之外， **IWMPMedia2** 介面也會公開下列屬性。</span><span class="sxs-lookup"><span data-stu-id="0cb12-107">In addition to the properties and methods inherited from **IWMPMedia**, the **IWMPMedia2** interface exposes the following property.</span></span>



| <span data-ttu-id="0cb12-108">屬性</span><span class="sxs-lookup"><span data-stu-id="0cb12-108">Property</span></span>                                                 | <span data-ttu-id="0cb12-109">描述</span><span class="sxs-lookup"><span data-stu-id="0cb12-109">Description</span></span>                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="0cb12-110">錯誤</span><span class="sxs-lookup"><span data-stu-id="0cb12-110">Error</span></span>](wmplibiwmpmedia2-iwmpmedia2-error--vb-and-c.md) | <span data-ttu-id="0cb12-111">取得 **IWMPErrorItem** 介面（如果媒體專案有錯誤狀況）。</span><span class="sxs-lookup"><span data-stu-id="0cb12-111">Gets an **IWMPErrorItem** interface if the media item has an error condition.</span></span> |



 

<span data-ttu-id="0cb12-112">藉由轉換下列其中一個屬性所傳回的值，或透過下列物件或介面所存取的方法，來取得 **IWMPMedia2** 介面。</span><span class="sxs-lookup"><span data-stu-id="0cb12-112">Get an **IWMPMedia2** interface by casting the value returned by one of the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="0cb12-113">物件或介面</span><span class="sxs-lookup"><span data-stu-id="0cb12-113">Object or interface</span></span>                                               | <span data-ttu-id="0cb12-114">屬性或方法</span><span class="sxs-lookup"><span data-stu-id="0cb12-114">Property or method</span></span>                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0cb12-115">IWMPControls</span><span class="sxs-lookup"><span data-stu-id="0cb12-115">IWMPControls</span></span>](iwmpcontrols--vb-and-c.md)                        | [<span data-ttu-id="0cb12-116">currentItem</span><span class="sxs-lookup"><span data-stu-id="0cb12-116">currentItem</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [<span data-ttu-id="0cb12-117">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="0cb12-117">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="0cb12-118">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) 、 [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="0cb12-118">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="0cb12-119">IWMPPlaylist</span><span class="sxs-lookup"><span data-stu-id="0cb12-119">IWMPPlaylist</span></span>](iwmpplaylist--vb-and-c.md)                        | <span data-ttu-id="0cb12-120">在 c # 中 **取得 \_ 專案** ([專案](iwmpplaylist-item--vb-and-c.md)) </span><span class="sxs-lookup"><span data-stu-id="0cb12-120">[Item](iwmpplaylist-item--vb-and-c.md) ( **get\_Item** in C#)</span></span>                                                                   |



 

## <a name="members"></a><span data-ttu-id="0cb12-121">成員</span><span class="sxs-lookup"><span data-stu-id="0cb12-121">Members</span></span>

<span data-ttu-id="0cb12-122">**IWMPMedia2 (VB 和 c # )** 介面不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="0cb12-122">The **IWMPMedia2 (VB and C#)** interface does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb12-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cb12-123">Requirements</span></span>



| <span data-ttu-id="0cb12-124">需求</span><span class="sxs-lookup"><span data-stu-id="0cb12-124">Requirement</span></span> | <span data-ttu-id="0cb12-125">值</span><span class="sxs-lookup"><span data-stu-id="0cb12-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cb12-126">標頭</span><span class="sxs-lookup"><span data-stu-id="0cb12-126">Header</span></span><br/> | <dl> <span data-ttu-id="0cb12-127"><dt>Wmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="0cb12-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cb12-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cb12-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb12-129">**適用于 Visual Basic .NET 和 C 的介面#**</span><span class="sxs-lookup"><span data-stu-id="0cb12-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="0cb12-130">**IWMPErrorItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="0cb12-130">**IWMPErrorItem (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0cb12-131">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="0cb12-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0cb12-132">**IWMPMedia3 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="0cb12-132">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





