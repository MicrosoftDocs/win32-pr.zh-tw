---
description: Swapinputs 屬性會指定是否交換轉換輸入。 如果值為 TRUE，則會交換輸入。 預設值為 FALSE。
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: swapinputs 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e2f02c642283e90b994bcd1bfa9e05076a7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320603"
---
# <a name="swapinputs-attribute"></a><span data-ttu-id="2c49f-105">swapinputs 屬性</span><span class="sxs-lookup"><span data-stu-id="2c49f-105">swapinputs Attribute</span></span>

> [!Note]  
> <span data-ttu-id="2c49f-106">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="2c49f-106">\[Deprecated.</span></span> <span data-ttu-id="2c49f-107">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="2c49f-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2c49f-108">`swapinputs`屬性指定是否交換轉換輸入。</span><span class="sxs-lookup"><span data-stu-id="2c49f-108">The `swapinputs` attribute specifies whether to swap transition inputs.</span></span> <span data-ttu-id="2c49f-109">如果值為 **TRUE**，則會交換輸入。</span><span class="sxs-lookup"><span data-stu-id="2c49f-109">If the value is **TRUE**, the inputs are swapped.</span></span> <span data-ttu-id="2c49f-110">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="2c49f-110">The default value is **FALSE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="2c49f-111">可能的值</span><span class="sxs-lookup"><span data-stu-id="2c49f-111">Possible Values</span></span>

<span data-ttu-id="2c49f-112">下列值定義為 TRUE： y、Y、t、T、1。</span><span class="sxs-lookup"><span data-stu-id="2c49f-112">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="2c49f-113">下列值定義為 FALSE： n、N、f、F、0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="2c49f-113">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="2c49f-114">套用至</span><span class="sxs-lookup"><span data-stu-id="2c49f-114">Applies To</span></span>

[<span data-ttu-id="2c49f-115">**過渡**</span><span class="sxs-lookup"><span data-stu-id="2c49f-115">**transition**</span></span>](transition-element.md)

## <a name="remarks"></a><span data-ttu-id="2c49f-116">備註</span><span class="sxs-lookup"><span data-stu-id="2c49f-116">Remarks</span></span>

<span data-ttu-id="2c49f-117">根據預設，轉換會從所有較低優先順序層級的複合開始至轉換所在的圖層。</span><span class="sxs-lookup"><span data-stu-id="2c49f-117">By default, a transition proceeds from the composite of all lower-priority layers to the layer on which the transition resides.</span></span> <span data-ttu-id="2c49f-118">如果 `swapinputs` 屬性是1，則會反轉此方向。</span><span class="sxs-lookup"><span data-stu-id="2c49f-118">If the `swapinputs` attribute is 1, this direction is reversed.</span></span> <span data-ttu-id="2c49f-119">如需有關 DES 所使用之分層模型的詳細資訊，請參閱 [時間軸模型](the-timeline-model.md)。</span><span class="sxs-lookup"><span data-stu-id="2c49f-119">For more information about the layering model used by DES, see [The Timeline Model](the-timeline-model.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2c49f-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c49f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c49f-121">XTL 屬性</span><span class="sxs-lookup"><span data-stu-id="2c49f-121">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="2c49f-122">**IAMTimelineTrans::SetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="2c49f-122">**IAMTimelineTrans::SetSwapInputs**</span></span>](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



