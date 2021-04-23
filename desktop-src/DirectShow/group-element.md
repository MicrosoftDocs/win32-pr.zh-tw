---
description: Group 元素會定義一個群組，也就是時間軸中的最上層物件。
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: " (DirectShow) 的群組元素"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31502cef89c8383e935f409d76b9e31ca53a2da1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909246"
---
# <a name="group-element"></a><span data-ttu-id="090ef-103">group 元素</span><span class="sxs-lookup"><span data-stu-id="090ef-103">group Element</span></span>

> [!Note]  
> <span data-ttu-id="090ef-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="090ef-104">\[Deprecated.</span></span> <span data-ttu-id="090ef-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="090ef-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="090ef-106">**Group** 元素會定義一個群組，也就是時間軸中的最上層物件。</span><span class="sxs-lookup"><span data-stu-id="090ef-106">The **group** element defines a group, the top-level object in a timeline.</span></span>

## <a name="attributes"></a><span data-ttu-id="090ef-107">屬性</span><span class="sxs-lookup"><span data-stu-id="090ef-107">Attributes</span></span>

<span data-ttu-id="090ef-108">[**bitdepth**](bitdepth-attribute.md)、 [**緩衝**](buffering-attribute.md)、 [**畫面播放速率**](framerate-attribute.md)、 [**高度**](height-attribute.md)、 [**鎖定**](lock-attribute.md)、 [**靜音**](mute-attribute.md)、 [**name**](name-attribute.md)、 [**previewmode**](previewmode-attribute.md)、 [**samplingrate**](samplingrate-attribute.md)、 [**type**](type-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid**](userid-attribute.md)、 [**username**](username-attribute.md)、 [**width**](width-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="090ef-108">[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="090ef-109">父系/子系資訊</span><span class="sxs-lookup"><span data-stu-id="090ef-109">Parent/Child Information</span></span>



| <span data-ttu-id="090ef-110">標籤</span><span class="sxs-lookup"><span data-stu-id="090ef-110">Label</span></span> | <span data-ttu-id="090ef-111">值</span><span class="sxs-lookup"><span data-stu-id="090ef-111">Value</span></span> |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="090ef-112">父代</span><span class="sxs-lookup"><span data-stu-id="090ef-112">Parent</span></span>   | [<span data-ttu-id="090ef-113">**時程表**</span><span class="sxs-lookup"><span data-stu-id="090ef-113">**timeline**</span></span>](timeline-element.md)                                                                     |
| <span data-ttu-id="090ef-114">Children</span><span class="sxs-lookup"><span data-stu-id="090ef-114">Children</span></span> | <span data-ttu-id="090ef-115">[**複合**](composite-element.md)、 [**效果**](effect-element.md)、 [**追蹤**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="090ef-115">[**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="090ef-116">備註</span><span class="sxs-lookup"><span data-stu-id="090ef-116">Remarks</span></span>

<span data-ttu-id="090ef-117">在專案中 `group` ，嵌套層的優先順序是由它們出現在元素內的順序隱含決定。</span><span class="sxs-lookup"><span data-stu-id="090ef-117">Within a `group` element, the priority of nested layers is determined implicitly by the order they appear within the element.</span></span> <span data-ttu-id="090ef-118">第一個圖層的優先順序為0，而後續層級的優先順序值也會增加。</span><span class="sxs-lookup"><span data-stu-id="090ef-118">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="090ef-119">範例</span><span class="sxs-lookup"><span data-stu-id="090ef-119">Examples</span></span>


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a><span data-ttu-id="090ef-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="090ef-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="090ef-121">XTL 元素</span><span class="sxs-lookup"><span data-stu-id="090ef-121">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



