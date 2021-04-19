---
title: 滑杆。值
description: Value 屬性會指定或抓取滑杆的目前位置。 |滑杆。值
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- 滑杆。值 Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87aeff5c97808efb812f530236227b07f463855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984052"
---
# <a name="slidervalue"></a><span data-ttu-id="2802d-105">滑杆。值</span><span class="sxs-lookup"><span data-stu-id="2802d-105">SLIDER.value</span></span>

<span data-ttu-id="2802d-106">**Value** 屬性會指定或抓取滑杆的目前位置。</span><span class="sxs-lookup"><span data-stu-id="2802d-106">The **value** attribute specifies or retrieves the current position of the slider.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="2802d-107">可能的值</span><span class="sxs-lookup"><span data-stu-id="2802d-107">Possible Values</span></span>

<span data-ttu-id="2802d-108">這個屬性是 (**float**) 的讀/寫 **數位**，預設值為 **min**。</span><span class="sxs-lookup"><span data-stu-id="2802d-108">This attribute is a read/write **Number** (**float**) with a default value of **min**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2802d-109">備註</span><span class="sxs-lookup"><span data-stu-id="2802d-109">Remarks</span></span>

<span data-ttu-id="2802d-110">此 **值** 應該一律大於或等於 **最小** 值，且小於或等於 **max**。如果您指定超出此範圍的值，則 [ **值** ] 和滑杆的位置都不會變更。</span><span class="sxs-lookup"><span data-stu-id="2802d-110">The **value** should always be greater than or equal to **min** and less than or equal to **max**. If you specify a value outside this range, **value** and the position of the slider are not changed.</span></span>

<span data-ttu-id="2802d-111">請參閱 **CUSTOMSLIDER**。說明如何使用 **滑杆** 元素屬性之範例的 [positionImage](customslider-positionimage.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="2802d-111">See the **CUSTOMSLIDER**.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2802d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2802d-112">Requirements</span></span>



| <span data-ttu-id="2802d-113">需求</span><span class="sxs-lookup"><span data-stu-id="2802d-113">Requirement</span></span> | <span data-ttu-id="2802d-114">值</span><span class="sxs-lookup"><span data-stu-id="2802d-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2802d-115">版本</span><span class="sxs-lookup"><span data-stu-id="2802d-115">Version</span></span><br/> | <span data-ttu-id="2802d-116">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="2802d-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2802d-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2802d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2802d-118">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="2802d-118">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="2802d-119">**滑杆。最小值**</span><span class="sxs-lookup"><span data-stu-id="2802d-119">**SLIDER.min**</span></span>](slider-min.md)
</dt> </dl>

 

 





