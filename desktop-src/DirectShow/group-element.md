---
description: Group 元素會定義一個群組，也就是時間軸中的最上層物件。
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: " (DirectShow) 的群組元素"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b8146586d93a53093a68bb1abc08e85c52f14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935976"
---
# <a name="group-element"></a><span data-ttu-id="a54e3-103">group 元素</span><span class="sxs-lookup"><span data-stu-id="a54e3-103">group Element</span></span>

> [!Note]  
> <span data-ttu-id="a54e3-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="a54e3-104">\[Deprecated.</span></span> <span data-ttu-id="a54e3-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="a54e3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a54e3-106">**Group** 元素會定義一個群組，也就是時間軸中的最上層物件。</span><span class="sxs-lookup"><span data-stu-id="a54e3-106">The **group** element defines a group, the top-level object in a timeline.</span></span>

## <a name="attributes"></a><span data-ttu-id="a54e3-107">屬性</span><span class="sxs-lookup"><span data-stu-id="a54e3-107">Attributes</span></span>

<span data-ttu-id="a54e3-108">[**bitdepth**](bitdepth-attribute.md)、 [**緩衝**](buffering-attribute.md)、 [**畫面播放速率**](framerate-attribute.md)、 [**高度**](height-attribute.md)、 [**鎖定**](lock-attribute.md)、 [**靜音**](mute-attribute.md)、 [**name**](name-attribute.md)、 [**previewmode**](previewmode-attribute.md)、 [**samplingrate**](samplingrate-attribute.md)、 [**type**](type-attribute.md)、 [**userdata**](userdata-attribute.md)、 [**userid**](userid-attribute.md)、 [**username**](username-attribute.md)、 [**width**](width-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="a54e3-108">[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="a54e3-109">父系/子系資訊</span><span class="sxs-lookup"><span data-stu-id="a54e3-109">Parent/Child Information</span></span>



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a54e3-110">父代</span><span class="sxs-lookup"><span data-stu-id="a54e3-110">Parent</span></span>   | [<span data-ttu-id="a54e3-111">**時程表**</span><span class="sxs-lookup"><span data-stu-id="a54e3-111">**timeline**</span></span>](timeline-element.md)                                                                     |
| <span data-ttu-id="a54e3-112">Children</span><span class="sxs-lookup"><span data-stu-id="a54e3-112">Children</span></span> | <span data-ttu-id="a54e3-113">[**複合**](composite-element.md)、 [**效果**](effect-element.md)、 [**追蹤**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="a54e3-113">[**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a54e3-114">備註</span><span class="sxs-lookup"><span data-stu-id="a54e3-114">Remarks</span></span>

<span data-ttu-id="a54e3-115">在專案中 `group` ，嵌套層的優先順序是由它們出現在元素內的順序隱含決定。</span><span class="sxs-lookup"><span data-stu-id="a54e3-115">Within a `group` element, the priority of nested layers is determined implicitly by the order they appear within the element.</span></span> <span data-ttu-id="a54e3-116">第一個圖層的優先順序為0，而後續層級的優先順序值也會增加。</span><span class="sxs-lookup"><span data-stu-id="a54e3-116">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="a54e3-117">範例</span><span class="sxs-lookup"><span data-stu-id="a54e3-117">Examples</span></span>


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a><span data-ttu-id="a54e3-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a54e3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a54e3-119">XTL 元素</span><span class="sxs-lookup"><span data-stu-id="a54e3-119">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



