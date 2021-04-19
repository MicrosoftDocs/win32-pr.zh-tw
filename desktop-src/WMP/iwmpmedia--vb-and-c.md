---
title: 'IWMPMedia (VB 和 C ) 介面 (h.264. h) '
description: 提供一種方式來設定和取出媒體專案的屬性。IWMPMedia 介面會公開下列屬性。
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- IWMPMedia (VB 和 C ) 介面 Windows Media Player
- IWMPMedia (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPMedia (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c60a3396710ea4c426bd41c96db34e1e59cc690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980163"
---
# <a name="iwmpmedia-vb-and-c-interface"></a><span data-ttu-id="bb154-105">IWMPMedia (VB 和 c # ) 介面</span><span class="sxs-lookup"><span data-stu-id="bb154-105">IWMPMedia (VB and C#) interface</span></span>

<span data-ttu-id="bb154-106">提供一種方式來設定和取出媒體專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="bb154-106">Provides a way to set and retrieve the properties of a media item.</span></span>

<span data-ttu-id="bb154-107">**IWMPMedia** 介面會公開下列屬性。</span><span class="sxs-lookup"><span data-stu-id="bb154-107">The **IWMPMedia** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="bb154-108">成員</span><span class="sxs-lookup"><span data-stu-id="bb154-108">Members</span></span>

<span data-ttu-id="bb154-109">**IWMPMedia (VB 和 c # )** 介面都有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bb154-109">The **IWMPMedia (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="bb154-110">方法</span><span class="sxs-lookup"><span data-stu-id="bb154-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="bb154-111">屬性</span><span class="sxs-lookup"><span data-stu-id="bb154-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bb154-112">方法</span><span class="sxs-lookup"><span data-stu-id="bb154-112">Methods</span></span>

<span data-ttu-id="bb154-113">**IWMPMedia (VB 和 c # )** 介面都有這些方法。</span><span class="sxs-lookup"><span data-stu-id="bb154-113">The **IWMPMedia (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="bb154-114">方法</span><span class="sxs-lookup"><span data-stu-id="bb154-114">Method</span></span>                                                                             | <span data-ttu-id="bb154-115">描述</span><span class="sxs-lookup"><span data-stu-id="bb154-115">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb154-116">**getAttributeName**</span><span class="sxs-lookup"><span data-stu-id="bb154-116">**getAttributeName**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | <span data-ttu-id="bb154-117">傳回對應至指定之索引的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="bb154-117">Returns the name of the attribute corresponding to the specified index.</span></span><br/>                            |
| [<span data-ttu-id="bb154-118">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="bb154-118">**getItemInfo**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | <span data-ttu-id="bb154-119">傳回媒體專案的指定屬性值。</span><span class="sxs-lookup"><span data-stu-id="bb154-119">Returns the value of the specified attribute for the media item.</span></span><br/>                                   |
| [<span data-ttu-id="bb154-120">**getItemInfoByAtom**</span><span class="sxs-lookup"><span data-stu-id="bb154-120">**getItemInfoByAtom**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | <span data-ttu-id="bb154-121">傳回具有指定之索引編號的屬性值。</span><span class="sxs-lookup"><span data-stu-id="bb154-121">Returns the value of the attribute with the specified index number.</span></span><br/>                                |
| [<span data-ttu-id="bb154-122">**getMarkerName**</span><span class="sxs-lookup"><span data-stu-id="bb154-122">**getMarkerName**</span></span>](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | <span data-ttu-id="bb154-123">傳回指定索引處的標記名稱。</span><span class="sxs-lookup"><span data-stu-id="bb154-123">Returns the name of the marker at the specified index.</span></span><br/>                                             |
| [<span data-ttu-id="bb154-124">**getMarkerTime**</span><span class="sxs-lookup"><span data-stu-id="bb154-124">**getMarkerTime**</span></span>](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | <span data-ttu-id="bb154-125">傳回指定索引處之標記的時間。</span><span class="sxs-lookup"><span data-stu-id="bb154-125">Returns the time of the marker at the specified index.</span></span><br/>                                             |
| [<span data-ttu-id="bb154-126">**isMemberOf**</span><span class="sxs-lookup"><span data-stu-id="bb154-126">**isMemberOf**</span></span>](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | <span data-ttu-id="bb154-127">傳回值，指出指定的媒體專案是否為指定播放清單的成員。</span><span class="sxs-lookup"><span data-stu-id="bb154-127">Returns a value indicating whether the specified media item is a member of the specified playlist.</span></span><br/> |
| [<span data-ttu-id="bb154-128">**isReadOnlyItem**</span><span class="sxs-lookup"><span data-stu-id="bb154-128">**isReadOnlyItem**</span></span>](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | <span data-ttu-id="bb154-129">傳回值，這個值表示是否可以編輯指定之媒體專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="bb154-129">Returns a value indicating whether the attributes of the specified media item can be edited.</span></span><br/>       |
| [<span data-ttu-id="bb154-130">**setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="bb154-130">**setItemInfo**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | <span data-ttu-id="bb154-131">設定媒體專案的指定屬性值。</span><span class="sxs-lookup"><span data-stu-id="bb154-131">Sets the value of the specified attribute for the media item.</span></span><br/>                                      |



 

### <a name="properties"></a><span data-ttu-id="bb154-132">屬性</span><span class="sxs-lookup"><span data-stu-id="bb154-132">Properties</span></span>

<span data-ttu-id="bb154-133">**IWMPMedia (VB 和 c # )** 介面都有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bb154-133">The **IWMPMedia (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="bb154-134">屬性</span><span class="sxs-lookup"><span data-stu-id="bb154-134">Property</span></span>                                                                                      | <span data-ttu-id="bb154-135">存取類型</span><span class="sxs-lookup"><span data-stu-id="bb154-135">Access type</span></span>          | <span data-ttu-id="bb154-136">Description</span><span class="sxs-lookup"><span data-stu-id="bb154-136">Description</span></span>                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb154-137">**attributeCount**</span><span class="sxs-lookup"><span data-stu-id="bb154-137">**attributeCount**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | <span data-ttu-id="bb154-138">唯讀</span><span class="sxs-lookup"><span data-stu-id="bb154-138">Read-only</span></span><br/> | <span data-ttu-id="bb154-139">取得可針對媒體專案查詢及/或設定的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="bb154-139">Gets the number of attributes that can be queried and/or set for the media item.</span></span><br/>                                                          |
| [<span data-ttu-id="bb154-140">**時間**</span><span class="sxs-lookup"><span data-stu-id="bb154-140">**duration**</span></span>](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | <span data-ttu-id="bb154-141">唯讀</span><span class="sxs-lookup"><span data-stu-id="bb154-141">Read-only</span></span><br/> | <span data-ttu-id="bb154-142">取得目前媒體專案的持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="bb154-142">Gets the duration in seconds of the current media item.</span></span><br/>                                                                                   |
| [<span data-ttu-id="bb154-143">**durationString**</span><span class="sxs-lookup"><span data-stu-id="bb154-143">**durationString**</span></span>](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | <span data-ttu-id="bb154-144">唯讀</span><span class="sxs-lookup"><span data-stu-id="bb154-144">Read-only</span></span><br/> | <span data-ttu-id="bb154-145">取得值，指出目前媒體專案的持續時間（以 HH： MM： SS 格式表示）。</span><span class="sxs-lookup"><span data-stu-id="bb154-145">Gets a value indicating the duration of the current media item in HH:MM:SS format.</span></span><br/>                                                        |
| [<span data-ttu-id="bb154-146">**imageSourceHeight**</span><span class="sxs-lookup"><span data-stu-id="bb154-146">**imageSourceHeight**</span></span>](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | <span data-ttu-id="bb154-147">唯讀</span><span class="sxs-lookup"><span data-stu-id="bb154-147">Read-only</span></span><br/> | <span data-ttu-id="bb154-148">取得目前媒體專案的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="bb154-148">Gets the height of the current media item in pixels.</span></span><br/>                                                                                      |
| [<span data-ttu-id="bb154-149">**imageSourceWidth**</span><span class="sxs-lookup"><span data-stu-id="bb154-149">**imageSourceWidth**</span></span>](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | <span data-ttu-id="bb154-150">唯讀</span><span class="sxs-lookup"><span data-stu-id="bb154-150">Read-only</span></span><br/> | <span data-ttu-id="bb154-151">取得目前媒體專案的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="bb154-151">Gets the width of the current media item in pixels.</span></span><br/>                                                                                       |
| [<span data-ttu-id="bb154-152">**isIdentical**</span><span class="sxs-lookup"><span data-stu-id="bb154-152">**isIdentical**</span></span>](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | <span data-ttu-id="bb154-153">唯讀</span><span class="sxs-lookup"><span data-stu-id="bb154-153">Read-only</span></span><br/> | <span data-ttu-id="bb154-154">取得值，指出指定的媒體專案是否與目前的專案相同。</span><span class="sxs-lookup"><span data-stu-id="bb154-154">Gets a value indicating whether the specified media item is the same as the current one.</span></span> <span data-ttu-id="bb154-155">在 c # 中，這是 **get \_ isIdentical** 方法。</span><span class="sxs-lookup"><span data-stu-id="bb154-155">In C#, this is the **get\_isIdentical** method.</span></span><br/> |
| [<span data-ttu-id="bb154-156">**markerCount**</span><span class="sxs-lookup"><span data-stu-id="bb154-156">**markerCount**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | <span data-ttu-id="bb154-157">唯讀</span><span class="sxs-lookup"><span data-stu-id="bb154-157">Read-only</span></span><br/> | <span data-ttu-id="bb154-158">取得媒體專案中的標記數目。</span><span class="sxs-lookup"><span data-stu-id="bb154-158">Gets the number of markers in the media item.</span></span><br/>                                                                                             |
| [<span data-ttu-id="bb154-159">**名字**</span><span class="sxs-lookup"><span data-stu-id="bb154-159">**name**</span></span>](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | <span data-ttu-id="bb154-160">唯讀</span><span class="sxs-lookup"><span data-stu-id="bb154-160">Read-only</span></span><br/> | <span data-ttu-id="bb154-161">取得或設定媒體專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb154-161">Gets or sets the name of the media item.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="bb154-162">**sourceURL**</span><span class="sxs-lookup"><span data-stu-id="bb154-162">**sourceURL**</span></span>](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | <span data-ttu-id="bb154-163">唯讀</span><span class="sxs-lookup"><span data-stu-id="bb154-163">Read-only</span></span><br/> | <span data-ttu-id="bb154-164">取得媒體專案的 URL。</span><span class="sxs-lookup"><span data-stu-id="bb154-164">Gets the URL of the media item.</span></span><br/>                                                                                                           |



 

<span data-ttu-id="bb154-165">使用透過下列物件或介面存取的下列屬性或方法，取得 **IWMPMedia** 介面。</span><span class="sxs-lookup"><span data-stu-id="bb154-165">Get an **IWMPMedia** interface by using the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="bb154-166">物件或介面</span><span class="sxs-lookup"><span data-stu-id="bb154-166">Object or interface</span></span>                                               | <span data-ttu-id="bb154-167">屬性或方法</span><span class="sxs-lookup"><span data-stu-id="bb154-167">Property or method</span></span>                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb154-168">**IWMPControls**</span><span class="sxs-lookup"><span data-stu-id="bb154-168">**IWMPControls**</span></span>](iwmpcontrols--vb-and-c.md)                    | [<span data-ttu-id="bb154-169">**currentitem**</span><span class="sxs-lookup"><span data-stu-id="bb154-169">**currentitem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [<span data-ttu-id="bb154-170">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="bb154-170">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="bb154-171">[**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)、 [ **newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="bb154-171">[**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [**newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="bb154-172">**IWMPPlaylist**</span><span class="sxs-lookup"><span data-stu-id="bb154-172">**IWMPPlaylist**</span></span>](iwmpplaylist--vb-and-c.md)                    | <span data-ttu-id="bb154-173">[](iwmpplaylist-item--vb-and-c.md) \_ 在 c # 中取得專案 (專案 ) </span><span class="sxs-lookup"><span data-stu-id="bb154-173">[**Item**](iwmpplaylist-item--vb-and-c.md) (get\_Item in C#)</span></span>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="bb154-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb154-174">Requirements</span></span>



| <span data-ttu-id="bb154-175">需求</span><span class="sxs-lookup"><span data-stu-id="bb154-175">Requirement</span></span> | <span data-ttu-id="bb154-176">值</span><span class="sxs-lookup"><span data-stu-id="bb154-176">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb154-177">標頭</span><span class="sxs-lookup"><span data-stu-id="bb154-177">Header</span></span><br/> | <dl> <span data-ttu-id="bb154-178"><dt>Wmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb154-178"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb154-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb154-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb154-180">**適用于 Visual Basic .NET 和 C 的介面#**</span><span class="sxs-lookup"><span data-stu-id="bb154-180">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="bb154-181">**IWMPMedia2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bb154-181">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bb154-182">**IWMPMedia3 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bb154-182">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





