---
title: AmbientAttributes.slideTo
description: SlideTo 方法會將控制項移至新的位置。 控制項在指定的時間週期內以非線性方式移動。
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- AmbientAttributes. slideTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deb214046ace59094b6bd5c362dfa716b9fceb57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984413"
---
# <a name="ambientattributesslideto"></a><span data-ttu-id="8784c-105">AmbientAttributes.slideTo</span><span class="sxs-lookup"><span data-stu-id="8784c-105">AmbientAttributes.slideTo</span></span>

<span data-ttu-id="8784c-106">**SlideTo** 方法會將控制項移至新的位置。</span><span class="sxs-lookup"><span data-stu-id="8784c-106">The **slideTo** method moves the control to a new location.</span></span> <span data-ttu-id="8784c-107">控制項在指定的時間週期內以非線性方式移動。</span><span class="sxs-lookup"><span data-stu-id="8784c-107">The control moves in a non-linear fashion over the specified time period.</span></span>

``` syntax
        elementID.slideTo(newX, newY, moveTime)
```

## <a name="parameters"></a><span data-ttu-id="8784c-108">參數</span><span class="sxs-lookup"><span data-stu-id="8784c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8784c-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span><span class="sxs-lookup"><span data-stu-id="8784c-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span></span>
</dt> <dd>

<span data-ttu-id="8784c-110">**數值** (**long**) 指定控制項 **左方** 屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="8784c-110">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="8784c-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span><span class="sxs-lookup"><span data-stu-id="8784c-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span></span>
</dt> <dd>

<span data-ttu-id="8784c-112">**數值** (**long**) 指定控制項 **頂端** 屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="8784c-112">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="8784c-113"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span><span class="sxs-lookup"><span data-stu-id="8784c-113"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span></span>
</dt> <dd>

<span data-ttu-id="8784c-114">**Number** (**long**) 指定控制項移至新位置所需的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8784c-114">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8784c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8784c-115">Return Value</span></span>

<span data-ttu-id="8784c-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8784c-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8784c-117">備註</span><span class="sxs-lookup"><span data-stu-id="8784c-117">Remarks</span></span>

<span data-ttu-id="8784c-118">這個方法與 **moveTo** 不同，後者會在移動控制項時建立線性動作。</span><span class="sxs-lookup"><span data-stu-id="8784c-118">This method is different from **moveTo**, which creates a linear motion when moving the control.</span></span> <span data-ttu-id="8784c-119">這個方法所建立的非線性動畫是一個滑動動作，可從動作開頭的零速度加速，並在結束時減速回零，以順利停止。</span><span class="sxs-lookup"><span data-stu-id="8784c-119">The non-linear motion created by this method is a sliding motion that accelerates from a speed of zero at the beginning of the motion and decelerates back to zero at the end, coming to a smooth stop.</span></span>

## <a name="requirements"></a><span data-ttu-id="8784c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8784c-120">Requirements</span></span>



| <span data-ttu-id="8784c-121">需求</span><span class="sxs-lookup"><span data-stu-id="8784c-121">Requirement</span></span> | <span data-ttu-id="8784c-122">值</span><span class="sxs-lookup"><span data-stu-id="8784c-122">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="8784c-123">版本</span><span class="sxs-lookup"><span data-stu-id="8784c-123">Version</span></span><br/> | <span data-ttu-id="8784c-124">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="8784c-124">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8784c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8784c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8784c-126">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="8784c-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="8784c-127">**AmbientAttributes left**</span><span class="sxs-lookup"><span data-stu-id="8784c-127">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="8784c-128">**AmbientAttributes**</span><span class="sxs-lookup"><span data-stu-id="8784c-128">**AmbientAttributes.moveTo**</span></span>](ambientattributes-moveto.md)
</dt> <dt>

[<span data-ttu-id="8784c-129">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="8784c-129">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> </dl>

 

 





