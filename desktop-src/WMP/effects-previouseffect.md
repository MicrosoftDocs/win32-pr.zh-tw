---
title: 效果。 previousEffect
description: PreviousEffect 方法會顯示先前的視覺效果，並略過預設值。
ms.assetid: f1cfef29-0241-4028-b047-4f17bf0e9250
keywords:
- 效果： previousEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.previousEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b5482e7c202d6d35f3a833b5bafc8a41dca38956
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984883"
---
# <a name="effectspreviouseffect"></a><span data-ttu-id="4ab37-104">效果。 previousEffect</span><span class="sxs-lookup"><span data-stu-id="4ab37-104">EFFECTS.previousEffect</span></span>

<span data-ttu-id="4ab37-105">**PreviousEffect** 方法會顯示先前的視覺效果，並略過預設值。</span><span class="sxs-lookup"><span data-stu-id="4ab37-105">The **previousEffect** method displays the previous visualization, skipping presets.</span></span>

``` syntax
        elementID.previousEffect()
```

## <a name="parameters"></a><span data-ttu-id="4ab37-106">參數</span><span class="sxs-lookup"><span data-stu-id="4ab37-106">Parameters</span></span>

<span data-ttu-id="4ab37-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4ab37-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ab37-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ab37-108">Return Value</span></span>

<span data-ttu-id="4ab37-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4ab37-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ab37-110">備註</span><span class="sxs-lookup"><span data-stu-id="4ab37-110">Remarks</span></span>

<span data-ttu-id="4ab37-111">這個方法會以撰寫順序顯示先前的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="4ab37-111">This method displays the previous visualization in the authoring order.</span></span> <span data-ttu-id="4ab37-112">如果目前的視覺效果是撰寫順序中的第一個視覺效果，而且如果 **allowAll** 為 false，則最後一個視覺效果會成為最新的視覺效果。</span><span class="sxs-lookup"><span data-stu-id="4ab37-112">If the current visualization is the first in the authoring order, and if **allowAll** is false, the last visualization is made current.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ab37-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ab37-113">Requirements</span></span>



| <span data-ttu-id="4ab37-114">需求</span><span class="sxs-lookup"><span data-stu-id="4ab37-114">Requirement</span></span> | <span data-ttu-id="4ab37-115">值</span><span class="sxs-lookup"><span data-stu-id="4ab37-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4ab37-116">版本</span><span class="sxs-lookup"><span data-stu-id="4ab37-116">Version</span></span><br/> | <span data-ttu-id="4ab37-117">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="4ab37-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4ab37-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ab37-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ab37-119">**效果元素**</span><span class="sxs-lookup"><span data-stu-id="4ab37-119">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="4ab37-120">**效果。 nextEffect**</span><span class="sxs-lookup"><span data-stu-id="4ab37-120">**EFFECTS.nextEffect**</span></span>](effects-nexteffect.md)
</dt> <dt>

[<span data-ttu-id="4ab37-121">**效果。 allowAll**</span><span class="sxs-lookup"><span data-stu-id="4ab37-121">**EFFECTS.allowAll**</span></span>](effects-allowall.md)
</dt> </dl>

 

 





