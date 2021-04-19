---
title: UserEffectiveRating 屬性
description: UserEffectiveRating 屬性是根據播放專案的頻率 Windows Media Player 計算的評等。
ms.assetid: 6a420e20-f61d-4e15-84f8-a738caabd1d7
keywords:
- UserEffectiveRating 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- UserEffectiveRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94abda9f8237c169845683263081566957a10b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989525"
---
# <a name="usereffectiverating-attribute"></a><span data-ttu-id="a1148-104">UserEffectiveRating 屬性</span><span class="sxs-lookup"><span data-stu-id="a1148-104">UserEffectiveRating Attribute</span></span>

<span data-ttu-id="a1148-105">**UserEffectiveRating** 屬性是根據播放專案的頻率 Windows Media Player 計算的評等。</span><span class="sxs-lookup"><span data-stu-id="a1148-105">The **UserEffectiveRating** attribute is the rating computed by Windows Media Player based on how often the item has been played.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a1148-106">套用至</span><span class="sxs-lookup"><span data-stu-id="a1148-106">Applies To</span></span>

-   [<span data-ttu-id="a1148-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="a1148-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="a1148-108">其他專案</span><span class="sxs-lookup"><span data-stu-id="a1148-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="a1148-109">播放清單</span><span class="sxs-lookup"><span data-stu-id="a1148-109">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="a1148-110">影片專案</span><span class="sxs-lookup"><span data-stu-id="a1148-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="a1148-111">備註</span><span class="sxs-lookup"><span data-stu-id="a1148-111">Remarks</span></span>

<span data-ttu-id="a1148-112">使用者評等是以整數值表示，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="a1148-112">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="a1148-113">指定值時，請使用 [寫入值] 資料行中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a1148-113">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="a1148-114">在抓取值時，您可以使用 [讀取值] 資料行中的範圍來決定星星數目。</span><span class="sxs-lookup"><span data-stu-id="a1148-114">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="a1148-115">分級</span><span class="sxs-lookup"><span data-stu-id="a1148-115">Rating</span></span>  | <span data-ttu-id="a1148-116">寫入值</span><span class="sxs-lookup"><span data-stu-id="a1148-116">Writing value</span></span> | <span data-ttu-id="a1148-117">讀取值</span><span class="sxs-lookup"><span data-stu-id="a1148-117">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="a1148-118">評分</span><span class="sxs-lookup"><span data-stu-id="a1148-118">Unrated</span></span> | <span data-ttu-id="a1148-119">0</span><span class="sxs-lookup"><span data-stu-id="a1148-119">0</span></span>             | <span data-ttu-id="a1148-120">0</span><span class="sxs-lookup"><span data-stu-id="a1148-120">0</span></span>              |
| <span data-ttu-id="a1148-121">1 顆星</span><span class="sxs-lookup"><span data-stu-id="a1148-121">1 star</span></span>  | <span data-ttu-id="a1148-122">1</span><span class="sxs-lookup"><span data-stu-id="a1148-122">1</span></span>             | <span data-ttu-id="a1148-123">1 到 12</span><span class="sxs-lookup"><span data-stu-id="a1148-123">1 to 12</span></span>        |
| <span data-ttu-id="a1148-124">2 顆星</span><span class="sxs-lookup"><span data-stu-id="a1148-124">2 stars</span></span> | <span data-ttu-id="a1148-125">25</span><span class="sxs-lookup"><span data-stu-id="a1148-125">25</span></span>            | <span data-ttu-id="a1148-126">13到37</span><span class="sxs-lookup"><span data-stu-id="a1148-126">13 to 37</span></span>       |
| <span data-ttu-id="a1148-127">3 顆星</span><span class="sxs-lookup"><span data-stu-id="a1148-127">3 stars</span></span> | <span data-ttu-id="a1148-128">50</span><span class="sxs-lookup"><span data-stu-id="a1148-128">50</span></span>            | <span data-ttu-id="a1148-129">38至62</span><span class="sxs-lookup"><span data-stu-id="a1148-129">38 to 62</span></span>       |
| <span data-ttu-id="a1148-130">4 顆星</span><span class="sxs-lookup"><span data-stu-id="a1148-130">4 stars</span></span> | <span data-ttu-id="a1148-131">75</span><span class="sxs-lookup"><span data-stu-id="a1148-131">75</span></span>            | <span data-ttu-id="a1148-132">63至86</span><span class="sxs-lookup"><span data-stu-id="a1148-132">63 to 86</span></span>       |
| <span data-ttu-id="a1148-133">5 顆星</span><span class="sxs-lookup"><span data-stu-id="a1148-133">5 stars</span></span> | <span data-ttu-id="a1148-134">99</span><span class="sxs-lookup"><span data-stu-id="a1148-134">99</span></span>            | <span data-ttu-id="a1148-135">87至99</span><span class="sxs-lookup"><span data-stu-id="a1148-135">87 to 99</span></span>       |



 

<span data-ttu-id="a1148-136">這個屬性只會儲存在程式庫中。</span><span class="sxs-lookup"><span data-stu-id="a1148-136">This attribute is stored only in the library.</span></span>

<span data-ttu-id="a1148-137">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a1148-137">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1148-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1148-138">Requirements</span></span>



| <span data-ttu-id="a1148-139">需求</span><span class="sxs-lookup"><span data-stu-id="a1148-139">Requirement</span></span> | <span data-ttu-id="a1148-140">值</span><span class="sxs-lookup"><span data-stu-id="a1148-140">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="a1148-141">版本</span><span class="sxs-lookup"><span data-stu-id="a1148-141">Version</span></span><br/> | <span data-ttu-id="a1148-142">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="a1148-142">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1148-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1148-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1148-144">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="a1148-144">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





