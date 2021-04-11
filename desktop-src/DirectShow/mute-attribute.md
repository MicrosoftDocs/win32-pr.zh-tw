---
description: 靜音屬性指定物件的靜音狀態。
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: 靜音屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4e43feb16d75312cedd0caf5c217af2dd71332
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109433"
---
# <a name="mute-attribute"></a><span data-ttu-id="7fc44-103">靜音屬性</span><span class="sxs-lookup"><span data-stu-id="7fc44-103">mute Attribute</span></span>

> [!Note]  
> <span data-ttu-id="7fc44-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="7fc44-104">\[Deprecated.</span></span> <span data-ttu-id="7fc44-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="7fc44-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7fc44-106">`mute`屬性會指定物件的靜音狀態。</span><span class="sxs-lookup"><span data-stu-id="7fc44-106">The `mute` attribute specifies the object's mute state.</span></span> <span data-ttu-id="7fc44-107">如果值為 **TRUE**，則不會轉譯物件和其子系。</span><span class="sxs-lookup"><span data-stu-id="7fc44-107">If the value is **TRUE**, neither the object nor its children are rendered.</span></span> <span data-ttu-id="7fc44-108">如果此值為 **FALSE**，則會轉譯物件，並根據其本身的靜音狀態來呈現其子系。</span><span class="sxs-lookup"><span data-stu-id="7fc44-108">If the value is **FALSE**, the object is rendered, and its children are rendered according to their own mute state.</span></span> <span data-ttu-id="7fc44-109">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7fc44-109">The default value is **FALSE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="7fc44-110">可能的值</span><span class="sxs-lookup"><span data-stu-id="7fc44-110">Possible Values</span></span>

<span data-ttu-id="7fc44-111">下列值定義為 TRUE： y、Y、t、T、1。</span><span class="sxs-lookup"><span data-stu-id="7fc44-111">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="7fc44-112">下列值定義為 FALSE： n、N、f、F、0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="7fc44-112">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="7fc44-113">套用至</span><span class="sxs-lookup"><span data-stu-id="7fc44-113">Applies To</span></span>

<span data-ttu-id="7fc44-114">[**剪輯**](clip-element.md)、 [**複合**](composite-element.md)、 [**效果**](effect-element.md)、 [**群組**](group-element.md)、 [**時間軸**](timeline-element.md)、 [**轉換**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="7fc44-114">[**clip**](clip-element.md), [**composite**](composite-element.md), [**effect**](effect-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="7fc44-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7fc44-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc44-116">XTL 屬性</span><span class="sxs-lookup"><span data-stu-id="7fc44-116">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="7fc44-117">**IAMTimelineObj::SetMuted**</span><span class="sxs-lookup"><span data-stu-id="7fc44-117">**IAMTimelineObj::SetMuted**</span></span>](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



