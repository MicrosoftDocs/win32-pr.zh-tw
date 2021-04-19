---
title: sourceFilter 元素
description: SourceFilter 元素包含可從程式庫中選取專案的元素。
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- sourceFilter 元素 Windows Media Player
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb43a9577c5fe8857b63067db5be90d314037b84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999671"
---
# <a name="sourcefilter-element"></a><span data-ttu-id="b2874-104">sourceFilter 元素</span><span class="sxs-lookup"><span data-stu-id="b2874-104">sourceFilter Element</span></span>

<span data-ttu-id="b2874-105">**SourceFilter** 元素包含可從程式庫中選取專案的元素。</span><span class="sxs-lookup"><span data-stu-id="b2874-105">The **sourceFilter** element contains elements that select items from a library.</span></span>

``` syntax
<sourceFilter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</sourceFilter>
```

## <a name="attributes"></a><span data-ttu-id="b2874-106">屬性</span><span class="sxs-lookup"><span data-stu-id="b2874-106">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="b2874-107"><span id="type"></span><span id="TYPE"></span>**類型**</span><span class="sxs-lookup"><span data-stu-id="b2874-107"><span id="type"></span><span id="TYPE"></span>**type**</span></span>
</dt> <dd>

<span data-ttu-id="b2874-108">篩選物件的型別。</span><span class="sxs-lookup"><span data-stu-id="b2874-108">The type of filter object.</span></span> <span data-ttu-id="b2874-109">這個屬性沒有預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="b2874-109">There are no predefined values for this attribute.</span></span>

</dd> <dt>

<span data-ttu-id="b2874-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>需要 (**識別碼**) </span><span class="sxs-lookup"><span data-stu-id="b2874-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="b2874-111">可唯一識別來源篩選物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b2874-111">The GUID that uniquely identifies the source filter object.</span></span> <span data-ttu-id="b2874-112">系統會叫用來源篩選物件的方法，以解讀 **sourceFilter** 元素中包含的 **片段** 元素。</span><span class="sxs-lookup"><span data-stu-id="b2874-112">The source filter object's methods are invoked to interpret the **fragment** elements contained in the **sourceFilter** element.</span></span>



| <span data-ttu-id="b2874-113">值</span><span class="sxs-lookup"><span data-stu-id="b2874-113">Value</span></span>                                  | <span data-ttu-id="b2874-114">描述</span><span class="sxs-lookup"><span data-stu-id="b2874-114">Description</span></span>                                              |
|----------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="b2874-115">{4202947A-A563-4B05-A754-A1B4B5989849}</span><span class="sxs-lookup"><span data-stu-id="b2874-115">{4202947A-A563-4B05-A754-A1B4B5989849}</span></span> | <span data-ttu-id="b2874-116">「我的媒體櫃中的音樂」來源篩選的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b2874-116">The GUID for the "Music in my library" source filter.</span></span>    |
| <span data-ttu-id="b2874-117">{B2D9BDDC-8E49-444B-9BA4-193ABF9C7870}</span><span class="sxs-lookup"><span data-stu-id="b2874-117">{B2D9BDDC-8E49-444B-9BA4-193ABF9C7870}</span></span> | <span data-ttu-id="b2874-118">「我的媒體櫃中的影片」來源篩選的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b2874-118">The GUID for the "Video in my library" source filter.</span></span>    |
| <span data-ttu-id="b2874-119">{CC823400-A8E4-4081-B073-D3B6D952FE69}</span><span class="sxs-lookup"><span data-stu-id="b2874-119">{CC823400-A8E4-4081-B073-D3B6D952FE69}</span></span> | <span data-ttu-id="b2874-120">「我的媒體櫃中的圖片」來源篩選的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b2874-120">The GUID for the "Pictures in my library" source filter.</span></span> |
| <span data-ttu-id="b2874-121">{E5415A66-7763-4BDE-B97F-5557CA73C303}</span><span class="sxs-lookup"><span data-stu-id="b2874-121">{E5415A66-7763-4BDE-B97F-5557CA73C303}</span></span> | <span data-ttu-id="b2874-122">「我的媒體櫃中的電視節目」來源篩選的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b2874-122">The GUID for the "TV shows in my library" source filter.</span></span> |



 

</dd> <dt>

<span data-ttu-id="b2874-123"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>需要 (**名稱**) </span><span class="sxs-lookup"><span data-stu-id="b2874-123"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="b2874-124">篩選物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2874-124">The name of the filter object.</span></span>



| <span data-ttu-id="b2874-125">值</span><span class="sxs-lookup"><span data-stu-id="b2874-125">Value</span></span>                  | <span data-ttu-id="b2874-126">描述</span><span class="sxs-lookup"><span data-stu-id="b2874-126">Description</span></span>                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2874-127">媒體櫃中的音樂</span><span class="sxs-lookup"><span data-stu-id="b2874-127">Music in my library</span></span>    | <span data-ttu-id="b2874-128">篩選物件，可從使用者程式庫中的一組音樂專案選取指定的專案。</span><span class="sxs-lookup"><span data-stu-id="b2874-128">A filter object that selects specified items from the set of music items in the user's library.</span></span> |
| <span data-ttu-id="b2874-129">媒體櫃中的影片</span><span class="sxs-lookup"><span data-stu-id="b2874-129">Video in my library</span></span>    | <span data-ttu-id="b2874-130">篩選物件，它會從使用者程式庫中的一組影片專案選取指定的專案。</span><span class="sxs-lookup"><span data-stu-id="b2874-130">A filter object that selects specified items from the set of video items in the user's library.</span></span> |
| <span data-ttu-id="b2874-131">媒體櫃中的圖片</span><span class="sxs-lookup"><span data-stu-id="b2874-131">Pictures in my library</span></span> | <span data-ttu-id="b2874-132">篩選物件，可從使用者程式庫中的一組相片專案選取指定的專案。</span><span class="sxs-lookup"><span data-stu-id="b2874-132">A filter object that selects specified items from the set of photo items in the user's library.</span></span> |
| <span data-ttu-id="b2874-133">媒體櫃中的電視節目</span><span class="sxs-lookup"><span data-stu-id="b2874-133">TV shows in my library</span></span> | <span data-ttu-id="b2874-134">篩選物件，可從使用者程式庫中的電視專案集合中選取指定的專案。</span><span class="sxs-lookup"><span data-stu-id="b2874-134">A filter object that selects specified items from the set of TV items in the user's library.</span></span>    |



 

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="b2874-135">父/子項目</span><span class="sxs-lookup"><span data-stu-id="b2874-135">Parent/Child Elements</span></span>



| <span data-ttu-id="b2874-136">階層</span><span class="sxs-lookup"><span data-stu-id="b2874-136">Hierarchy</span></span> | <span data-ttu-id="b2874-137">元素</span><span class="sxs-lookup"><span data-stu-id="b2874-137">Elements</span></span>                         |
|-----------|----------------------------------|
| <span data-ttu-id="b2874-138">父代</span><span class="sxs-lookup"><span data-stu-id="b2874-138">Parent</span></span>    | [<span data-ttu-id="b2874-139">querySet</span><span class="sxs-lookup"><span data-stu-id="b2874-139">querySet</span></span>](queryset-element.md) |
| <span data-ttu-id="b2874-140">子系</span><span class="sxs-lookup"><span data-stu-id="b2874-140">Child</span></span>     | [<span data-ttu-id="b2874-141">片段</span><span class="sxs-lookup"><span data-stu-id="b2874-141">fragment</span></span>](fragment-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="b2874-142">備註</span><span class="sxs-lookup"><span data-stu-id="b2874-142">Remarks</span></span>

<span data-ttu-id="b2874-143">**SourceFilter** 元素會從程式庫中選取專案，而不考慮結果集的大小。</span><span class="sxs-lookup"><span data-stu-id="b2874-143">The **sourceFilter** element selects items from the library without regard for the size of the result set.</span></span> <span data-ttu-id="b2874-144">另一方面， **filter** 元素會限制結果集的大小。</span><span class="sxs-lookup"><span data-stu-id="b2874-144">The **filter** element, on the other hand, limits the size of the result set.</span></span>

## <a name="examples"></a><span data-ttu-id="b2874-145">範例</span><span class="sxs-lookup"><span data-stu-id="b2874-145">Examples</span></span>


```
<sourceFilter 
    type = "smartFilterObject" 
    id = "{4202947A-A563-4B05-A754-A1B4B5989849}" 
    name = "Music in my library">
        <fragment name = "Genre">
            <argument name = "condition">Is</argument>
            <argument name = "value">Rock</argument>
        </fragment>
        <fragment name = "Album Artist">
            <argument name = "condition">Is Not</argument>
            <argument name = "value">Brenda Diaz</argument>
        </fragment>
</sourceFilter>
```



## <a name="requirements"></a><span data-ttu-id="b2874-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2874-146">Requirements</span></span>



| <span data-ttu-id="b2874-147">需求</span><span class="sxs-lookup"><span data-stu-id="b2874-147">Requirement</span></span> | <span data-ttu-id="b2874-148">值</span><span class="sxs-lookup"><span data-stu-id="b2874-148">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="b2874-149">版本</span><span class="sxs-lookup"><span data-stu-id="b2874-149">Version</span></span><br/> | <span data-ttu-id="b2874-150">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="b2874-150">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2874-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2874-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2874-152">**filter 元素**</span><span class="sxs-lookup"><span data-stu-id="b2874-152">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="b2874-153">**片段元素**</span><span class="sxs-lookup"><span data-stu-id="b2874-153">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="b2874-154">**querySet 元素**</span><span class="sxs-lookup"><span data-stu-id="b2874-154">**querySet Element**</span></span>](queryset-element.md)
</dt> <dt>

[<span data-ttu-id="b2874-155">**Windows Media 播放清單元素參考**</span><span class="sxs-lookup"><span data-stu-id="b2874-155">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





