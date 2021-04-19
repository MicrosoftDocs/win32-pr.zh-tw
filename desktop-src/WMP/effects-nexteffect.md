---
title: 效果。 nextEffect
description: NextEffect 方法會顯示下一個視覺效果的第一個預設值，略過中間的預設值。
ms.assetid: dedd8e8b-2337-46f5-91a8-43ef54c86012
keywords:
- 效果： nextEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.nextEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b84d7ec4d6095ffdac2a0f0592aa3f3e832e68e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990280"
---
# <a name="effectsnexteffect"></a><span data-ttu-id="2638d-104">效果。 nextEffect</span><span class="sxs-lookup"><span data-stu-id="2638d-104">EFFECTS.nextEffect</span></span>

<span data-ttu-id="2638d-105">**NextEffect** 方法會顯示下一個視覺效果的第一個預設值，略過中間的預設值。</span><span class="sxs-lookup"><span data-stu-id="2638d-105">The **nextEffect** method displays the first preset of the next visualization, skipping intervening presets.</span></span>

``` syntax
        elementID.nextEffect()
```

## <a name="parameters"></a><span data-ttu-id="2638d-106">參數</span><span class="sxs-lookup"><span data-stu-id="2638d-106">Parameters</span></span>

<span data-ttu-id="2638d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2638d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2638d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2638d-108">Return Value</span></span>

<span data-ttu-id="2638d-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2638d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2638d-110">備註</span><span class="sxs-lookup"><span data-stu-id="2638d-110">Remarks</span></span>

<span data-ttu-id="2638d-111">這個方法會以撰寫順序顯示下一個視覺效果的第一個預設值。</span><span class="sxs-lookup"><span data-stu-id="2638d-111">This method displays the first preset of the next visualization in the authoring order.</span></span> <span data-ttu-id="2638d-112">如果目前的視覺效果是撰寫順序中的最後一個視覺效果，而且如果 **allowAll** 為 false，則會將第一個視覺效果設為最新。</span><span class="sxs-lookup"><span data-stu-id="2638d-112">If the current visualization is the last in the authoring order, and if **allowAll** is false, the first visualization is made current.</span></span>

## <a name="requirements"></a><span data-ttu-id="2638d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2638d-113">Requirements</span></span>



| <span data-ttu-id="2638d-114">需求</span><span class="sxs-lookup"><span data-stu-id="2638d-114">Requirement</span></span> | <span data-ttu-id="2638d-115">值</span><span class="sxs-lookup"><span data-stu-id="2638d-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2638d-116">版本</span><span class="sxs-lookup"><span data-stu-id="2638d-116">Version</span></span><br/> | <span data-ttu-id="2638d-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="2638d-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2638d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2638d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2638d-119">**效果元素**</span><span class="sxs-lookup"><span data-stu-id="2638d-119">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="2638d-120">**效果。 allowAll**</span><span class="sxs-lookup"><span data-stu-id="2638d-120">**EFFECTS.allowAll**</span></span>](effects-allowall.md)
</dt> <dt>

[<span data-ttu-id="2638d-121">**效果。 previousEffect**</span><span class="sxs-lookup"><span data-stu-id="2638d-121">**EFFECTS.previousEffect**</span></span>](effects-previouseffect.md)
</dt> </dl>

 

 





