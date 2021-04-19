---
description: 複合元素定義了組合、追蹤的容器物件，以及其他的嵌套組合。
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: 複合元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c81bf445769c049287bdfa7d23f4ab82bb0f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106976995"
---
# <a name="composite-element"></a><span data-ttu-id="7d3df-103">複合元素</span><span class="sxs-lookup"><span data-stu-id="7d3df-103">composite Element</span></span>

> [!Note]  
> <span data-ttu-id="7d3df-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="7d3df-104">\[Deprecated.</span></span> <span data-ttu-id="7d3df-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="7d3df-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7d3df-106">`composite`元素會定義組合、追蹤的容器物件，以及其他的嵌套組合。</span><span class="sxs-lookup"><span data-stu-id="7d3df-106">The `composite` element defines a composition, a container object for tracks and other nested compositions.</span></span>

## <a name="attributes"></a><span data-ttu-id="7d3df-107">屬性</span><span class="sxs-lookup"><span data-stu-id="7d3df-107">Attributes</span></span>

<span data-ttu-id="7d3df-108">[**鎖定**](lock-attribute.md)、 [**靜音**](mute-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid**](userid-attribute.md)、 [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="7d3df-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="7d3df-109">父系/子系資訊</span><span class="sxs-lookup"><span data-stu-id="7d3df-109">Parent/Child Information</span></span>



|          |                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d3df-110">父代</span><span class="sxs-lookup"><span data-stu-id="7d3df-110">Parent</span></span>   | <span data-ttu-id="7d3df-111">`composite`、 [**群組**](group-element.md)</span><span class="sxs-lookup"><span data-stu-id="7d3df-111">`composite`, [**group**](group-element.md)</span></span>                                                                             |
| <span data-ttu-id="7d3df-112">Children</span><span class="sxs-lookup"><span data-stu-id="7d3df-112">Children</span></span> | <span data-ttu-id="7d3df-113">`composite`、 [**效果**](effect-element.md)、 [**追蹤**](track-element.md)、 [**轉換**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="7d3df-113">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7d3df-114">備註</span><span class="sxs-lookup"><span data-stu-id="7d3df-114">Remarks</span></span>

<span data-ttu-id="7d3df-115">在專案中 `composite` ，嵌套層的優先順序是由它們出現在元素內的順序隱含決定。</span><span class="sxs-lookup"><span data-stu-id="7d3df-115">Within a `composite` element, the priority of nested layers is determined implicitly by the order in which they appear within the element.</span></span> <span data-ttu-id="7d3df-116">第一個圖層的優先順序為0，而後續層級的優先順序值也會增加。</span><span class="sxs-lookup"><span data-stu-id="7d3df-116">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="7d3df-117">範例</span><span class="sxs-lookup"><span data-stu-id="7d3df-117">Examples</span></span>


```XML
<composite> </composite>
```



## <a name="see-also"></a><span data-ttu-id="7d3df-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d3df-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d3df-119">XTL 元素</span><span class="sxs-lookup"><span data-stu-id="7d3df-119">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



