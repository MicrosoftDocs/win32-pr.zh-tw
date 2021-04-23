---
description: 複合元素定義了組合、追蹤的容器物件，以及其他的嵌套組合。
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: 複合元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5eff3e0c16040f837e4c8a792ebac3124d723d1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908836"
---
# <a name="composite-element"></a><span data-ttu-id="fb4da-103">複合元素</span><span class="sxs-lookup"><span data-stu-id="fb4da-103">composite Element</span></span>

> [!Note]  
> <span data-ttu-id="fb4da-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="fb4da-104">\[Deprecated.</span></span> <span data-ttu-id="fb4da-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="fb4da-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fb4da-106">`composite`元素會定義組合、追蹤的容器物件，以及其他的嵌套組合。</span><span class="sxs-lookup"><span data-stu-id="fb4da-106">The `composite` element defines a composition, a container object for tracks and other nested compositions.</span></span>

## <a name="attributes"></a><span data-ttu-id="fb4da-107">屬性</span><span class="sxs-lookup"><span data-stu-id="fb4da-107">Attributes</span></span>

<span data-ttu-id="fb4da-108">[**鎖定**](lock-attribute.md)、 [**靜音**](mute-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid**](userid-attribute.md)、 [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="fb4da-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="fb4da-109">父系/子系資訊</span><span class="sxs-lookup"><span data-stu-id="fb4da-109">Parent/Child Information</span></span>



| <span data-ttu-id="fb4da-110">標籤</span><span class="sxs-lookup"><span data-stu-id="fb4da-110">Label</span></span> | <span data-ttu-id="fb4da-111">值</span><span class="sxs-lookup"><span data-stu-id="fb4da-111">Value</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4da-112">父代</span><span class="sxs-lookup"><span data-stu-id="fb4da-112">Parent</span></span>   | <span data-ttu-id="fb4da-113">`composite`、 [**群組**](group-element.md)</span><span class="sxs-lookup"><span data-stu-id="fb4da-113">`composite`, [**group**](group-element.md)</span></span>                                                                             |
| <span data-ttu-id="fb4da-114">Children</span><span class="sxs-lookup"><span data-stu-id="fb4da-114">Children</span></span> | <span data-ttu-id="fb4da-115">`composite`、 [**效果**](effect-element.md)、 [**追蹤**](track-element.md)、 [**轉換**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="fb4da-115">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fb4da-116">備註</span><span class="sxs-lookup"><span data-stu-id="fb4da-116">Remarks</span></span>

<span data-ttu-id="fb4da-117">在專案中 `composite` ，嵌套層的優先順序是由它們出現在元素內的順序隱含決定。</span><span class="sxs-lookup"><span data-stu-id="fb4da-117">Within a `composite` element, the priority of nested layers is determined implicitly by the order in which they appear within the element.</span></span> <span data-ttu-id="fb4da-118">第一個圖層的優先順序為0，而後續層級的優先順序值也會增加。</span><span class="sxs-lookup"><span data-stu-id="fb4da-118">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="fb4da-119">範例</span><span class="sxs-lookup"><span data-stu-id="fb4da-119">Examples</span></span>


```XML
<composite> </composite>
```



## <a name="see-also"></a><span data-ttu-id="fb4da-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb4da-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb4da-121">XTL 元素</span><span class="sxs-lookup"><span data-stu-id="fb4da-121">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



