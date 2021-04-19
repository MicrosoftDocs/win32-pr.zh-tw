---
title: UserRating 屬性
description: UserRating 屬性是使用者在程式庫中所指定的分級。
ms.assetid: 33df5316-1506-4ecb-b729-c2d66b878825
keywords:
- UserRating 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- UserRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a25dd7b4e55195deaecf5228b9ad5bad9195c2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975725"
---
# <a name="userrating-attribute"></a><span data-ttu-id="74db2-104">UserRating 屬性</span><span class="sxs-lookup"><span data-stu-id="74db2-104">UserRating Attribute</span></span>

<span data-ttu-id="74db2-105">**UserRating** 屬性是使用者在程式庫中所指定的分級。</span><span class="sxs-lookup"><span data-stu-id="74db2-105">The **UserRating** attribute is the rating specified by the user in the library.</span></span>

## <a name="applies-to"></a><span data-ttu-id="74db2-106">套用至</span><span class="sxs-lookup"><span data-stu-id="74db2-106">Applies To</span></span>

-   [<span data-ttu-id="74db2-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="74db2-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="74db2-108">其他專案</span><span class="sxs-lookup"><span data-stu-id="74db2-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="74db2-109">相片專案</span><span class="sxs-lookup"><span data-stu-id="74db2-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="74db2-110">播放清單</span><span class="sxs-lookup"><span data-stu-id="74db2-110">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="74db2-111">影片專案</span><span class="sxs-lookup"><span data-stu-id="74db2-111">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="74db2-112">備註</span><span class="sxs-lookup"><span data-stu-id="74db2-112">Remarks</span></span>

<span data-ttu-id="74db2-113">使用者評等是以整數值表示，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="74db2-113">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="74db2-114">指定值時，請使用 [寫入值] 資料行中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="74db2-114">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="74db2-115">在抓取值時，您可以使用 [讀取值] 資料行中的範圍來決定星星數目。</span><span class="sxs-lookup"><span data-stu-id="74db2-115">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="74db2-116">分級</span><span class="sxs-lookup"><span data-stu-id="74db2-116">Rating</span></span>  | <span data-ttu-id="74db2-117">寫入值</span><span class="sxs-lookup"><span data-stu-id="74db2-117">Writing value</span></span> | <span data-ttu-id="74db2-118">讀取值</span><span class="sxs-lookup"><span data-stu-id="74db2-118">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="74db2-119">評分</span><span class="sxs-lookup"><span data-stu-id="74db2-119">Unrated</span></span> | <span data-ttu-id="74db2-120">0</span><span class="sxs-lookup"><span data-stu-id="74db2-120">0</span></span>             | <span data-ttu-id="74db2-121">0</span><span class="sxs-lookup"><span data-stu-id="74db2-121">0</span></span>              |
| <span data-ttu-id="74db2-122">1 顆星</span><span class="sxs-lookup"><span data-stu-id="74db2-122">1 star</span></span>  | <span data-ttu-id="74db2-123">1</span><span class="sxs-lookup"><span data-stu-id="74db2-123">1</span></span>             | <span data-ttu-id="74db2-124">1 到 12</span><span class="sxs-lookup"><span data-stu-id="74db2-124">1 to 12</span></span>        |
| <span data-ttu-id="74db2-125">2 顆星</span><span class="sxs-lookup"><span data-stu-id="74db2-125">2 stars</span></span> | <span data-ttu-id="74db2-126">25</span><span class="sxs-lookup"><span data-stu-id="74db2-126">25</span></span>            | <span data-ttu-id="74db2-127">13到37</span><span class="sxs-lookup"><span data-stu-id="74db2-127">13 to 37</span></span>       |
| <span data-ttu-id="74db2-128">3 顆星</span><span class="sxs-lookup"><span data-stu-id="74db2-128">3 stars</span></span> | <span data-ttu-id="74db2-129">50</span><span class="sxs-lookup"><span data-stu-id="74db2-129">50</span></span>            | <span data-ttu-id="74db2-130">38至62</span><span class="sxs-lookup"><span data-stu-id="74db2-130">38 to 62</span></span>       |
| <span data-ttu-id="74db2-131">4 顆星</span><span class="sxs-lookup"><span data-stu-id="74db2-131">4 stars</span></span> | <span data-ttu-id="74db2-132">75</span><span class="sxs-lookup"><span data-stu-id="74db2-132">75</span></span>            | <span data-ttu-id="74db2-133">63至86</span><span class="sxs-lookup"><span data-stu-id="74db2-133">63 to 86</span></span>       |
| <span data-ttu-id="74db2-134">5 顆星</span><span class="sxs-lookup"><span data-stu-id="74db2-134">5 stars</span></span> | <span data-ttu-id="74db2-135">99</span><span class="sxs-lookup"><span data-stu-id="74db2-135">99</span></span>            | <span data-ttu-id="74db2-136">87至99</span><span class="sxs-lookup"><span data-stu-id="74db2-136">87 to 99</span></span>       |



 

<span data-ttu-id="74db2-137">這個屬性只會儲存在程式庫中。</span><span class="sxs-lookup"><span data-stu-id="74db2-137">This attribute is stored only in the library.</span></span>

<span data-ttu-id="74db2-138">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="74db2-138">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="74db2-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="74db2-139">Requirements</span></span>



| <span data-ttu-id="74db2-140">需求</span><span class="sxs-lookup"><span data-stu-id="74db2-140">Requirement</span></span> | <span data-ttu-id="74db2-141">值</span><span class="sxs-lookup"><span data-stu-id="74db2-141">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74db2-142">版本</span><span class="sxs-lookup"><span data-stu-id="74db2-142">Version</span></span><br/> | <span data-ttu-id="74db2-143">Windows Media Player 9 系列或更新版本 (只有 Windows Media Player 10 或更新版本才支援相片專案) </span><span class="sxs-lookup"><span data-stu-id="74db2-143">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74db2-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74db2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74db2-145">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="74db2-145">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





