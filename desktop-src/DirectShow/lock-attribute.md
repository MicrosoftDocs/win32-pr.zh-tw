---
description: Lock 屬性指定是否應編輯物件。 如果該值為 TRUE，則應用程式應該將物件視為鎖定，而且不允許對該物件或其子系進行變更。 預設值為 FALSE。
ms.assetid: 1aa92665-ab3b-4f04-9e6b-905942c197ef
title: lock 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7716f047e0df47ffb5e84cb2de0e9fe345836b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688275"
---
# <a name="lock-attribute"></a><span data-ttu-id="472df-105">lock 屬性</span><span class="sxs-lookup"><span data-stu-id="472df-105">lock Attribute</span></span>

> [!Note]  
> <span data-ttu-id="472df-106">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="472df-106">\[Deprecated.</span></span> <span data-ttu-id="472df-107">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="472df-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="472df-108">`lock`屬性指定是否應編輯物件。</span><span class="sxs-lookup"><span data-stu-id="472df-108">The `lock` attribute specifies whether an object should be edited.</span></span> <span data-ttu-id="472df-109">如果該值為 **TRUE**，則應用程式應該將物件視為鎖定，而且不允許對該物件或其子系進行變更。</span><span class="sxs-lookup"><span data-stu-id="472df-109">If the value is **TRUE**, the application should treat the object as locked, and disallow changes to that object or its children.</span></span> <span data-ttu-id="472df-110">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="472df-110">The default value is **FALSE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="472df-111">可能的值</span><span class="sxs-lookup"><span data-stu-id="472df-111">Possible Values</span></span>

<span data-ttu-id="472df-112">可能的值會將下列值定義為 TRUE： y、Y、t、T、1。</span><span class="sxs-lookup"><span data-stu-id="472df-112">Possible Values The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="472df-113">下列值定義為 FALSE： n、N、f、F、0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="472df-113">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="472df-114">套用至</span><span class="sxs-lookup"><span data-stu-id="472df-114">Applies To</span></span>

<span data-ttu-id="472df-115">[**剪輯**](clip-element.md)、 [**複合**](composite-element.md)、 [**效果**](effect-element.md)、 [**群組**](group-element.md)、 [**時間軸**](timeline-element.md)、 [**轉換**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="472df-115">[**clip**](clip-element.md), [**composite**](composite-element.md), [**effect**](effect-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="472df-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="472df-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="472df-117">XTL 屬性</span><span class="sxs-lookup"><span data-stu-id="472df-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="472df-118">**IAMTimelineObj::SetLocked**</span><span class="sxs-lookup"><span data-stu-id="472df-118">**IAMTimelineObj::SetLocked**</span></span>](iamtimelineobj-setlocked.md)
</dt> </dl>

 

 



