---
title: AmbientAttributes.moveSizeTo
description: MoveSizeTo 方法會移動控制項，並在新的位置指定控制項的新大小。 控制項會在指定的時間週期內以動畫方式移動和調整大小。
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- AmbientAttributes. moveSizeTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406d48772e85a55ab82241518d499182931cc2fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976005"
---
# <a name="ambientattributesmovesizeto"></a><span data-ttu-id="292b4-105">AmbientAttributes.moveSizeTo</span><span class="sxs-lookup"><span data-stu-id="292b4-105">AmbientAttributes.moveSizeTo</span></span>

<span data-ttu-id="292b4-106">**MoveSizeTo** 方法會移動控制項，並在新的位置指定控制項的新大小。</span><span class="sxs-lookup"><span data-stu-id="292b4-106">The **moveSizeTo** method moves the control and specifies a new size for the control in the new location.</span></span> <span data-ttu-id="292b4-107">控制項會在指定的時間週期內以動畫方式移動和調整大小。</span><span class="sxs-lookup"><span data-stu-id="292b4-107">The control moves and resizes in an animated fashion over the specified time period.</span></span>

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
```

## <a name="parameters"></a><span data-ttu-id="292b4-108">參數</span><span class="sxs-lookup"><span data-stu-id="292b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="292b4-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span><span class="sxs-lookup"><span data-stu-id="292b4-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span></span>
</dt> <dd>

<span data-ttu-id="292b4-110">**數值** (**long**) 指定控制項 **左方** 屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="292b4-110">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="292b4-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span><span class="sxs-lookup"><span data-stu-id="292b4-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span></span>
</dt> <dd>

<span data-ttu-id="292b4-112">**數值** (**long**) 指定控制項 **頂端** 屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="292b4-112">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="292b4-113"><span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*</span><span class="sxs-lookup"><span data-stu-id="292b4-113"><span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*</span></span>
</dt> <dd>

<span data-ttu-id="292b4-114">為控制項的 **width** 屬性指定新值的 (**long**) **數位**。</span><span class="sxs-lookup"><span data-stu-id="292b4-114">**Number** (**long**) specifying the new value for the **width** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="292b4-115"><span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*</span><span class="sxs-lookup"><span data-stu-id="292b4-115"><span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*</span></span>
</dt> <dd>

<span data-ttu-id="292b4-116">**數值** (**long**) 指定控制項 **height** 屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="292b4-116">**Number** (**long**) specifying the new value for the **height** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="292b4-117"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span><span class="sxs-lookup"><span data-stu-id="292b4-117"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span></span>
</dt> <dd>

<span data-ttu-id="292b4-118">**Number** (**long**) 指定控制項移至新位置所需的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="292b4-118">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> <dt>

<span data-ttu-id="292b4-119"><span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*</span><span class="sxs-lookup"><span data-stu-id="292b4-119"><span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*</span></span>
</dt> <dd>

<span data-ttu-id="292b4-120">**布林值** ，指定移動控制項時所建立的動作類型。</span><span class="sxs-lookup"><span data-stu-id="292b4-120">**Boolean** specifying the type of motion created when moving the control.</span></span>



| <span data-ttu-id="292b4-121">值</span><span class="sxs-lookup"><span data-stu-id="292b4-121">Value</span></span> | <span data-ttu-id="292b4-122">描述</span><span class="sxs-lookup"><span data-stu-id="292b4-122">Description</span></span>                                                             |
|-------|-------------------------------------------------------------------------|
| <span data-ttu-id="292b4-123">true</span><span class="sxs-lookup"><span data-stu-id="292b4-123">true</span></span>  | <span data-ttu-id="292b4-124">移動是非線性的 (滑動動作，可加速和減速) 。</span><span class="sxs-lookup"><span data-stu-id="292b4-124">Motion is non-linear (sliding motion that accelerates and decelerates).</span></span> |
| <span data-ttu-id="292b4-125">false</span><span class="sxs-lookup"><span data-stu-id="292b4-125">false</span></span> | <span data-ttu-id="292b4-126">動作是線性的。</span><span class="sxs-lookup"><span data-stu-id="292b4-126">Motion is linear.</span></span>                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="292b4-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="292b4-127">Return Value</span></span>

<span data-ttu-id="292b4-128">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="292b4-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="292b4-129">備註</span><span class="sxs-lookup"><span data-stu-id="292b4-129">Remarks</span></span>

<span data-ttu-id="292b4-130">控制項的動作可以是線性或非線性。</span><span class="sxs-lookup"><span data-stu-id="292b4-130">The motion of the control can be linear or non-linear.</span></span> <span data-ttu-id="292b4-131">線性運動表示控制項會以固定速度移至新位置，突然開始和停止。</span><span class="sxs-lookup"><span data-stu-id="292b4-131">Linear motion means the control moves at a constant speed to its new location, starting and stopping abruptly.</span></span> <span data-ttu-id="292b4-132">當指定非線性動作時，會建立滑動動作，以加速從動作開頭的零開始，並在結束時減速回零，以順利停止。</span><span class="sxs-lookup"><span data-stu-id="292b4-132">When non-linear motion is specified, a sliding motion is created that accelerates from zero at the beginning of the motion and decelerates back to zero at the end, coming to a smooth stop.</span></span>

## <a name="requirements"></a><span data-ttu-id="292b4-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="292b4-133">Requirements</span></span>



| <span data-ttu-id="292b4-134">需求</span><span class="sxs-lookup"><span data-stu-id="292b4-134">Requirement</span></span> | <span data-ttu-id="292b4-135">值</span><span class="sxs-lookup"><span data-stu-id="292b4-135">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="292b4-136">版本</span><span class="sxs-lookup"><span data-stu-id="292b4-136">Version</span></span><br/> | <span data-ttu-id="292b4-137">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="292b4-137">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="292b4-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="292b4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="292b4-139">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="292b4-139">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="292b4-140">**AmbientAttributes 高度**</span><span class="sxs-lookup"><span data-stu-id="292b4-140">**AmbientAttributes.height**</span></span>](ambientattributes-height.md)
</dt> <dt>

[<span data-ttu-id="292b4-141">**AmbientAttributes left**</span><span class="sxs-lookup"><span data-stu-id="292b4-141">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="292b4-142">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="292b4-142">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> <dt>

[<span data-ttu-id="292b4-143">**AmbientAttributes 寬度**</span><span class="sxs-lookup"><span data-stu-id="292b4-143">**AmbientAttributes.width**</span></span>](ambientattributes-width.md)
</dt> </dl>

 

 





