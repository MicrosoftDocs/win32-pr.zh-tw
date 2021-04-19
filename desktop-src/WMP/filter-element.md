---
title: filter 元素
description: 篩選元素包含的元素會限制播放清單的大小、播放清單的持續時間，或播放清單中的媒體專案數。
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- 篩選元素 Windows Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32d2d306faebef813996b59575220efeba99dfb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984011"
---
# <a name="filter-element"></a><span data-ttu-id="07982-104">filter 元素</span><span class="sxs-lookup"><span data-stu-id="07982-104">filter Element</span></span>

<span data-ttu-id="07982-105">**篩選** 元素包含的元素會限制播放清單的大小、播放清單的持續時間，或播放清單中的媒體專案數。</span><span class="sxs-lookup"><span data-stu-id="07982-105">The **filter** element contains elements that limit the size of a playlist, duration of a playlist, or number of media items in a playlist.</span></span>

``` syntax
<filter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</filter>
            
```

## <a name="attributes"></a><span data-ttu-id="07982-106">屬性</span><span class="sxs-lookup"><span data-stu-id="07982-106">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="07982-107"><span id="type"></span><span id="TYPE"></span>**類型**</span><span class="sxs-lookup"><span data-stu-id="07982-107"><span id="type"></span><span id="TYPE"></span>**type**</span></span>
</dt> <dd>

<span data-ttu-id="07982-108">篩選物件的型別。</span><span class="sxs-lookup"><span data-stu-id="07982-108">The type of filter object.</span></span> <span data-ttu-id="07982-109">這個屬性沒有預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="07982-109">There are no predefined values for this attribute.</span></span>

</dd> <dt>

<span data-ttu-id="07982-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>需要 (**識別碼**) </span><span class="sxs-lookup"><span data-stu-id="07982-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="07982-111">可唯一識別篩選物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="07982-111">The GUID that uniquely identifies a filter object.</span></span> <span data-ttu-id="07982-112">系統會叫用篩選物件的方法，以解讀 **篩選** 元素中包含的 **片段** 專案。</span><span class="sxs-lookup"><span data-stu-id="07982-112">The filter object's methods are invoked to interpret the **fragment** elements contained in the **filter** element.</span></span>



| <span data-ttu-id="07982-113">值</span><span class="sxs-lookup"><span data-stu-id="07982-113">Value</span></span>                                  | <span data-ttu-id="07982-114">描述</span><span class="sxs-lookup"><span data-stu-id="07982-114">Description</span></span>                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07982-115">{BC5E21B0-504C-46F6-82BF-FB975C911AD6}</span><span class="sxs-lookup"><span data-stu-id="07982-115">{BC5E21B0-504C-46F6-82BF-FB975C911AD6}</span></span> | <span data-ttu-id="07982-116">「Microsoft 自動播放清單篩選--依計數、大小或持續時間限制自動播放清單」篩選器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="07982-116">The id for the "Microsoft Auto Playlist Filter -- Limits auto playlists by count, size or duration" filter.</span></span> |



 

</dd> <dt>

<span data-ttu-id="07982-117"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>需要 (**名稱**) </span><span class="sxs-lookup"><span data-stu-id="07982-117"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="07982-118">篩選物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="07982-118">The name of the filter object.</span></span>



| <span data-ttu-id="07982-119">值</span><span class="sxs-lookup"><span data-stu-id="07982-119">Value</span></span>                                                                              | <span data-ttu-id="07982-120">描述</span><span class="sxs-lookup"><span data-stu-id="07982-120">Description</span></span>                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="07982-121">Microsoft 自動播放清單篩選--依計數、大小或持續時間限制自動播放清單</span><span class="sxs-lookup"><span data-stu-id="07982-121">Microsoft Auto Playlist Filter -- Limits auto playlists by count, size or duration</span></span> | <span data-ttu-id="07982-122">依計數、大小或持續時間限制自動播放清單。</span><span class="sxs-lookup"><span data-stu-id="07982-122">Limits auto playlists by count, size, or duration.</span></span> |



 

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="07982-123">父/子項目</span><span class="sxs-lookup"><span data-stu-id="07982-123">Parent/Child Elements</span></span>



| <span data-ttu-id="07982-124">階層</span><span class="sxs-lookup"><span data-stu-id="07982-124">Hierarchy</span></span> | <span data-ttu-id="07982-125">元素</span><span class="sxs-lookup"><span data-stu-id="07982-125">Elements</span></span>                                   |
|-----------|--------------------------------------------|
| <span data-ttu-id="07982-126">父代</span><span class="sxs-lookup"><span data-stu-id="07982-126">Parent</span></span>    | [<span data-ttu-id="07982-127">smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="07982-127">smartPlaylist</span></span>](smartplaylist-element.md) |
| <span data-ttu-id="07982-128">子系</span><span class="sxs-lookup"><span data-stu-id="07982-128">Child</span></span>     | [<span data-ttu-id="07982-129">片段</span><span class="sxs-lookup"><span data-stu-id="07982-129">fragment</span></span>](fragment-element.md)           |



 

## <a name="remarks"></a><span data-ttu-id="07982-130">備註</span><span class="sxs-lookup"><span data-stu-id="07982-130">Remarks</span></span>

<span data-ttu-id="07982-131">**篩選** 元素不會將任何媒體元件新增至播放清單;它只會移除或篩選 **sourceFilter** 元素所選取的內容。</span><span class="sxs-lookup"><span data-stu-id="07982-131">The **filter** element does not add any media elements to a playlist; it simply removes or filters out content that was selected by the **sourceFilter** element.</span></span>

## <a name="examples"></a><span data-ttu-id="07982-132">範例</span><span class="sxs-lookup"><span data-stu-id="07982-132">Examples</span></span>


```XML
<filter 
    type = "smartFilterObject" 
    id = "{BC5E21B0-504C-46F6-82BF-FB975C911AD6}" 
    name = "Microsoft Auto Playlist Filter -- Limits auto playlists by count,size or duration">
        <fragment name = "Limit Number of Items">
            <argument name = "number">25</argument>
        </fragment>
</filter>
```



## <a name="requirements"></a><span data-ttu-id="07982-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="07982-133">Requirements</span></span>



| <span data-ttu-id="07982-134">需求</span><span class="sxs-lookup"><span data-stu-id="07982-134">Requirement</span></span> | <span data-ttu-id="07982-135">值</span><span class="sxs-lookup"><span data-stu-id="07982-135">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="07982-136">版本</span><span class="sxs-lookup"><span data-stu-id="07982-136">Version</span></span><br/> | <span data-ttu-id="07982-137">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="07982-137">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07982-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07982-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07982-139">**引數元素**</span><span class="sxs-lookup"><span data-stu-id="07982-139">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="07982-140">**片段元素**</span><span class="sxs-lookup"><span data-stu-id="07982-140">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="07982-141">**smartPlaylist 元素**</span><span class="sxs-lookup"><span data-stu-id="07982-141">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="07982-142">**sourceFilter 元素**</span><span class="sxs-lookup"><span data-stu-id="07982-142">**sourceFilter Element**</span></span>](sourcefilter-element.md)
</dt> <dt>

[<span data-ttu-id="07982-143">**Windows Media 播放清單元素參考**</span><span class="sxs-lookup"><span data-stu-id="07982-143">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





