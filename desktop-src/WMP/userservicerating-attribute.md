---
title: UserServiceRating 屬性
description: UserServiceRating 屬性已保留供日後使用。
ms.assetid: e6113474-725d-4eb1-9c05-cff7749f2010
keywords:
- UserServiceRating 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- UserServiceRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690a090aaa9d07ee850caee004242272368129f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992370"
---
# <a name="userservicerating-attribute"></a><span data-ttu-id="80148-104">UserServiceRating 屬性</span><span class="sxs-lookup"><span data-stu-id="80148-104">UserServiceRating Attribute</span></span>

<span data-ttu-id="80148-105">**UserServiceRating** 屬性已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="80148-105">The **UserServiceRating** attribute is reserved for future use.</span></span>

## <a name="applies-to"></a><span data-ttu-id="80148-106">套用至</span><span class="sxs-lookup"><span data-stu-id="80148-106">Applies To</span></span>

-   [<span data-ttu-id="80148-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="80148-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="80148-108">播放清單</span><span class="sxs-lookup"><span data-stu-id="80148-108">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="80148-109">影片專案</span><span class="sxs-lookup"><span data-stu-id="80148-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="80148-110">備註</span><span class="sxs-lookup"><span data-stu-id="80148-110">Remarks</span></span>

<span data-ttu-id="80148-111">使用者評等是以整數值表示，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="80148-111">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="80148-112">指定值時，請使用 [寫入值] 資料行中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="80148-112">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="80148-113">在抓取值時，您可以使用 [讀取值] 資料行中的範圍來決定星星數目。</span><span class="sxs-lookup"><span data-stu-id="80148-113">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="80148-114">分級</span><span class="sxs-lookup"><span data-stu-id="80148-114">Rating</span></span>  | <span data-ttu-id="80148-115">寫入值</span><span class="sxs-lookup"><span data-stu-id="80148-115">Writing value</span></span> | <span data-ttu-id="80148-116">讀取值</span><span class="sxs-lookup"><span data-stu-id="80148-116">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="80148-117">評分</span><span class="sxs-lookup"><span data-stu-id="80148-117">Unrated</span></span> | <span data-ttu-id="80148-118">0</span><span class="sxs-lookup"><span data-stu-id="80148-118">0</span></span>             | <span data-ttu-id="80148-119">0</span><span class="sxs-lookup"><span data-stu-id="80148-119">0</span></span>              |
| <span data-ttu-id="80148-120">1 顆星</span><span class="sxs-lookup"><span data-stu-id="80148-120">1 star</span></span>  | <span data-ttu-id="80148-121">1</span><span class="sxs-lookup"><span data-stu-id="80148-121">1</span></span>             | <span data-ttu-id="80148-122">1 到 12</span><span class="sxs-lookup"><span data-stu-id="80148-122">1 to 12</span></span>        |
| <span data-ttu-id="80148-123">2 顆星</span><span class="sxs-lookup"><span data-stu-id="80148-123">2 stars</span></span> | <span data-ttu-id="80148-124">25</span><span class="sxs-lookup"><span data-stu-id="80148-124">25</span></span>            | <span data-ttu-id="80148-125">13到37</span><span class="sxs-lookup"><span data-stu-id="80148-125">13 to 37</span></span>       |
| <span data-ttu-id="80148-126">3 顆星</span><span class="sxs-lookup"><span data-stu-id="80148-126">3 stars</span></span> | <span data-ttu-id="80148-127">50</span><span class="sxs-lookup"><span data-stu-id="80148-127">50</span></span>            | <span data-ttu-id="80148-128">38至62</span><span class="sxs-lookup"><span data-stu-id="80148-128">38 to 62</span></span>       |
| <span data-ttu-id="80148-129">4 顆星</span><span class="sxs-lookup"><span data-stu-id="80148-129">4 stars</span></span> | <span data-ttu-id="80148-130">75</span><span class="sxs-lookup"><span data-stu-id="80148-130">75</span></span>            | <span data-ttu-id="80148-131">63至86</span><span class="sxs-lookup"><span data-stu-id="80148-131">63 to 86</span></span>       |
| <span data-ttu-id="80148-132">5 顆星</span><span class="sxs-lookup"><span data-stu-id="80148-132">5 stars</span></span> | <span data-ttu-id="80148-133">99</span><span class="sxs-lookup"><span data-stu-id="80148-133">99</span></span>            | <span data-ttu-id="80148-134">87至99</span><span class="sxs-lookup"><span data-stu-id="80148-134">87 to 99</span></span>       |



 

<span data-ttu-id="80148-135">這個屬性只會儲存在程式庫中。</span><span class="sxs-lookup"><span data-stu-id="80148-135">This attribute is stored only in the library.</span></span>

<span data-ttu-id="80148-136">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="80148-136">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="80148-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="80148-137">Requirements</span></span>



| <span data-ttu-id="80148-138">需求</span><span class="sxs-lookup"><span data-stu-id="80148-138">Requirement</span></span> | <span data-ttu-id="80148-139">值</span><span class="sxs-lookup"><span data-stu-id="80148-139">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="80148-140">版本</span><span class="sxs-lookup"><span data-stu-id="80148-140">Version</span></span><br/> | <span data-ttu-id="80148-141">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="80148-141">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80148-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80148-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80148-143">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="80148-143">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





