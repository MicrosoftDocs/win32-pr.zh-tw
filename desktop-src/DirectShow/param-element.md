---
description: Param 元素會指定轉換、效果或其他子物件上的屬性值。
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: " (DirectShow) 的 param 元素"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb1d007a7f3e2dcffaa7b9163c76be604fed7a9a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846559"
---
# <a name="param-element"></a><span data-ttu-id="8924a-103">param 元素</span><span class="sxs-lookup"><span data-stu-id="8924a-103">param Element</span></span>

> [!Note]  
> <span data-ttu-id="8924a-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="8924a-104">\[Deprecated.</span></span> <span data-ttu-id="8924a-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="8924a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8924a-106">`param`元素會指定轉換、效果或其他子物件上的屬性值。</span><span class="sxs-lookup"><span data-stu-id="8924a-106">The `param` element specifies the value of a property on a transition, effect, or other subobject.</span></span>

## <a name="attributes"></a><span data-ttu-id="8924a-107">屬性</span><span class="sxs-lookup"><span data-stu-id="8924a-107">Attributes</span></span>

<span data-ttu-id="8924a-108">[**名稱**](name-attribute.md)、 [**值**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="8924a-108">[**name**](name-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="8924a-109">父系/子系資訊</span><span class="sxs-lookup"><span data-stu-id="8924a-109">Parent/Child Information</span></span>



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8924a-110">父代</span><span class="sxs-lookup"><span data-stu-id="8924a-110">Parent</span></span>   | <span data-ttu-id="8924a-111">[**剪輯**](clip-element.md)、 [**效果**](effect-element.md)、 [**轉換**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="8924a-111">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span> |
| <span data-ttu-id="8924a-112">Children</span><span class="sxs-lookup"><span data-stu-id="8924a-112">Children</span></span> | <span data-ttu-id="8924a-113">[**at**](at-element.md)、 [**線性**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="8924a-113">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>                                               |



 

## <a name="remarks"></a><span data-ttu-id="8924a-114">備註</span><span class="sxs-lookup"><span data-stu-id="8924a-114">Remarks</span></span>

<span data-ttu-id="8924a-115">**Value** 屬性會在轉換或效果開始時，指定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="8924a-115">The **value** attribute specifies the value of the property at the start of the transition or effect.</span></span> <span data-ttu-id="8924a-116">使用 **at** 或 **線性** 元素來指定變更值。</span><span class="sxs-lookup"><span data-stu-id="8924a-116">Use the **at** or **linear** element to specify changing values.</span></span> <span data-ttu-id="8924a-117">如果 **param** 元素包含 no 或 **線性** 元素，此值會在 **效果或轉換** 的持續時間內保持不變。</span><span class="sxs-lookup"><span data-stu-id="8924a-117">If the **param** element contains no **at** or **linear** elements, the value remains constant over the duration of the effect or transition.</span></span>

> [!Note]  
> <span data-ttu-id="8924a-118">**剪切** 元素內的 **param** 專案不 **能包含或\*\*\*\*線性** 元素。</span><span class="sxs-lookup"><span data-stu-id="8924a-118">A **param** element inside a **clip** element cannot contain **at** or **linear** elements.</span></span>

 

<span data-ttu-id="8924a-119">許多轉換支援標準 **進度** 屬性，範圍從0到1.0，指出輸出中反映的轉換百分比。</span><span class="sxs-lookup"><span data-stu-id="8924a-119">Many transitions support a standard **Progress** property that ranges from 0 to 1.0, indicating what percentage of the transition is reflected in the output.</span></span> <span data-ttu-id="8924a-120">**進度**= 0.0，轉換會在其序列的開頭 (完全是) 的第一個影片影像。</span><span class="sxs-lookup"><span data-stu-id="8924a-120">At **Progress** = 0.0, the transition is at the beginning of its sequence (entirely the first video image).</span></span> <span data-ttu-id="8924a-121">**進行** 中 = 0.5 時，轉換是一半的完成。</span><span class="sxs-lookup"><span data-stu-id="8924a-121">At **Progress** = 0.5, the transition is half complete.</span></span> <span data-ttu-id="8924a-122"> (例如，在抹除 **過程** = 0.5，轉換界限位於影像的中央，) **正在進行** 中 = 1.0，則轉換已完成 (完全) 第二個影像。</span><span class="sxs-lookup"><span data-stu-id="8924a-122">(For example, in a wipe, at **Progress** = 0.5 the transition boundary is in the center of the image) At **Progress** = 1.0, the transition is complete (entirely the second image).</span></span> <span data-ttu-id="8924a-123">根據預設，轉換會在轉換開始進行時，從 **進度** = 0.0 移至 **進度** = 1.0 結尾。</span><span class="sxs-lookup"><span data-stu-id="8924a-123">By default, transitions go from **Progress** = 0.0 at the start of the transition to **Progress** = 1.0 at the end.</span></span>

<span data-ttu-id="8924a-124">其他屬性通常專屬於特定的轉換或效果。</span><span class="sxs-lookup"><span data-stu-id="8924a-124">Other properties are usually specific to one particular transition or effect.</span></span> <span data-ttu-id="8924a-125">例如，抹除轉換支援可控制轉換區域寬度的 **GradientSize** 屬性。</span><span class="sxs-lookup"><span data-stu-id="8924a-125">For example, the wipe transition supports a **GradientSize** property that controls the width of the transition area.</span></span>

<span data-ttu-id="8924a-126">若要回溯執行轉換，請在轉換開始時將 **進度** 屬性設為1.0，並使用 **線性** 元素將值變更為0.0，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="8924a-126">To run a transition backward, set the **Progress** property to 1.0 at the start of the transition, and use the **linear** element to change the value to 0.0, as shown in the following example:</span></span>


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a><span data-ttu-id="8924a-127">範例</span><span class="sxs-lookup"><span data-stu-id="8924a-127">Examples</span></span>


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a><span data-ttu-id="8924a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8924a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8924a-129">XTL 元素</span><span class="sxs-lookup"><span data-stu-id="8924a-129">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



